---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 70342620aeab42ba7236091e8aacc32ea44354ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930753"
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
Type: String
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

Certifikatet är base64-kodning av följande JSON-objekt (Java Object Notation), som är kodat i UTF-8:

{"data": " \<Base64-encoded-file\> ", "datatyp": " \<file-format\> ", "lösen ord": " \<pfx-file-password\> "}


För närvarande accepterar data typen bara. PFX-filer.

```yaml
Type: String
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
Type: IAzureContextContainer
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
Type: String
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
Type: PSVirtualMachine
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

### PSVirtualMachine
Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
