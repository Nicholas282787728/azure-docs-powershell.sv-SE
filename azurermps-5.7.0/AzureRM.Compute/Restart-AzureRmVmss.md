---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584420"
---
# <span data-ttu-id="a933d-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="a933d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a933d-102">SYNOPSIS</span></span>
<span data-ttu-id="a933d-103">Startar om VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="a933d-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a933d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a933d-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a933d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a933d-105">DESCRIPTION</span></span>
<span data-ttu-id="a933d-106">Cmdleten **restart-AzureRmVmss** startar om den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a933d-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a933d-107">Denna cmdlet kan också användas för att starta om en specifik virtuell dator i VMSS med hjälp av *InstanceID* -parametern.</span><span class="sxs-lookup"><span data-stu-id="a933d-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="a933d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a933d-108">EXAMPLES</span></span>

### <span data-ttu-id="a933d-109">Exempel 1: starta om VMSS</span><span class="sxs-lookup"><span data-stu-id="a933d-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="a933d-110">Det här kommandot startar om VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="a933d-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="a933d-111">Exempel 2: starta om en specifik virtuell dator inom VMSS</span><span class="sxs-lookup"><span data-stu-id="a933d-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="a933d-112">Det här kommandot startar om en virtuell dator som har instans-ID 1 i VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="a933d-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a933d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a933d-113">PARAMETERS</span></span>

### <span data-ttu-id="a933d-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a933d-114">-InstanceId</span></span>
<span data-ttu-id="a933d-115">Anger ID för de instanser som behöver startas om.</span><span class="sxs-lookup"><span data-stu-id="a933d-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a933d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a933d-116">-ResourceGroupName</span></span>
<span data-ttu-id="a933d-117">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="a933d-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a933d-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a933d-118">-VMScaleSetName</span></span>
<span data-ttu-id="a933d-119">Arter namnet på den VMSS som denna cmdlet startar om.</span><span class="sxs-lookup"><span data-stu-id="a933d-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="a933d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a933d-120">-Confirm</span></span>
<span data-ttu-id="a933d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a933d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a933d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a933d-122">-WhatIf</span></span>
<span data-ttu-id="a933d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a933d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a933d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a933d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a933d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a933d-125">CommonParameters</span></span>
<span data-ttu-id="a933d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a933d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a933d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a933d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a933d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a933d-128">INPUTS</span></span>

### <span data-ttu-id="a933d-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="a933d-129">None</span></span>
<span data-ttu-id="a933d-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a933d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a933d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a933d-131">OUTPUTS</span></span>

###  
<span data-ttu-id="a933d-132">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a933d-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a933d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a933d-133">NOTES</span></span>

## <span data-ttu-id="a933d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a933d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a933d-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a933d-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a933d-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a933d-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a933d-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a933d-140">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a933d-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a933d-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


