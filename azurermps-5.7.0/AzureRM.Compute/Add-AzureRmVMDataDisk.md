---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575723"
---
# Add-AzureRmVMDataDisk

## Sammanfattning
Lägger till en datadisk till en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVMDataDisk** lägger till en datadisk till en virtuell dator.
Du kan lägga till en datadisk när du skapar en virtuell dator eller lägga till en data disk till en befintlig virtuell dator.

## BESKRIVS

### Exempel 1: lägga till data diskar på en ny virtuell dator
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.

Nästa tre kommandon tilldelar sökvägar till tre data diskar till $DataDiskVhdUri 01-$DataDiskVhdUri 02-och $DataDiskVhdUri 03-variabler.
Den här metoden är endast för läsbarhet av följande kommandon.

De tre sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.
URI: n för varje disk lagras i $DataDiskVhdUri 01 $DataDiskVhdUri 02 och $DataDiskVhdUri 03.

### Exempel 2: lägga till en datadisk till en befintlig virtuell dator
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) .
Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.

Det andra kommandot lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.

Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.

### Exempel 3: lägga till en datadisk till en ny virtuell dator från en generaliserad användar bild
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.

Nästa två kommandon tilldelar sökvägar för data-och data diskarna till $DataImageUri och $DataDiskUri variabler.
Den här metoden används för att förbättra läsbarheten för följande kommandon.

De sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.

### Exempel 4: lägga till data diskar till en ny virtuell dator från en specialiserad användar bild
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.

Med nästa kommando kopplas sökvägar till den $DataDiskUri variabeln.
Den här metoden används för att förbättra läsbarheten för följande kommandon.

Med kommandot sista lägger du till en datadisk till den virtuella datorn som lagras i $VirtualMachine.
Kommandot anger namn och plats för disken och andra egenskaper för disken.

## MALLPARAMETRAR

### -Cachning
Anger diskens cacheläge.
De acceptabla värdena för den här parametern är:

- ReadOnly
- Läs
- Ingen

Standardvärdet är ReadWrite.
Om du ändrar det här värdet startas den virtuella datorn om.

Den här inställningen påverkar diskens konsekvens och prestanda.

```yaml
Type: CachingTypes
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
Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.
De acceptabla värdena för den här parametern är:

- Anteckning.
Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.
Ange inte parametern *SourceImageUri* när du anger det här alternativet.
*VhdUri* är allt som behövs för att det ska bli så att Azure Platform anger platsen för den virtuella hård disken (VHD) som ska kopplas till den virtuella datorn.
- Tomt.
Ange detta för att skapa en tom data disk.
- FromImage.
Ange det här alternativet om du vill skapa en virtuell dator från en allmän bild eller disk.
När du anger det här alternativet måste du ange parametern *SourceImageUri* även för att berätta för Azure Platform platsen för den virtuella hård disk som ska bifogas som en data skiva.
Parametern *VhdUri* används som den plats där data diskens VHD lagras när den används av den virtuella datorn.

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Anger storleken i GB på en tom disk som ska kopplas till en virtuell dator.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Anger LUN (Logical Unit Number) för en data disk.

```yaml
Type: Int32
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den datadisk som ska läggas till.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Anger källans URI för disken som cmdleten kopplas till.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Anger lagrings konto typen för hanterad disk.

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Anger URI (Uniform Resource Identifier) för den virtuella hård disk (VHD)-filen som ska skapas när en plattforms bild eller användar bild används.
Denna cmdlet kopierar det binära Large Object (BLOB) till den här platsen.
Det här är den plats där den virtuella datorn startas.

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

### -VM
Anger det lokala virtuella dator objekt där en data disk ska läggas till.
Du kan använda cmdleten **Get-AzureRmVM** för att hämta ett virtuellt dator objekt.
Du kan använda cmdleten **New-AzureRmVMConfig** för att skapa ett virtuellt dator objekt.

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

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmVMDataDisk](./Remove-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
