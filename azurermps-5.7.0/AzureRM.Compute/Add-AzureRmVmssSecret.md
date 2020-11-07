---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755266"
---
# Add-AzureRmVmssSecret

## Sammanfattning
Lägger till en hemlighet till en VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVmssSecret** lägger till en hemlighet till den virtuella datorns skal uppsättning (VMSS).
Hemligheten måste lagras i ett Azure Key-valv.
Mer information om viktiga valv finns i [Vad är Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Mer information om cmdletar finns i [cmdlets för Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) i Microsoft Developer Network Library eller cmdleten [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## BESKRIVS

### Exempel 1: lägga till en hemlighet på VMSS
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

I det här exemplet läggs en hemlighet till i VMSS.
Det första kommandot använder cmdleten Get-AzureRmKeyVault för att hämta en valv hemlighet från valvet ContosoVault och lagrar resultatet i variabeln som heter $Vault.
Med det andra kommandot används cmdleten **New-AzureRmVmssVaultCertificateConfig** för att skapa en konfiguration för ett valv certifikat med hjälp av den angivna certifikat-URL: en från certifikat arkivet med namnen certifikat och lagrar resultaten i variabeln som heter $CertConfig.
I det tredje kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.
Det fjärde kommandot lägger till en hemlighet till VMSS med hjälp av valv hemligheten med nyckel resurs-ID: t och valvet-certifikatet som lagras i $Vault och $CertConfig variabler.

## MALLPARAMETRAR

### -SourceVaultId
Anger resurs-ID för det huvud valv som innehåller de certifikat som du kan lägga till på den virtuella datorn.
Det här värdet fungerar också som nycklar för att lägga till flera certifikat.
Det innebär att du kan använda samma värde för parametern *SourceVaultId* när du lägger till flera certifikat från samma Key-valv.

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

### -VaultCertificate
Anger det valv **certifikat** objekt som innehåller certifikatets URL och certifikat namn.
Du kan använda cmdleten [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) för att skapa det här objektet.

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger VMSS-objektet.
Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa det här objektet.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
