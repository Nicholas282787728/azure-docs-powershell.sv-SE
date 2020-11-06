---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 539c9306709b7044f2a3d7263ac8168d59f54e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580827"
---
# Add-AzureRmVMSecret

## Sammanfattning
Lägger till en hemlighet till en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVMSecret** lägger till en hemlighet till en virtuell dator.
Med det här värdet kan du lägga till ett certifikat till den virtuella datorn.
Hemligheten måste lagras i ett nyckel valv.
Mer information om viktiga valv finns i [Vad är Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Mer information om cmdletar finns i cmdlets för [Azure Key vaulting](https://msdn.microsoft.com/library/azure/dn868052.aspx) i Microsoft Developer Network Library eller cmdleten [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## BESKRIVS

### Exempel 1: lägga till en hemlighet på en virtuell dator
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Det andra kommandot skapar ett Credential-objekt med hjälp av Get-Credential cmdlet och lagrar sedan resultatet i variabeln $Credential.
Kommandot frågar efter användar namn och lösen ord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .
I det tredje kommandot används cmdleten **set-AzureRmVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.
Det fjärde kommandot tilldelar ett valv-ID till $SourceVaultId variabel för senare användning.
Kommandot utgår från att variabeln $SubscriptionId har ett lämpligt värde.
Det femte kommandot tilldelar ett värde till variabeln $CertificateStore 01 för senare användning.
Det sjätte kommandot tilldelar en URL till en certifikat lagrings plats.
Det sjunde kommandot lägger till en hemlighet till den virtuella datorn som lagras i $VirtualMachine.
Parametern SourceVaultId anger Key Vault.
Kommandot anger namnet på certifikat arkivet och URL-adressen till certifikatet.
Du kan köra **AzureRmVMSecret** flera gånger för att lägga till hemligheter för andra certifikat.

## MALLPARAMETRAR

### -CertificateStore
Anger namnet på ett certifikat Arkiv på den virtuella dator som kör operativ systemet Windows.
Denna cmdlet lägger till certifikatet i arkivet som den här parametern anger.
Du kan endast ange den här parametern för virtuella datorer som kör operativ systemet Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Anger URL-adressen som pekar på en nyckel valv hemlighet som innehåller ett certifikat.
Certifikatet är base64-kodningen för följande JavaScript-objekt, som är kodade i UTF-8: {"data": " \<Base64-encoded-file\> ", "datatyp": " \<file-format\> ", "lösen ord": " \<pfx-file-password\> "}, för närvarande accepterar data typen bara. PFX-filer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

### -SourceVaultId
Anger resurs-ID för det huvud valv som innehåller de certifikat som du kan lägga till på den virtuella datorn.
Det här värdet fungerar också som nycklar för att lägga till flera certifikat.
Det innebär att du kan använda samma värde för *SourceVaultId* när du lägger till flera certifikat från samma Key-valv.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det virtuella dator objekt som denna cmdlet ändrar.
Använd cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) för att hämta ett virtuellt dator objekt.
Du kan använda cmdleten [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) för att skapa ett virtuellt dator objekt.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
