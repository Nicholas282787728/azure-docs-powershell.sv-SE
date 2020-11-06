---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574655"
---
# Get-AzureKeyVaultSecret

## Sammanfattning
Hämtar hemligheterna i ett nyckeltal.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByVaultName (standard)
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureKeyVaultSecret** får hemligheter i ett nyckeltal.
Denna cmdlet tar emot specifik hemlighet eller alla hemligheter i ett nyckel valv.

## BESKRIVS

### Exempel 1: Hämta alla aktuella versioner av alla hemligheter i ett nyckeltal
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

Det här kommandot får de aktuella versionerna av alla hemligheter i det nyckelord som heter Contoso.

### Exempel 2: skaffa alla versioner av en viss hemlighet
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Det här kommandot får alla versioner av hemligheten som heter ITSecret i nyckel valvet contoso.

### Exempel 3: Skaffa den senaste versionen av en viss hemlighet
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Det här kommandot får den aktuella versionen av hemligheten som heter ITSecret i nyckel valvet contoso.

### Exempel 4: skaffa en specifik version av en viss hemlighet
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Det här kommandot får en specifik version av hemligheten som heter ITSecret i nyckel valvet contoso.

### Exempel 5: Hämta värdet oformaterad text för den aktuella versionen av en viss hemlighet
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Dessa kommandon får den aktuella versionen av en hemlighet som heter ITSecret och visar sedan det oformaterade textvärdet för den hemligheten.

### Exempel 6: Hämta alla hemligheter som tagits bort men inte rensats för detta huvud valv.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Det här kommandot får alla hemligheter som tagits bort tidigare, men inte rensats, i det nyckelord som heter Contoso.

### Exempel 7: hämtar den hemliga ITSecret som har tagits bort men inte rensats för detta nyckel valv.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Det här kommandot får den hemliga ITSecret som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.
Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för den här borttagna hemligheten.

## MALLPARAMETRAR

### -IncludeVersions
Visar att denna cmdlet får alla versioner av en hemlighet.
Den aktuella versionen av en hemlighet är den första i listan.
Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .

Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av hemligheten med det angivna *namnet*.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Anger om tidigare borttagna hemligheter ska visas i resultatet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den hemlighet som ska visas.

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det nyckel valv som hemligheten tillhör.
Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Anger den hemliga versionen.
Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
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

### Strängvärdet

## VÄRDEN

### List<Microsoft. Azure. commands. nyckel valv. Models. SecretIdentityItem>, Microsoft. Azure. kommandon. nyckel valv. Models. Secret, list<Microsoft. Azure. commands.. Models. DeletedSecretIdentityItem>, Microsoft. Azure. kommandon. nyckel valv. Models.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Ångra-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

