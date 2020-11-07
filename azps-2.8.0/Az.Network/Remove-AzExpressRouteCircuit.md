---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: a4672e459a692ce8c0c19b35bf68240d979e75ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918093"
---
# <span data-ttu-id="ee309-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee309-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="ee309-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee309-102">SYNOPSIS</span></span>
<span data-ttu-id="ee309-103">Tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ee309-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ee309-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee309-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee309-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee309-105">DESCRIPTION</span></span>
<span data-ttu-id="ee309-106">Cmdleten **Remove-AzExpressRouteCircuit** tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ee309-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ee309-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee309-107">EXAMPLES</span></span>

### <span data-ttu-id="ee309-108">Exempel 1: ta bort en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="ee309-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="ee309-109">Exempel 2: ta bort en ExpressRoute-krets med rörledningen</span><span class="sxs-lookup"><span data-stu-id="ee309-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="ee309-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee309-110">PARAMETERS</span></span>

### <span data-ttu-id="ee309-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee309-111">-AsJob</span></span>
<span data-ttu-id="ee309-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee309-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee309-113">-DefaultProfile</span></span>
<span data-ttu-id="ee309-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee309-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee309-115">-Force</span></span>
<span data-ttu-id="ee309-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ee309-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee309-117">-Name</span></span>
<span data-ttu-id="ee309-118">Namnet på ExpressRoute-kretsen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ee309-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee309-119">-PassThru</span></span>
<span data-ttu-id="ee309-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ee309-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ee309-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ee309-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee309-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee309-123">Anger namnet på den resurs grupp som den här ExpressRoute-kretsen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ee309-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee309-124">-Confirm</span></span>
<span data-ttu-id="ee309-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee309-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee309-126">-WhatIf</span></span>
<span data-ttu-id="ee309-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee309-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee309-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee309-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee309-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee309-129">CommonParameters</span></span>
<span data-ttu-id="ee309-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee309-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee309-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee309-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee309-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee309-132">INPUTS</span></span>

### <span data-ttu-id="ee309-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee309-133">System.String</span></span>

## <span data-ttu-id="ee309-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee309-134">OUTPUTS</span></span>

### <span data-ttu-id="ee309-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee309-135">System.Boolean</span></span>

## <span data-ttu-id="ee309-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee309-136">NOTES</span></span>

## <span data-ttu-id="ee309-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee309-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee309-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee309-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ee309-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee309-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="ee309-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee309-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="ee309-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee309-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
