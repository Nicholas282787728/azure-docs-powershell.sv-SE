---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099396"
---
# <span data-ttu-id="71f5f-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="71f5f-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="71f5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="71f5f-103">Tar bort en datadisk från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="71f5f-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="71f5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71f5f-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="71f5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="71f5f-106">Cmdleten **Remove-AzureDataDisk** tar bort en datadisk från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="71f5f-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="71f5f-107">Denna cmdlet tar som standard inte bort data diskens BLOB från lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="71f5f-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="71f5f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71f5f-108">EXAMPLES</span></span>

### <span data-ttu-id="71f5f-109">Exempel 1: ta bort en data disk</span><span class="sxs-lookup"><span data-stu-id="71f5f-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="71f5f-110">Det här kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="71f5f-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="71f5f-111">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="71f5f-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71f5f-112">Den aktuella cmdleten tar bort den datadisk som innehåller LUN 0.</span><span class="sxs-lookup"><span data-stu-id="71f5f-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="71f5f-113">Exempel 2: ta bort en data disk och den virtuella hård disk filen</span><span class="sxs-lookup"><span data-stu-id="71f5f-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="71f5f-114">Det här kommandot får den virtuella datorn med namnet VirtualMachine07 i tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="71f5f-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="71f5f-115">Kommandot skickar den virtuella datorn till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71f5f-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="71f5f-116">Den aktuella cmdleten tar bort den datadisk som innehåller LUN 0.</span><span class="sxs-lookup"><span data-stu-id="71f5f-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="71f5f-117">Kommandot innehåller parametern *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="71f5f-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="71f5f-118">Därför tas den underliggande virtuella hård disken också bort.</span><span class="sxs-lookup"><span data-stu-id="71f5f-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="71f5f-119">Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar med hjälp av cmdleten **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="71f5f-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="71f5f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71f5f-120">PARAMETERS</span></span>

### <span data-ttu-id="71f5f-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="71f5f-121">-DeleteVHD</span></span>
<span data-ttu-id="71f5f-122">Anger att denna cmdlet tar bort data disken och den virtuella hård disken (VHD) från Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="71f5f-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71f5f-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71f5f-123">-InformationAction</span></span>
<span data-ttu-id="71f5f-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="71f5f-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71f5f-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71f5f-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71f5f-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="71f5f-126">Continue</span></span>
- <span data-ttu-id="71f5f-127">Över</span><span class="sxs-lookup"><span data-stu-id="71f5f-127">Ignore</span></span>
- <span data-ttu-id="71f5f-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="71f5f-128">Inquire</span></span>
- <span data-ttu-id="71f5f-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71f5f-129">SilentlyContinue</span></span>
- <span data-ttu-id="71f5f-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="71f5f-130">Stop</span></span>
- <span data-ttu-id="71f5f-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="71f5f-131">Suspend</span></span>

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

### <span data-ttu-id="71f5f-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71f5f-132">-InformationVariable</span></span>
<span data-ttu-id="71f5f-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="71f5f-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71f5f-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="71f5f-134">-LUN</span></span>
<span data-ttu-id="71f5f-135">Anger LUN (Logical Unit Number) för data enheten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="71f5f-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="71f5f-136">Giltiga värden är: 0 till 15.</span><span class="sxs-lookup"><span data-stu-id="71f5f-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71f5f-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="71f5f-137">-Profile</span></span>
<span data-ttu-id="71f5f-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="71f5f-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71f5f-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="71f5f-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71f5f-140">-VM</span><span class="sxs-lookup"><span data-stu-id="71f5f-140">-VM</span></span>
<span data-ttu-id="71f5f-141">Anger det virtuella dator objekt som är kopplat till data disken.</span><span class="sxs-lookup"><span data-stu-id="71f5f-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="71f5f-142">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="71f5f-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="71f5f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f5f-143">CommonParameters</span></span>
<span data-ttu-id="71f5f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f5f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f5f-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f5f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f5f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71f5f-146">INPUTS</span></span>

## <span data-ttu-id="71f5f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71f5f-147">OUTPUTS</span></span>

## <span data-ttu-id="71f5f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71f5f-148">NOTES</span></span>

## <span data-ttu-id="71f5f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71f5f-149">RELATED LINKS</span></span>

[<span data-ttu-id="71f5f-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="71f5f-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="71f5f-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="71f5f-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="71f5f-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="71f5f-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="71f5f-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="71f5f-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="71f5f-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="71f5f-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


