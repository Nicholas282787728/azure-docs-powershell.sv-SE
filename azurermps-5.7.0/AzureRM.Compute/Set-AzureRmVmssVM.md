---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578264"
---
# <span data-ttu-id="2bbca-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="2bbca-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="2bbca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bbca-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbca-103">Ändrar tillstånd för en VMSS-instans.</span><span class="sxs-lookup"><span data-stu-id="2bbca-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bbca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bbca-104">SYNTAX</span></span>

### <span data-ttu-id="2bbca-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="2bbca-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bbca-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2bbca-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bbca-107">DESCRIPTION</span></span>
<span data-ttu-id="2bbca-108">Cmdleten **set-AzureRmVmssVM** ändrar tillståndet för en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2bbca-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2bbca-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bbca-109">EXAMPLES</span></span>

## <span data-ttu-id="2bbca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bbca-110">PARAMETERS</span></span>

### <span data-ttu-id="2bbca-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2bbca-111">-InstanceId</span></span>
<span data-ttu-id="2bbca-112">Anger ID för den VMSS-instans som denna cmdlet ändrar tillstånd för.</span><span class="sxs-lookup"><span data-stu-id="2bbca-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbca-113">-Ombild</span><span class="sxs-lookup"><span data-stu-id="2bbca-113">-Reimage</span></span>
<span data-ttu-id="2bbca-114">Anger att denna cmdlet ombildar VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="2bbca-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bbca-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="2bbca-115">-ReimageAll</span></span>
<span data-ttu-id="2bbca-116">Anger att cmdleten återavbildningar alla diskar i VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="2bbca-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bbca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbca-117">-ResourceGroupName</span></span>
<span data-ttu-id="2bbca-118">Anger namnet på den resurs grupp som innehåller VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="2bbca-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="2bbca-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2bbca-119">-VMScaleSetName</span></span>
<span data-ttu-id="2bbca-120">Anger namnet på den VMSS-instans som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="2bbca-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2bbca-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bbca-121">-Confirm</span></span>
<span data-ttu-id="2bbca-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bbca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbca-123">-WhatIf</span></span>
<span data-ttu-id="2bbca-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bbca-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bbca-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bbca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbca-126">CommonParameters</span></span>
<span data-ttu-id="2bbca-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bbca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbca-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bbca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbca-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bbca-129">INPUTS</span></span>

### <span data-ttu-id="2bbca-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="2bbca-130">None</span></span>
<span data-ttu-id="2bbca-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2bbca-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bbca-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bbca-132">OUTPUTS</span></span>

## <span data-ttu-id="2bbca-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bbca-133">NOTES</span></span>

## <span data-ttu-id="2bbca-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bbca-134">RELATED LINKS</span></span>

[<span data-ttu-id="2bbca-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="2bbca-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
