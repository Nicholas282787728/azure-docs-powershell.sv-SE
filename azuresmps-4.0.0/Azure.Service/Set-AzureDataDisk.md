---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099296"
---
# <span data-ttu-id="fed0b-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fed0b-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="fed0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fed0b-102">SYNOPSIS</span></span>
<span data-ttu-id="fed0b-103">Ändrar Host caching för en befintlig data disk på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="fed0b-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="fed0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fed0b-104">SYNTAX</span></span>

### <span data-ttu-id="fed0b-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="fed0b-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fed0b-106">Ändra storlek på</span><span class="sxs-lookup"><span data-stu-id="fed0b-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fed0b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fed0b-107">DESCRIPTION</span></span>
<span data-ttu-id="fed0b-108">Cmdleten **set-AzureDataDisk** ändrar cache-attributen för en befintlig datadisk på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="fed0b-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="fed0b-109">Ange vilken datadisk som ska uppdateras med LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="fed0b-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="fed0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fed0b-110">EXAMPLES</span></span>

### <span data-ttu-id="fed0b-111">Exempel 1: ändra Host caching för en data disk</span><span class="sxs-lookup"><span data-stu-id="fed0b-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="fed0b-112">Det här kommandot får de virtuella datorerna som körs på tjänsten som heter ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fed0b-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="fed0b-113">Kommandot skickar dem till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="fed0b-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fed0b-114">Denna cmdlet ställer in data disken på LUN 2 på den virtuella datorn med namnet VirtualMachine07 för att använda ReadOnly-cachelagring för värdar.</span><span class="sxs-lookup"><span data-stu-id="fed0b-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="fed0b-115">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar med hjälp av cmdleten **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fed0b-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="fed0b-116">Exempel 2: ändra caching för alla data diskar på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fed0b-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="fed0b-117">Det här kommandot får ett objekt för den virtuella datorn som heter VirtualMachine07 på ContosoService-moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fed0b-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="fed0b-118">Kommandot skickar det till cmdleten **Get-AzureDataDisk** , som hämtar data diskarna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fed0b-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="fed0b-119">Den aktuella cmdleten ställer in läget för cachelagring av Host för varje data disk mot ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fed0b-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="fed0b-120">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="fed0b-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="fed0b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fed0b-121">PARAMETERS</span></span>

### <span data-ttu-id="fed0b-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="fed0b-122">-DiskName</span></span>
<span data-ttu-id="fed0b-123">Anger namnet på den data disk konfiguration som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="fed0b-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed0b-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="fed0b-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="fed0b-125">Diskcachelagring stöds inte för diskar 4 TiB och senare.</span><span class="sxs-lookup"><span data-stu-id="fed0b-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="fed0b-126">Om flera diskar är anslutna till din virtuella dator stöder alla diskar som är mindre än 4 TiB cachelagring.</span><span class="sxs-lookup"><span data-stu-id="fed0b-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="fed0b-127">Ändring av cache-inställningen för en Azure-disk kopplas från och kopplas till mål disketten.</span><span class="sxs-lookup"><span data-stu-id="fed0b-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="fed0b-128">Om det är operativ systemets disk startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="fed0b-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="fed0b-129">Stoppa alla program/tjänster som påverkas av detta avbrott innan du ändrar inställningen för diskcachen.</span><span class="sxs-lookup"><span data-stu-id="fed0b-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="fed0b-130">Dessa rekommendationer kan leda till skadade data.</span><span class="sxs-lookup"><span data-stu-id="fed0b-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="fed0b-131">Anger diskens cacheinställningar på nivån.</span><span class="sxs-lookup"><span data-stu-id="fed0b-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="fed0b-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="fed0b-132">Valid values are:</span></span>

- <span data-ttu-id="fed0b-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="fed0b-133">None</span></span>
- <span data-ttu-id="fed0b-134">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fed0b-134">ReadOnly</span></span>
- <span data-ttu-id="fed0b-135">Läs</span><span class="sxs-lookup"><span data-stu-id="fed0b-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed0b-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fed0b-136">-InformationAction</span></span>
<span data-ttu-id="fed0b-137">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fed0b-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fed0b-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fed0b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fed0b-139">Vidare</span><span class="sxs-lookup"><span data-stu-id="fed0b-139">Continue</span></span>
- <span data-ttu-id="fed0b-140">Över</span><span class="sxs-lookup"><span data-stu-id="fed0b-140">Ignore</span></span>
- <span data-ttu-id="fed0b-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="fed0b-141">Inquire</span></span>
- <span data-ttu-id="fed0b-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fed0b-142">SilentlyContinue</span></span>
- <span data-ttu-id="fed0b-143">Stanna</span><span class="sxs-lookup"><span data-stu-id="fed0b-143">Stop</span></span>
- <span data-ttu-id="fed0b-144">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fed0b-144">Suspend</span></span>

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

### <span data-ttu-id="fed0b-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fed0b-145">-InformationVariable</span></span>
<span data-ttu-id="fed0b-146">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fed0b-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fed0b-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="fed0b-147">-LUN</span></span>
<span data-ttu-id="fed0b-148">Anger LUN för data enheten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fed0b-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="fed0b-149">Giltiga värden är: 0 till 15.</span><span class="sxs-lookup"><span data-stu-id="fed0b-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed0b-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="fed0b-150">-Profile</span></span>
<span data-ttu-id="fed0b-151">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fed0b-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fed0b-152">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fed0b-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fed0b-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fed0b-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="fed0b-154">Anger den nya storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="fed0b-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="fed0b-155">Den nya storleken måste vara större än den aktuella storleken.</span><span class="sxs-lookup"><span data-stu-id="fed0b-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed0b-156">-VM</span><span class="sxs-lookup"><span data-stu-id="fed0b-156">-VM</span></span>
<span data-ttu-id="fed0b-157">Anger det virtuella dator objekt som är kopplat till data disken.</span><span class="sxs-lookup"><span data-stu-id="fed0b-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="fed0b-158">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="fed0b-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="fed0b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed0b-159">CommonParameters</span></span>
<span data-ttu-id="fed0b-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed0b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed0b-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed0b-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed0b-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fed0b-162">INPUTS</span></span>

## <span data-ttu-id="fed0b-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fed0b-163">OUTPUTS</span></span>

## <span data-ttu-id="fed0b-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fed0b-164">NOTES</span></span>

## <span data-ttu-id="fed0b-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fed0b-165">RELATED LINKS</span></span>

[<span data-ttu-id="fed0b-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fed0b-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="fed0b-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fed0b-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fed0b-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fed0b-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="fed0b-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fed0b-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="fed0b-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fed0b-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


