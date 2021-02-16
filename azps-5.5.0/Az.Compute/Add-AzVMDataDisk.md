---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233438"
---
# Add-AzVMDataDisk

## SYNOPSIS
Lägger till en datadisk till en virtuell dator.

## SYNTAX

### VmNormalDiskParameterSetName (standard)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzVMDataDisk** lägger till en datadisk på en virtuell dator.
Du kan lägga till en datadisk när du skapar en virtuell dator, eller så kan du lägga till en datadisk till en befintlig virtuell dator.

## EXEMPEL

### Exempel 1: Lägga till datadiskar i en ny virtuell dator
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Det första kommandot skapar ett virtuellt maskinobjekt och lagrar det sedan i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Följande tre kommandon tilldelar sökvägar för tre datadiskar till variablerna $DataDiskVhdUri 01, $DataDiskVhdUri 02 och $DataDiskVhdUri 03.
Den här metoden är endast läsbar för följande kommandon.
De sista tre kommandona lägger var och en till en datadisk på den virtuella datorn som lagras $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.
URI:en för varje disk lagras i $DataDiskVhdUri 01, $DataDiskVhdUri 02 och $DataDiskVhdUri 03.

### Exempel 2: Lägga till en dataskiva till en befintlig virtuell dator
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Det första kommandot hämtar den virtuella datorn med namnet VirtualMa machinee07 med cmdleten [Get-AzVM.](./Get-AzVM.md)
Kommandot lagrar den virtuella datorn i $VirtualMachine variabeln.
Det andra kommandot lägger till en dataskiva på den virtuella datorn som lagras $VirtualMachine.
Det slutliga kommandot uppdaterar statusen för den virtuella datorn som lagras $VirtualMachine i ResourceGroup11.

### Exempel 3: Lägga till en dataskiva till en ny virtuell dator från en allmän användarbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Det första kommandot skapar ett virtuellt maskinobjekt och lagrar det i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
De följande två kommandona tilldelar sökvägar för databilden och datadiskarna till de $DataImageUri respektive $DataDiskUri variablerna.
Den här metoden används för att göra följande kommandon läsbarhet.
De slutliga kommandona lägger till en dataskiva till den virtuella datorn som lagras i $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.

### Exempel 4: Lägga till datadiskar till en ny virtuell dator från en särskild användarbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Det första kommandot skapar ett virtuellt maskinobjekt och lagrar det i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Med följande kommandon tilldelas sökvägar för datadisken till den $DataDiskUri variabeln.
Den här metoden används för att göra följande kommandon läsbarhet.
Det slutliga kommandot lägger till en dataskiva till den virtuella datorn som lagras $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.

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
Position: 3
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
Position: 6
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
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Anger det logiska enhetsnumret (LUN) för en datadisk.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Anger ID för en hanterad disk.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på den dataskiva som ska läggas till.

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

### -SourceImageUri
Anger käll-URI:n för den disk som denna cmdlet bifogar.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Anger lagringskontotyp för hanterad disk.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Anger URI (Uniform Resource Identifier) för den virtuella hårddiskfilen (VHD) som ska skapas när en plattformsbild eller användarbild används.
Den här cmdleten kopierar det binära stora objektet (blob) till den här platsen.
Det här är den plats där du vill starta den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det lokala virtuella datorobjektet som du vill lägga till en datadisk i.
Du kan använda **cmdleten Get-AzVM** till att hämta ett virtuellt datorobjekt.
Du kan använda cmdleten **New-AzVMConfig** till att skapa ett virtuellt datorobjekt.

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

### -WriteAccelerator
Anger om WriteAccelerator ska aktiveras eller inaktiveras på en hanterad datadisk.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
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

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
