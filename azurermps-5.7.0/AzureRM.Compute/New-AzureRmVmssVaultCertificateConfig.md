---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579612"
---
# New-AzureRmVmssVaultCertificateConfig

## Sammanfattning
Skapar en konfiguration för ett nyckelord för valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).
Utdata från denna cmdlet är avsedda att användas med Add-AzureRmVmssSecret cmdlet.

## BESKRIVS

### Exempel 1: skapa en konfiguration för ett valv certifikat
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.

## MALLPARAMETRAR

### -CertificateStore
Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.
Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Anger URI för ett certifikat som är lagrat i Key Vault.

Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8:


{"data": " \<Base64-encoded-certificate\> ", "datatyp": "PFX", "lösen ord": " \<pfx-file-password\> "}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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

###  
Denna cmdlet genererar inga utdata.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVmssSecret](./Add-AzureRmVmssSecret.md)
