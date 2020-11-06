---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574653"
---
# Get-AzureRmKeyVault

## Sammanfattning
Hämtar viktiga valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetVaultByName
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmKeyVault** hämtar information om viktiga valv i ett abonnemang. Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.

Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.

## BESKRIVS

### Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang
```
PS C:\>Get-AzureRMKeyVault
```

Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.

### Exempel 2: skaffa ett speciellt nyckeltal
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

Det här kommandot får Key-valvet som heter Contoso03Vault i ditt nuvarande abonnemang och lagrar det sedan i $MyVault variabel. Du kan kontrol lera egenskaperna för $MyVault för att få information om nyckelordet.

### Exempel 3: Hämta viktiga valv i en resurs grupp
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.

### Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.

### Exempel 5: skaffa ett borttaget nyckeltal
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Det här kommandot hämtar informationen om viktiga valv som heter Contoso03Vault i ditt nuvarande abonnemang och i eastus2 region.

## MALLPARAMETRAR

### -InRemovedState
Anger om de tidigare borttagna valverna ska visas i resultatet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Platsen för det borttagna valvet.

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som är kopplad till Key Vault eller Key vaultes.

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel:

@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på Key-valvet.

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. PSVault

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. PSVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmKeyVault](./New-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
