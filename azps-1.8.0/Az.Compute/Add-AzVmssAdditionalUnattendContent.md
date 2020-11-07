---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 92bf4afc1933a95e582ee028780e002ea5ac8252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754606"
---
# Add-AzVmssAdditionalUnattendContent

## Sammanfattning
Lägger till information i svars filen för obevakad Windows-installation.

## FRÅGESYNTAXEN

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzVmssAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.

## BESKRIVS

### Exempel 1: lägga till information i svars filen för obevakad Windows-installation
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

Det här kommandot lägger till information i svars filen för obevakad Windows-installation.

## MALLPARAMETRAR

### -ComponentName
Anger namnet på den komponent som ska konfigureras med det tillagda innehållet.
Det enda tillåtna värdet är Microsoft-Windows-Shell-Setup.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Innehåll
Anger det XML-formaterade innehåll som läggs till i unattend.xml filen för den angivna sökvägen och komponenten.

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
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -PassName
Anger namnet på det pass som innehållet gäller för.
Det enda tillåtna värdet är oobeSystem.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SettingName
Anger namnet på den inställning som innehållet gäller för.
De acceptabla värdena för den här parametern är::
- FirstLogonCommands
- Automatisk inloggning

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Ange den virtuella datorns **skal uppsättnings** objekt.
Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. PassNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ComponentNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzVmssConfig](./New-AzVmssConfig.md)
