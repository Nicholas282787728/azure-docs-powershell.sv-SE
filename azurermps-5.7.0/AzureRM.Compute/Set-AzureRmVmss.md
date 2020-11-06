---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578280"
---
# <span data-ttu-id="0b3d7-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="0b3d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3d7-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b3d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b3d7-104">SYNTAX</span></span>

### <span data-ttu-id="0b3d7-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="0b3d7-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b3d7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0b3d7-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b3d7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b3d7-107">DESCRIPTION</span></span>
<span data-ttu-id="0b3d7-108">Cmdleten **set-AzureRmVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0b3d7-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0b3d7-109">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="0b3d7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b3d7-110">EXAMPLES</span></span>

### <span data-ttu-id="0b3d7-111">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="0b3d7-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="0b3d7-112">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="0b3d7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b3d7-113">PARAMETERS</span></span>

### <span data-ttu-id="0b3d7-114">-Ombild</span><span class="sxs-lookup"><span data-stu-id="0b3d7-114">-Reimage</span></span>
<span data-ttu-id="0b3d7-115">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3d7-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="0b3d7-116">-ReimageAll</span></span>
<span data-ttu-id="0b3d7-117">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b3d7-119">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0b3d7-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0b3d7-120">-VMScaleSetName</span></span>
<span data-ttu-id="0b3d7-121">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3d7-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b3d7-122">-Confirm</span></span>
<span data-ttu-id="0b3d7-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3d7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3d7-124">-WhatIf</span></span>
<span data-ttu-id="0b3d7-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b3d7-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3d7-127">CommonParameters</span></span>
<span data-ttu-id="0b3d7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3d7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3d7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3d7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b3d7-130">INPUTS</span></span>

### <span data-ttu-id="0b3d7-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="0b3d7-131">None</span></span>
<span data-ttu-id="0b3d7-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b3d7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b3d7-133">OUTPUTS</span></span>

### <span data-ttu-id="0b3d7-134">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0b3d7-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0b3d7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b3d7-135">NOTES</span></span>

## <span data-ttu-id="0b3d7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b3d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="0b3d7-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-138">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-140">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-142">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="0b3d7-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b3d7-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


