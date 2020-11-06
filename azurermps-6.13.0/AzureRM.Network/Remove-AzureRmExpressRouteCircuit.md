---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e38cdc9a7f0b34fa5e7769192fa5fcb0ad342de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580752"
---
# <span data-ttu-id="1fef2-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1fef2-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="1fef2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fef2-102">SYNOPSIS</span></span>
<span data-ttu-id="1fef2-103">Tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="1fef2-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fef2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fef2-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fef2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fef2-105">DESCRIPTION</span></span>
<span data-ttu-id="1fef2-106">Cmdleten **Remove-AzureRmExpressRouteCircuit** tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="1fef2-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1fef2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fef2-107">EXAMPLES</span></span>

### <span data-ttu-id="1fef2-108">Exempel 1: ta bort en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="1fef2-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="1fef2-109">Exempel 2: ta bort en ExpressRoute-krets med rörledningen</span><span class="sxs-lookup"><span data-stu-id="1fef2-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="1fef2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fef2-110">PARAMETERS</span></span>

### <span data-ttu-id="1fef2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fef2-111">-AsJob</span></span>
<span data-ttu-id="1fef2-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1fef2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fef2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fef2-113">-DefaultProfile</span></span>
<span data-ttu-id="1fef2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fef2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fef2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1fef2-115">-Force</span></span>
<span data-ttu-id="1fef2-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1fef2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1fef2-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fef2-117">-Name</span></span>
<span data-ttu-id="1fef2-118">Namnet på ExpressRoute-kretsen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1fef2-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="1fef2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fef2-119">-PassThru</span></span>
<span data-ttu-id="1fef2-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1fef2-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1fef2-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1fef2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fef2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fef2-122">-ResourceGroupName</span></span>
<span data-ttu-id="1fef2-123">Anger namnet på den resurs grupp som den här ExpressRoute-kretsen tillhör.</span><span class="sxs-lookup"><span data-stu-id="1fef2-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="1fef2-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fef2-124">-Confirm</span></span>
<span data-ttu-id="1fef2-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fef2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fef2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fef2-126">-WhatIf</span></span>
<span data-ttu-id="1fef2-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fef2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fef2-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fef2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fef2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fef2-129">CommonParameters</span></span>
<span data-ttu-id="1fef2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fef2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fef2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fef2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fef2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fef2-132">INPUTS</span></span>

### <span data-ttu-id="1fef2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1fef2-133">System.String</span></span>

## <span data-ttu-id="1fef2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fef2-134">OUTPUTS</span></span>

### <span data-ttu-id="1fef2-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fef2-135">System.Boolean</span></span>

## <span data-ttu-id="1fef2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fef2-136">NOTES</span></span>

## <span data-ttu-id="1fef2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fef2-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fef2-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1fef2-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1fef2-139">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1fef2-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1fef2-140">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1fef2-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1fef2-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1fef2-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
