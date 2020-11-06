---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574349"
---
# <span data-ttu-id="62e7a-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="62e7a-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="62e7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="62e7a-103">Tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="62e7a-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62e7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62e7a-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62e7a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="62e7a-106">Cmdleten **Remove-AzureRmAvailabilitySet** tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="62e7a-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="62e7a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="62e7a-108">Exempel 1: ta bort en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="62e7a-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="62e7a-109">Det här kommandot tar bort en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="62e7a-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="62e7a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="62e7a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="62e7a-111">-Force</span></span>
<span data-ttu-id="62e7a-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="62e7a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62e7a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="62e7a-113">-Name</span></span>
<span data-ttu-id="62e7a-114">Namnet på tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="62e7a-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e7a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e7a-115">-ResourceGroupName</span></span>
<span data-ttu-id="62e7a-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62e7a-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="62e7a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62e7a-117">-Confirm</span></span>
<span data-ttu-id="62e7a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62e7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e7a-119">-WhatIf</span></span>
<span data-ttu-id="62e7a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62e7a-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="62e7a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62e7a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e7a-122">CommonParameters</span></span>
<span data-ttu-id="62e7a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e7a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e7a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e7a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62e7a-125">INPUTS</span></span>

### <span data-ttu-id="62e7a-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="62e7a-126">None</span></span>
<span data-ttu-id="62e7a-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="62e7a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62e7a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62e7a-128">OUTPUTS</span></span>

## <span data-ttu-id="62e7a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62e7a-129">NOTES</span></span>

## <span data-ttu-id="62e7a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62e7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="62e7a-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="62e7a-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="62e7a-132">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="62e7a-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


