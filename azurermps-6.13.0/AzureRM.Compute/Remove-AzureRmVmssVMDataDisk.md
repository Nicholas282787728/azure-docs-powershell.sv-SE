---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: 5c82c2dfb852cd6c3d397b34e90d9a611ff0efaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585056"
---
# Remove-AzureRmVmssVMDataDisk

## Sammanfattning
Tar bort en datadisk från en virtuell dator skala ange virtuell dator

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmVmssVMDataDisk** tar bort en datadisk från en virtuell dators SKALNINGs dator

## BESKRIVS

### Exempel 1: ta bort en datadisk från en virtuell dator skala ange virtuell dator
```powershell
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzureRmVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Det första kommandot getsan befintliga VMSS VM som anges av resurs gruppens namn, VMSS namn och instans-ID.
Med det andra kommandot tas data disken LUN 0 bort från den virtuella datorns skal uppsättning den virtuella dator som lagras i $VmssVM det sista kommandot uppdaterar den VMSS virtuella dator med borttagen data disk.

## MALLPARAMETRAR

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

### -LUN
Anger diskens logiska enhets nummer.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
Den virtuella datorns skalning ange VM-profilen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
