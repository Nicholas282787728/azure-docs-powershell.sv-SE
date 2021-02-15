---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238991"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Lägger till information i svarsfilen för obevakade Windows-inställningar.

## SYNTAX

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Add-AzVMAdditionalUnattendContent** lägger till information i svarsfilen för obevakade Windows-inställningar.
Ange ytterligare bas-64-kodad .xml-formaterad information som denna cmdlet lägger till unattend.xml filen.

## EXEMPEL

### Exempel 1: Lägga till innehåll i unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Det första kommandot hämtar tillgänglighetsuppsättningen med namnet AvailabilitySet03 i resursgruppen ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabeln.
Det andra kommandot skapar ett virtuellt maskinobjekt och lagrar det sedan i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Den virtuella datorn tillhör den tillgänglighetsuppsättning som lagras i $AvailabilitySet.
Det tredje kommandot skapar ett autentiseringsobjekt med hjälp av cmdleten Get-Credential och lagrar sedan resultatet i $Credential variabeln.
Kommandot uppmanar dig att ange ett användarnamn och lösenord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .
Det fjärde kommandot använder **cmdleten Set-AzVMOperatingSystem** till att konfigurera den virtuella datorn som lagras i $VirtualMachine.
Det femte kommandot tilldelar innehåll till den $AucContent variabeln.
Innehållet innehåller ett lösenord.
Det slutliga kommandot lägger till det innehåll som lagrats $AucContent i unattend.xml filen.

## PARAMETERS

### -Innehåll
Anger 64-kodat XML-formaterat innehåll.
Den här cmdleten lägger till innehållet unattend.xml filen.
XML-innehållet måste vara mindre än 4 kB och måste innehålla rotelementet för inställningen eller funktionen som denna cmdlet infogar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -SettingName
Anger namnet på den inställning som innehållet gäller för.
De godtagbara värdena för den här parametern är:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det virtuella datorobjektet som denna cmdlet ändrar.
Om du vill hämta ett virtuellt datorobjekt använder [du cmdleten Get-AzVM.](./Get-AzVM.md)
Skapa ett virtuellt maskinobjekt med cmdleten [New-AzVMConfig.](./New-AzVMConfig.md)

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

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
