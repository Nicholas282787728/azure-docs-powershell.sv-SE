---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238631"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Anger egenskaper för operativsystemet för en virtuell dator.

## SYNTAX

### Windows (standard)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzVMOperatingSystem** anger egenskaper för operativsystem för en virtuell dator.
Du kan ange inloggningsuppgifter, datornamn och operativsystemstyp.

## EXEMPEL

### Exempel 1: Ange egenskaper för operativsystemet för nya virtuella datorer
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Det första kommandot konverterar ett lösenord till en säker sträng och lagrar det sedan i $SecurePassword variabeln.
Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .
Det andra kommandot skapar en autentiseringsuppgifter för användaren FullerP och lösenordet som lagras i $SecurePassword och lagrar sedan autentiserings uppgifter i $Credential variabeln.
Om du vill ha mer information skriver du `Get-Help New-Object` .
Det tredje kommandot hämtar tillgänglighetsuppsättningen med namnet AvailabilitySet03 i resursgruppen ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabeln.
Det fjärde kommandot skapar ett virtuellt maskinobjekt och lagrar det sedan i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Den virtuella datorn tillhör den tillgänglighetsuppsättning som lagras i $AvailabilitySet.
De följande fyra kommandona tilldelar värden till variabler som ska användas i följande kommando.
Eftersom du kan ange dessa strängar direkt i kommandot **Set-AzVMOperatingSystem** används den här metoden endast för läsbarhet.
Du kan dock använda en liknande metod i skript.
Det slutliga kommandot anger egenskaper för operativsystemet för den virtuella datorn som lagras $VirtualMachine.
Kommandot använder autentiseringsuppgifterna som lagras i $Credential.
Kommandot använder variabler som har tilldelats i tidigare kommandon för vissa parametrar.

## PARAMETERS

### -Datornamn
Anger namnet på datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Anger användarnamnet och lösenordet för den virtuella datorn som ett **PSCredential-objekt.**
Använd cmdleten Get-Credential för att få en autentiseringsuppgifter.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Anger en bas-64-kodad sträng med anpassade data.
Detta avkodas till en binär matris som sparas som en fil på den virtuella datorn.
Den maximala längden på den binära matrisen är 65 535 byte.<br>
**Obs! Skicka inte några hemligheter eller lösenord i egenskapen customData**<br>
Den här egenskapen kan inte uppdateras när den virtuella datorn har skapats. <br>
customData överförs till den virtuella maskinerna för att sparas som en fil. Mer information finns [i Anpassade data på Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) <br>
Mer information om hur du använder moln init för Linux VM finns i [Använda moln init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) för att anpassa en Linux VM när du skapar den

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -DisablePasswordAuthentication
Anger att denna cmdlet inaktiverar lösenordsautentisering.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Inaktivera provision VM Agent.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Anger att denna cmdlet aktiverar automatisk uppdatering.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Anger att operativsystemets typ är Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Anger läge för korrigering under gäst till den virtuella IaaS-datorn.<br><br>
Möjliga värden är:<br>
**Manuellt** – du styr programkorrigeringarna på en virtuell dator. Det gör du genom att använda korrigeringar manuellt i den virtuella datorn. I det här läget inaktiveras automatiska uppdateringar. egenskapen WindowsConfiguration.enableAutomaticUpdates måste vara falskt<br>
**AutomaticByOS** – Den virtuella datorn uppdateras automatiskt av operativsystemet. Egenskapen WindowsConfiguration.enableAutomaticUpdates måste vara sann. <br >
**AutomaticByPlatform** – den virtuella datorn uppdateras automatiskt av operativsystemet. Properties provisionVMAgent och WindowsConfiguration.enableAutomaticUpdates måste uppfyllas

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Anger att inställningarna kräver att den virtuella datoragenten installeras på den virtuella datorn.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Anger tidszonen för den virtuella datorn. t.ex. \" Pacific Standard \" Time. <br>
Möjliga värden kan [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) tidszoner som returneras av [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det lokala virtuella datorobjektet för vilket du anger egenskaper för operativsystemet.
Om du vill hämta ett virtuellt datorobjekt använder du Get-AzVM-cmdleten.
Skapa ett virtuellt maskinobjekt med hjälp New-AzVMConfig cmdlet.

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

### -Windows
Anger att typen av operativsystem är Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Anger URI för ett WinRM-certifikat.
Det här måste lagras i ett nyckelvalv.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Anger att detta operativsystem använder HTTP WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Anger att detta operativsystem använder HTTPS WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


