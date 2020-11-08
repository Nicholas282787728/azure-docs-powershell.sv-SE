---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093242"
---
# <span data-ttu-id="e4c0f-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-101">Remove-AzureVM</span></span>

## <span data-ttu-id="e4c0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c0f-103">Tar bort en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="e4c0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4c0f-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4c0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c0f-106">Cmdleten **Remove-AzureVM** tar bort en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="e4c0f-107">Den här processen tar inte bort underliggande VHD-filer för de diskar som är monterade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="e4c0f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4c0f-108">EXAMPLES</span></span>

### <span data-ttu-id="e4c0f-109">Exempel 1: ta bort en virtuell dator från en tjänst</span><span class="sxs-lookup"><span data-stu-id="e4c0f-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="e4c0f-110">Det här kommandot tar bort den virtuella datorn med namnet VirtualMachine03 som körs i ContosoService03-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="e4c0f-111">Exempel 2: ta bort en virtuell dator och ta bort VHD-filerna</span><span class="sxs-lookup"><span data-stu-id="e4c0f-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="e4c0f-112">Det här kommandot tar bort den virtuella VirtualMachine04-datorn som körs i ContosoService03-tjänsten och anger att VHD-filerna ska tas bort med parametern *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="e4c0f-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="e4c0f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4c0f-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c0f-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="e4c0f-114">-DeleteVHD</span></span>
<span data-ttu-id="e4c0f-115">Anger om den här cmdleten tar bort den virtuella datorn och underliggande disk-blob.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c0f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e4c0f-116">-InformationAction</span></span>
<span data-ttu-id="e4c0f-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e4c0f-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e4c0f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4c0f-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="e4c0f-119">Continue</span></span>
- <span data-ttu-id="e4c0f-120">Över</span><span class="sxs-lookup"><span data-stu-id="e4c0f-120">Ignore</span></span>
- <span data-ttu-id="e4c0f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="e4c0f-121">Inquire</span></span>
- <span data-ttu-id="e4c0f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e4c0f-122">SilentlyContinue</span></span>
- <span data-ttu-id="e4c0f-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="e4c0f-123">Stop</span></span>
- <span data-ttu-id="e4c0f-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e4c0f-124">Suspend</span></span>

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

### <span data-ttu-id="e4c0f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e4c0f-125">-InformationVariable</span></span>
<span data-ttu-id="e4c0f-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e4c0f-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4c0f-127">-Name</span></span>
<span data-ttu-id="e4c0f-128">Anger namnet på den virtuella dator som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-128">Specifies the name of the virtual machine being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c0f-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="e4c0f-129">-Profile</span></span>
<span data-ttu-id="e4c0f-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4c0f-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4c0f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4c0f-132">-ServiceName</span></span>
<span data-ttu-id="e4c0f-133">Anger namnet på den Azure-tjänst som den virtuella datorn tas bort från.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c0f-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4c0f-134">-Confirm</span></span>
<span data-ttu-id="e4c0f-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c0f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c0f-136">-WhatIf</span></span>
<span data-ttu-id="e4c0f-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c0f-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c0f-139">CommonParameters</span></span>
<span data-ttu-id="e4c0f-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c0f-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4c0f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c0f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4c0f-142">INPUTS</span></span>

## <span data-ttu-id="e4c0f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4c0f-143">OUTPUTS</span></span>

## <span data-ttu-id="e4c0f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4c0f-144">NOTES</span></span>

## <span data-ttu-id="e4c0f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4c0f-145">RELATED LINKS</span></span>

[<span data-ttu-id="e4c0f-146">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="e4c0f-147">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="e4c0f-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="e4c0f-148">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="e4c0f-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="e4c0f-150">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="e4c0f-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e4c0f-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


