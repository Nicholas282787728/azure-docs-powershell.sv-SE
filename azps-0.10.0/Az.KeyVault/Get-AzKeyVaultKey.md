---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922718"
---
# Get-AzKeyVaultKey

## Sammanfattning
Hämtar nyckel valv nycklar.

## FRÅGESYNTAXEN

### ByVaultName (standard)
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzKeyVaultKey** hämtar nyckel valv för Azure.
Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.

## BESKRIVS

### Exempel 1: Hämta alla nycklar i ett nyckel valv
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

Det här kommandot får alla nycklar i nyckel valvet contoso.

### Exempel 2: hämta den aktuella versionen av en-tangenten
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Med det här kommandot får du den aktuella versionen av den Key som heter ITPfx i nyckelordet contoso.

### Exempel 3: Hämta alla versioner av en viktig
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Det här kommandot får alla versioner som heter ITPfx i vaultnamed contoso.

### Exempel 4: skaffa en specifik version av en
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Det här kommandot får en specifik version av den Key som heter ITPfx i nyckelordet contoso.
När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.

### Exempel 5: Hämta alla de nycklar som har tagits bort men inte rensats för detta nyckel valv.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.

### Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Det här kommandot får den ITPfx som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.
Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.

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

### -IncludeVersions
Anger att denna cmdlet får alla versioner av en viktig.
Den aktuella versionen av en Key är den första som visas i listan.
Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .

Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Anger om tidigare borttagna nycklar ska visas i resultatet

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på det Key-paket som ska visas.

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.
Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.

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

### -Version
Anger huvud versionen.
Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Strängvärdet

## VÄRDEN

### List<Microsoft. Azure. kommandon. DeletedKeyIdentityItem. Models. KeyIdentityItem>, Microsoft. Azure. kommandon.-paket, list<Microsoft. Azure. commands.. Models.>, Microsoft. Azure. commands. Vault. Models.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Ångra-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)

