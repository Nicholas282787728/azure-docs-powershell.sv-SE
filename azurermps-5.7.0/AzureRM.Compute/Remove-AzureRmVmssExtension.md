---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576583"
---
# <span data-ttu-id="4d6d2-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4d6d2-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="4d6d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6d2-103">Tar bort ett tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d6d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d6d2-104">SYNTAX</span></span>

### <span data-ttu-id="4d6d2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6d2-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d6d2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6d2-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d6d2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d6d2-107">DESCRIPTION</span></span>
<span data-ttu-id="4d6d2-108">Cmdleten **Remove-AzureRmVmssExtension** tar bort ett tillägg från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4d6d2-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4d6d2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d6d2-109">EXAMPLES</span></span>

## <span data-ttu-id="4d6d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d6d2-110">PARAMETERS</span></span>

### <span data-ttu-id="4d6d2-111">-ID</span><span class="sxs-lookup"><span data-stu-id="4d6d2-111">-Id</span></span>
<span data-ttu-id="4d6d2-112">Anger ID för tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6d2-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d6d2-113">-Name</span></span>
<span data-ttu-id="4d6d2-114">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6d2-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d6d2-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d6d2-116">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-116">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6d2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d6d2-117">-Confirm</span></span>
<span data-ttu-id="4d6d2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d6d2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d6d2-119">-WhatIf</span></span>
<span data-ttu-id="4d6d2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d6d2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d6d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6d2-122">CommonParameters</span></span>
<span data-ttu-id="4d6d2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6d2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6d2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d6d2-125">INPUTS</span></span>

### <span data-ttu-id="4d6d2-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d6d2-126">None</span></span>
<span data-ttu-id="4d6d2-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d6d2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d6d2-128">OUTPUTS</span></span>

### <span data-ttu-id="4d6d2-129">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4d6d2-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4d6d2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d6d2-130">NOTES</span></span>

## <span data-ttu-id="4d6d2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d6d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="4d6d2-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4d6d2-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
