---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233430"
---
# Add-AzVMSecret

## SYNOPSIS
Gör en hemlig dator.

## SYNTAX

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzVMSecret** ger en hemlig fil till en virtuell dator.
Med det här värdet kan du lägga till ett certifikat till den virtuella datorn.
Hemligheten måste lagras i ett nyckelvalv.
Mer information om nyckelvalv finns i [Vad är Azure-nyckelvalv?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Mer information om cmdlets finns i [Azure-cmdlets](/powershell/module/az.keyvault) för nyckelvalv eller [Set-AzKeyVaultSecret-cmdleten.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## EXEMPEL

### Exempel 1: Lägg till en hemlig dator
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Det första kommandot skapar ett virtuellt maskinobjekt och lagrar det sedan i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Det andra kommandot skapar ett autentiseringsobjekt med hjälp av cmdleten Get-Credential och lagrar sedan resultatet i $Credential variabeln.
Kommandot uppmanar dig att ange ett användarnamn och lösenord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .
Det tredje kommandot använder **cmdleten Set-AzVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.
Det fjärde kommandot tilldelar ett källvalv-ID till variabeln $SourceVaultId för senare användning.
Kommandot förutsätter att den $SubscriptionId har ett lämpligt värde.
Det femte kommandot tilldelar ett värde till variabeln $CertificateStore 01 för senare användning.
Det sjätte kommandot tilldelar en URL-adress för ett certifikatarkiv.
Det sjunde kommandot lägger till en hemligt till den virtuella datorn som lagras i $VirtualMachine.
SourceVaultId-parametern anger nyckelvalvet.
Kommandot anger namnet på certifikatarkivet och certifikatets URL.
Du kan köra **Add-AzVMSecret flera gånger för** att lägga till hemligheter för andra certifikat.

## PARAMETERS

### -CertificateStore
Anger namnet på ett certifikatarkiv på den virtuella datorn som kör Windows-operativsystemet.
Den här cmdleten lägger till certifikatet i lagret som den här parametern anger.
Du kan bara ange den här parametern för virtuella datorer som kör Windows-operativsystemet.

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
Anger URL-adressen som pekar på en nyckelvalvshemlighet som innehåller ett certifikat.
Certifikatet är Base64-kodningen för följande JavaScript Object Notation-objekt (JSON), som kodas i UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } För närvarande accepterar dataType endast \<pfx-file-password\> .pfx-filer.

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
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Anger resurs-ID för nyckelvalvet som innehåller certifikaten som du kan lägga till i den virtuella datorn.
Det här värdet är också nyckeln till att lägga till flera certifikat.
Det innebär att du kan använda samma värde för *SourceVaultId när* du lägger till flera certifikat från samma nyckelvalv.

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
Anger det virtuella datorobjektet som denna cmdlet ändrar.
Om du vill hämta ett virtuellt datorobjekt använder [du cmdleten Get-AzVM.](./Get-AzVM.md)
Du kan använda cmdleten [New-AzVMConfig](./New-AzVMConfig.md) till att skapa ett virtuellt datorobjekt.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
