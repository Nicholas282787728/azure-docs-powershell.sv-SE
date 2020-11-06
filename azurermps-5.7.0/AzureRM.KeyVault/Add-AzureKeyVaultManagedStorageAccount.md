---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575650"
---
# Add-AzureKeyVaultManagedStorageAccount

## Sammanfattning
Lägger till ett befintligt Azure Storage-konto till det angivna nyckel valvet för dess nycklar för att hanteras av nyckel valv tjänsten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Konfigurerar ett befintligt Azure Storage-konto med nyckel valv för lagrings konto nycklar som ska hanteras av nyckel valv. Lagrings kontot måste redan finnas. Lagrings nycklarna exponeras aldrig för den som ringer.
Key valv regenererar och växlar den aktiva nyckeln automatiskt baserat på återställnings perioden.

## BESKRIVS

### Exempel 1: Ange ett Azure Storage-konto med nyckel valv för att hantera dess nycklar
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Ställer in ett lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet. Den aktiva knappen är ' KEY1 '. Denna nyckel används för att generera SAS-token. Key valv återskapar ' key2 '-nyckeln efter återgenererings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln. Den här processen för automatisk förnyelse fortsätter mellan ' KEY1 ' och ' key2 ' med en lucka på 90 dagar.

### Exempel 2: Ange ett klassiskt Azure Storage-konto med nyckel valv för att hantera dess nycklar
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Ställer in ett klassiskt lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet. Den aktiva tangenten är "primär". Denna nyckel används för att generera SAS-token. Key valv återskapar ' sekundär '-nyckeln efter återställnings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln. Den här processen för automatisk förnyelse fortsätter mellan ' primär ' och ' sekundär ' med en lucka på 90 dagar.

## MALLPARAMETRAR

### -AccountName
Namn på hanterat lagrings konto för viktiga valv. Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
Azure Resource ID för lagrings kontot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Namn på lagrings konto nyckeln som måste användas för att skapa SAS-token.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inaktivera
Inaktiverar användning av hanterat lagrings kontots nyckel för generering av SAS-token.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRegenerateKey
Autoåterskapa-nyckeln. Om värdet är true får det hanterade lagrings kontots inaktiva nycklar automatisk omgenerering och blir den nya aktiva nyckeln efter återställnings perioden. Om det här är falskt skapas inte nycklar för hanterat lagrings konto automatiskt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegenerationPeriod
Återställnings period. Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatiskt återskapande lagrings konto och blir den nya aktiva nyckeln.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel:

@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. ManagedStorageAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[AzureRM.](/powershell/module/azurerm.keyvault)
