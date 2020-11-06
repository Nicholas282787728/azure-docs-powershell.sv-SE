---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573505"
---
# <span data-ttu-id="59d82-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="59d82-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="59d82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59d82-102">SYNOPSIS</span></span>
<span data-ttu-id="59d82-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="59d82-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59d82-104">SYNTAX</span></span>

### <span data-ttu-id="59d82-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d82-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59d82-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="59d82-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59d82-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59d82-107">DESCRIPTION</span></span>
<span data-ttu-id="59d82-108">Cmdleten **Update-AzureRmAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="59d82-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="59d82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59d82-109">EXAMPLES</span></span>

### <span data-ttu-id="59d82-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59d82-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="59d82-111">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="59d82-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="59d82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59d82-112">PARAMETERS</span></span>

### <span data-ttu-id="59d82-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="59d82-113">-AvailabilitySet</span></span>
<span data-ttu-id="59d82-114">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="59d82-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59d82-115">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="59d82-115">-Managed</span></span>
<span data-ttu-id="59d82-116">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="59d82-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d82-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="59d82-117">-Sku</span></span>
<span data-ttu-id="59d82-118">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="59d82-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d82-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59d82-119">-Confirm</span></span>
<span data-ttu-id="59d82-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59d82-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d82-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d82-121">-WhatIf</span></span>
<span data-ttu-id="59d82-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59d82-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59d82-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59d82-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d82-124">CommonParameters</span></span>
<span data-ttu-id="59d82-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d82-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d82-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d82-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59d82-127">INPUTS</span></span>

### <span data-ttu-id="59d82-128">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="59d82-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="59d82-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59d82-129">OUTPUTS</span></span>

### <span data-ttu-id="59d82-130">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="59d82-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="59d82-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59d82-131">NOTES</span></span>

## <span data-ttu-id="59d82-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59d82-132">RELATED LINKS</span></span>

