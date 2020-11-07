---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758398"
---
# Get-AzureKeyVaultCertificate

## Sammanfattning
Hämtar ett certifikat från ett nyckelord.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByVaultName (standard)
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByCertificateName
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateVersions
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedCertificates
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.

## BESKRIVS

### Exempel 1: skaffa ett certifikat
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.

### Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.

### Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.
Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.

## MALLPARAMETRAR

### -IncludeVersions
Anger att den här åtgärden får alla versioner av certifikatet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Anger om tidigare borttagna certifikat ska tas med i resultatet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på det certifikat som ska erhållas.

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på ett nyckelord.

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
Anger ett certifikats version.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

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

## VÄRDEN

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. CertificateIdentityItem]

### Microsoft. Azure. commands. valv. Models. KeyVaultCertificate

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureKeyVaultCertificate](./Add-AzureKeyVaultCertificate.md)

[Import-AzureKeyVaultCertificate](./Import-AzureKeyVaultCertificate.md)

[Remove-AzureKeyVaultCertificate](./Remove-AzureKeyVaultCertificate.md)

[Ångra-AzureKeyVaultSecretCertificate](./Undo-AzureKeyVaultSecretCertificate.md)
