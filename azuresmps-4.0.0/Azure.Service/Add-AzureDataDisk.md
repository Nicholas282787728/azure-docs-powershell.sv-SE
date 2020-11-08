---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093461"
---
# <span data-ttu-id="5e111-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e111-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="5e111-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e111-102">SYNOPSIS</span></span>
<span data-ttu-id="5e111-103">Lägger till en datadisk till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5e111-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="5e111-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e111-104">SYNTAX</span></span>

### <span data-ttu-id="5e111-105">CreateNew (standard)</span><span class="sxs-lookup"><span data-stu-id="5e111-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e111-106">Importeras</span><span class="sxs-lookup"><span data-stu-id="5e111-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e111-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="5e111-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e111-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e111-108">DESCRIPTION</span></span>
<span data-ttu-id="5e111-109">Cmdleten **Add-AzureDataDisk** lägger till en ny eller befintlig datadisk till ett objekt i Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="5e111-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="5e111-110">Använd parametern *createnew* för att skapa en ny data skiva med angiven storlek och etikett.</span><span class="sxs-lookup"><span data-stu-id="5e111-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="5e111-111">Använd *import* parametern för att bifoga en befintlig disk från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="5e111-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="5e111-112">Använd parametern *ImportFrom* för att bifoga en befintlig disk från en BLOB i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5e111-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="5e111-113">Du kan ange värd-cache-läget för den anslutna data disken.</span><span class="sxs-lookup"><span data-stu-id="5e111-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="5e111-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e111-114">EXAMPLES</span></span>

### <span data-ttu-id="5e111-115">Exempel 1: importera en data disk från databasen</span><span class="sxs-lookup"><span data-stu-id="5e111-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="5e111-116">Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet VirtualMachine07 i ContosoService-moln tjänsten genom att använda cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e111-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="5e111-117">Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="5e111-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e111-118">Det kommandot kopplar en befintlig datadisk från databasen till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5e111-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="5e111-119">Data disken har en LUN på 0.</span><span class="sxs-lookup"><span data-stu-id="5e111-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="5e111-120">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar med hjälp av cmdleten **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e111-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="5e111-121">Exempel 2: lägga till en ny data skiva</span><span class="sxs-lookup"><span data-stu-id="5e111-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="5e111-122">Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="5e111-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="5e111-123">Kommandot skickar det till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e111-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="5e111-124">Kommandot bifogar en ny data skiva med namnet MyNewDisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="5e111-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="5e111-125">Cmdleten skapar disken i behållaren VHD: er i det vanliga lagrings kontot för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5e111-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="5e111-126">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="5e111-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="5e111-127">Exempel 3: lägga till en datadisk från en angiven plats</span><span class="sxs-lookup"><span data-stu-id="5e111-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="5e111-128">Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet Database.</span><span class="sxs-lookup"><span data-stu-id="5e111-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="5e111-129">Kommandot skickar det till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e111-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="5e111-130">Kommandot kopplar en befintlig datadisk med namnet Disk14. VHD från den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="5e111-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="5e111-131">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="5e111-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="5e111-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e111-132">PARAMETERS</span></span>

### <span data-ttu-id="5e111-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="5e111-133">-CreateNew</span></span>
<span data-ttu-id="5e111-134">Anger att denna cmdlet skapar en data disk.</span><span class="sxs-lookup"><span data-stu-id="5e111-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="5e111-135">-DiskLabel</span></span>
<span data-ttu-id="5e111-136">Anger disk etiketten för en ny data disk.</span><span class="sxs-lookup"><span data-stu-id="5e111-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="5e111-137">-DiskName</span></span>
<span data-ttu-id="5e111-138">Anger namnet på en data disk i disk lagringen.</span><span class="sxs-lookup"><span data-stu-id="5e111-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5e111-139">-DiskSizeInGB</span></span>
<span data-ttu-id="5e111-140">Anger storleken på logiska diskar för en ny data disk i GB.</span><span class="sxs-lookup"><span data-stu-id="5e111-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="5e111-141">-HostCaching</span></span>
<span data-ttu-id="5e111-142">Anger diskens cacheinställningar på nivån.</span><span class="sxs-lookup"><span data-stu-id="5e111-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="5e111-143">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="5e111-143">Valid values are:</span></span> 

- <span data-ttu-id="5e111-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="5e111-144">None</span></span> 
- <span data-ttu-id="5e111-145">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="5e111-145">ReadOnly</span></span> 
- <span data-ttu-id="5e111-146">Läs</span><span class="sxs-lookup"><span data-stu-id="5e111-146">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-147">-Importera</span><span class="sxs-lookup"><span data-stu-id="5e111-147">-Import</span></span>
<span data-ttu-id="5e111-148">Anger att denna cmdlet importerar en befintlig data disk från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="5e111-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="5e111-149">-ImportFrom</span></span>
<span data-ttu-id="5e111-150">Anger att denna cmdlet importerar en befintlig data disk från en blob till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5e111-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5e111-151">-InformationAction</span></span>
<span data-ttu-id="5e111-152">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="5e111-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e111-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5e111-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e111-154">Vidare</span><span class="sxs-lookup"><span data-stu-id="5e111-154">Continue</span></span>
- <span data-ttu-id="5e111-155">Över</span><span class="sxs-lookup"><span data-stu-id="5e111-155">Ignore</span></span>
- <span data-ttu-id="5e111-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="5e111-156">Inquire</span></span>
- <span data-ttu-id="5e111-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5e111-157">SilentlyContinue</span></span>
- <span data-ttu-id="5e111-158">Stanna</span><span class="sxs-lookup"><span data-stu-id="5e111-158">Stop</span></span>
- <span data-ttu-id="5e111-159">Avbryt</span><span class="sxs-lookup"><span data-stu-id="5e111-159">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5e111-160">-InformationVariable</span></span>
<span data-ttu-id="5e111-161">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="5e111-161">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="5e111-162">-LUN</span></span>
<span data-ttu-id="5e111-163">Anger LUN (Logical Unit Number) för data enheten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5e111-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="5e111-164">Giltiga värden är: 0 till 15.</span><span class="sxs-lookup"><span data-stu-id="5e111-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="5e111-165">Varje data disk måste ha ett unikt LUN.</span><span class="sxs-lookup"><span data-stu-id="5e111-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="5e111-166">-MediaLocation</span></span>
<span data-ttu-id="5e111-167">Anger platsen för blobben i ett Azure Storage-konto där denna cmdlet lagrar data disken.</span><span class="sxs-lookup"><span data-stu-id="5e111-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="5e111-168">Om du inte anger en plats lagras data disken i behållaren VHD: er i standard lagrings kontot för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5e111-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="5e111-169">Om det inte finns en behållare för virtuella hård diskar skapas en behållare för virtuella hård diskar.</span><span class="sxs-lookup"><span data-stu-id="5e111-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-170">-Profil</span><span class="sxs-lookup"><span data-stu-id="5e111-170">-Profile</span></span>
<span data-ttu-id="5e111-171">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5e111-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e111-172">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5e111-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-173">-VM</span><span class="sxs-lookup"><span data-stu-id="5e111-173">-VM</span></span>
<span data-ttu-id="5e111-174">Anger det virtuella dator objekt som denna cmdlet ansluter en data disk till.</span><span class="sxs-lookup"><span data-stu-id="5e111-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="5e111-175">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="5e111-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e111-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e111-176">CommonParameters</span></span>
<span data-ttu-id="5e111-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e111-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e111-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e111-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e111-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e111-179">INPUTS</span></span>

## <span data-ttu-id="5e111-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e111-180">OUTPUTS</span></span>

## <span data-ttu-id="5e111-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e111-181">NOTES</span></span>

## <span data-ttu-id="5e111-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e111-182">RELATED LINKS</span></span>

[<span data-ttu-id="5e111-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e111-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="5e111-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5e111-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="5e111-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e111-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="5e111-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e111-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="5e111-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5e111-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


