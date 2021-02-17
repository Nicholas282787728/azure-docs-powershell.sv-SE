---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238601"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Anger profilegenskaper för VMSS-operativsystemet.

## SYNTAX

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzVmssOsProfile** anger profilegenskaper för skalning för virtuell datorskala.

## EXEMPEL

### Exempel 1: Ange egenskaper för operativsystemets profil för ett VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Det här kommandot anger egenskaper för profilen i operativsystemet för de virtuella maskiner som tillhör VMSS som heter ContosoVMSS.
Kommandot anger datornamnsprefixet för alla instanser av den virtuella datorn i VMSS för att testa och tillhandahåller administratörsnamn och lösenord.

## PARAMETERS

### -AdditionalUnattendContent
Anger ett objekt för oövervakat innehåll.
Du kan använda Add-AzVMAdditionalUnattendContent för att skapa objektet.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Anger administratörslösenordet som ska användas för alla instanser av den virtuella datorn i VMSS.

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

### -AdminUsername
Anger det administratörskontonamn som ska användas för alla instanser av den virtuella datorn i VMSS. <br>
**Begränsning för endast Windows:** Det går inte att sluta \" med.\" <br>
**Värden som inte är till någon del:** \" \"administratör, \" \" administratör, \" \" användare, \" \" användare1, \" \" test, \" \" användare2, \" \" test1, \" \" användare3, \" \" administratör1, \" \" 1, \" 123, \" en , \" \" \" actuser, \" \" \" adm, \" \" admin2, \" \" aspnet, \" \" säkerhetskopiering, \" \" konsol, \" \" david, \" \" gäst, \" \" john, \" \" ägare, \" \" rot, \" \" \" \" server, sql, \" \" support, \" \" \" \" support_388945a0, sys, \" \" \" test2, \" test3, \" \" användare4, \" \" användare5. <br>
**Minsta längd (Linux):** 1 tecken <br>
**Maxlängd (Linux):** 64 tecken <br>
**Maxlängd (Windows):** 20 tecken  <br>
<li> För rotåtkomst till Linux VM, se [Använda rotbehörigheter på virtuella Linux-datorer i Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> En lista över inbyggda systemanvändare i Linux som inte ska användas i det här fältet finns i Välja användarnamn [för Linux i Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -ComputerNamePrefix
Anger datornamnsprefixet för alla instanser av den virtuella datorn i VMSS.
Datornamn måste innehålla 1 till 15 tecken.

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

### -CustomData
Anger en bas-64-kodad sträng med anpassade data.
Detta avkodas till en binär matris som sparas som en fil på den virtuella datorn.
Den maximala längden på den binära matrisen är 65 535 byte. <br>
Mer information om hur du använder moln init för den virtuella maskinerna finns i Använda moln init för att [anpassa en Linux VM när den skapas.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -LinuxConfigurationDisablePasswordAuthentication
Anger att denna cmdlet inaktiverar lösenordsautentisering.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lyssnaren
Anger Windows Remote Management-lyssnare(WinRM).
Detta aktiverar Windows PowerShell på distans.
Du kan använda cmdlet Add-AzVmssWinRMListener för att skapa lyssnaren.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Anger SSH-objektet (Secure Shell).
Du kan använda Add-AzVMSshPublicKey cmdleten för att skapa objektet.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hemligt
Anger det hemligt objekt som innehåller certifikatreferenserna som ska plats på den virtuella datorn.
Du kan använda cmdleten Add-AzVmssSecret för att skapa hemliga objektet.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Anger tidszonen för den virtuella datorn. t.ex. \" Pacific Standard \" Time. <br>
Möjliga värden kan [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) tidszoner som returneras av [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger VMSS-objektet.
Du kan använda New-AzVmssConfig cmdleten för att skapa objektet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Anger om virtuella datorer i VMSS har aktiverats för automatiska uppdateringar.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Anger om agenten för den virtuella datorn ska tillhandahållas på virtuella datorer i VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


