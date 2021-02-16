---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229159"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Lägger till en datadisk till en Vmss VM.

## SYNTAX

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Add-AzVmssVMDataDisk** lägger till en datadisk till en Vmss VM.

## EXEMPEL

### Exempel 1: Lägga till en hanterad datadisk i en Vmss VM.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Det första kommandot får en befintlig hanterad disk.
Nästa kommando får en befintlig Vmss VM givet av resursgruppnamnet, vmss-namnet och instans-ID.
Nästa kommando lägger till den hanterade hårddisken till vmss VM som lagras lokalt i $VmssVM.
Det slutliga kommandot uppdaterar Vmss VM med en tillagd datadisk.

## PARAMETERS

### -Cachelagring
Anger cachelagringsläge för disken.
De godtagbara värdena för den här parametern är:
- ReadOnly
- ReadWrite
- Inget standardvärdet är Skrivskydd.
Om du ändrar det här värdet startar den virtuella datorn om.
Den här inställningen påverkar konsekvensen och prestandan på disken.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Anger om den här cmdleten skapar en disk i den virtuella datorn från en plattform eller användarbild, skapar en tom disk eller bifogar en befintlig disk.
De godtagbara värdena för den här parametern är:
- Bifoga.
Ange det här alternativet om du vill skapa en virtuell dator från en särskild disk.
När du anger det här alternativet ska du inte ange *parametern SourceImageUri.*
*VhdUri* är allt som behövs för att kunna tala om för Azure-plattformen var den virtuella hårddisken (VHD) är att ansluta som en data disk till den virtuella datorn.
- Tom.
Ange detta för att skapa en tom dataskiva.
- FromImage.
Ange det här alternativet om du vill skapa en virtuell dator från en generaliserad bild eller disk.
När du anger det här alternativet måste du också ange *parametern SourceImageUri* för att kunna ange platsen för VHD på Azure-plattformen som ska bifogas som en datadisk.
Parametern *VhdUri* används som den plats där datadisken VHD lagras när den används av den virtuella datorn.

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

### -DiskEncryptionSetId
Anger resurs-ID för den kund hanterade diskkrypteringsuppsättningen.  Det här kan bara anges för hanterad disk.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Anger storleken i GB för en tom disk som ska anslutas till en virtuell dator.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Anger det logiska enhetsnumret (LUN) för en datadisk.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Anger ID för en hanterad disk.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Anger lagringskontotyp för hanterad disk.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
Anger den lokala virtuella datorskalauppsättningen FÖR VM-objekt som en datadisk ska läggas till för.
Du kan använda **cmdleten Get-AzVmssVM** till att hämta en virtuell datorskalauppsättning för VM-objekt.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Anger om WriteAccelerator ska aktiveras eller inaktiveras på en hanterad datadisk.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## ANTECKNINGAR

## RELATERADE LÄNKAR
