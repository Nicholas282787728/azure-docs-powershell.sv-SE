---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922742"
---
# Get-AzKeyVault

## Sammanfattning
Hämtar viktiga valv.

## FRÅGESYNTAXEN

### GetVaultByName
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzKeyVault** hämtar information om viktiga valv i ett abonnemang. Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.

Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.

## BESKRIVS

### Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang
```
PS C:\>Get-AzKeyVault
```

Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.

### Exempel 2: skaffa ett speciellt nyckeltal
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

Det här kommandot får Key-valvet som heter Contoso03Vault i ditt nuvarande abonnemang och lagrar det sedan i $MyVault variabel. Du kan kontrol lera egenskaperna för $MyVault för att få information om nyckelordet.

### Exempel 3: Hämta viktiga valv i en resurs grupp
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.

### Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang
```
PS C:\>Get-AzKeyVault -InRemovedState
```

Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.

### Exempel 5: skaffa ett borttaget nyckeltal
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Det här kommandot hämtar informationen om viktiga valv som heter Contoso03Vault i ditt nuvarande abonnemang och i eastus2 region.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Anger om de tidigare borttagna valverna ska visas i resultatet.

```yaml
Type: SwitchParameter
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
Type: String
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
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel:

@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: Hashtable
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
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. PSVault

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. PSVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzKeyVault](./New-AzKeyVault.md)

[Remove-AzKeyVault](./Remove-AzKeyVault.md)
