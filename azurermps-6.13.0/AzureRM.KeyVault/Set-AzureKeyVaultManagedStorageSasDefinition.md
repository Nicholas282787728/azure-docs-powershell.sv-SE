---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576258"
---
# Set-AzureKeyVaultManagedStorageSasDefinition

## Sammanfattning
Ställer in en säkerhets beskrivning för en delad åtkomst (SAS) med ett huvud valv för ett visst offentligt hanterat Azure Storage-konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Standard (standard)
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Ställer in en säkerhets beskrivning för en signatur (SAS) med ett angivet Azure Storage-konto för viktiga valv. Detta anger också en hemlighet som kan användas för att hämta SAS-token per denna SAS-definition.
SAS-token genereras med de här parametrarna och den aktiva nyckeln för det hanterade Azure Storage-kontot för Key valv.

## BESKRIVS

### Exempel 1: Ange en SAS-definition för konto typer och få en aktuell SAS-token baserad på den
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

Anger ett konto för SAS-definitionen för konton på ett valv-hanterat lagrings konto ' mysa ' i valv ' mykv '. Ordningen ovan gör följande:
  - hämtar ett (befintligt) lagrings konto
  - hämtar ett (befintligt) huvud valv
  - lägger till ett valv-hanterat lagrings konto i valvet, ställer in KEY1 som aktiv-nycklar och med en återställnings period på 180 dagar
  - anger en lagrings kontext för det angivna lagrings kontot med KEY1
  - skapar ett konto SAS-token för tjänster, fil, tabell och kö, för resurs typ tjänst, behållare och objekt med alla behörigheter, över https och med angivna start-och slutdatum
  - anger en säkerhets definition för ett nyckel valv som hanteras i ett valv i valvet med mallen URI som den SAS-token som skapades ovan, av SAS-typ "konto" och giltigt i 30 dagar
  - hämtar den faktiska åtkomst-token från den nyckel valv hemlighet som motsvarar SAS-definitionen

## MALLPARAMETRAR

### -AccountName
Namn på hanterat lagrings konto för viktiga valv. Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inaktivera
Inaktiverar användning av SAS-definition för generering av SAS-token.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ManagedStorageAccount-objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namn på lagrings-sa. Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasType
Säkerhets Association för lagring.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateUri
URI för definitions mal len lagrings Association med SAS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityPeriod
Giltighets tids period som används för att ange förfallo tiden för SAS-token från den tid då den genereras

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem
Parametrar: InputObject (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinition

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azureâ € ofta ‹ RM. â € ofta ‹ keyâ € ofta ‹ valv](/powershell/module/azurerm.keyvault/)
