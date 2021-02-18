---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100254013"
---
# Get-AzVmssVM

## SYNOPSIS
Hämtar egenskaperna för en virtuell VMSS-dator.

## SYNTAX

### DefaultParameter (standard)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzVmssVM** hämtar modellvyn och instansvyn för en virtuell maskinskaleuppsättning (VMSS).
Modellvyn är de användaregenskaper som angetts för den virtuella datorn.
Instansvyn är den virtuella datorns instansnivåstatus.
Ange *statusparametern* för att endast hämta instansvyn för en virtuell dator.

## EXEMPEL

### Exempel 1: Hämta egenskaperna för en virtuell VMSS-dator
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Det här kommandot hämtar egenskaperna för den virtuella VMSS-datorn med namnet VMSS001 som tillhör resursgruppen med namnet Group001.
Eftersom kommandot inte anger växelparametern *InstanceView* får cmdleten modellvyn för den virtuella datorn.

### Exempel 2: Hämta modellvyegenskaperna för en virtuell VMSS-dator
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Det här kommandot hämtar egenskaperna för den virtuella VMSS-datorn med namnet VMSS004 som tillhör resursgruppen med namnet Group002.
Med kommandot får du instans-ID:t lagrat i $ID som du vill hämta modellvyn för.

### Exempel 3: Hämta instansvyns egenskaper för en virtuell VMSS-dator
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Det här kommandot hämtar egenskaperna för den virtuella VMSS-datorn med namnet VMSS004 som tillhör resursgruppen med namnet Group002.
Eftersom kommandot anger parametern *InstanceView-växel,* hämtar cmdleten instansvyn för den virtuella datorn.
Kommandot hämtar instans-ID:t som lagras i $ID som instansvyn ska visas för.

## PARAMETERS

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

### -InstanceId
Anger det instans-ID som modellvyn ska hämtas för.

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

### -InstanceView
Anger att denna cmdlet endast hämtar instansvyn för den virtuella datorn.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen för VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Arter namnet på VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


