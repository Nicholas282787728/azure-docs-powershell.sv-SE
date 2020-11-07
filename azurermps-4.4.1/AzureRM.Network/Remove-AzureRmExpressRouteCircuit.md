---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577636"
---
# <span data-ttu-id="3c5f4-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c5f4-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3c5f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5f4-103">Tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c5f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c5f4-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c5f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="3c5f4-106">Cmdleten **Remove-AzureRmExpressRouteCircuit** tar bort en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3c5f4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c5f4-107">EXAMPLES</span></span>

### <span data-ttu-id="3c5f4-108">Exempel 1: ta bort en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="3c5f4-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="3c5f4-109">Exempel 2: ta bort en ExpressRoute-krets med rörledningen</span><span class="sxs-lookup"><span data-stu-id="3c5f4-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="3c5f4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c5f4-110">PARAMETERS</span></span>

### <span data-ttu-id="3c5f4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3c5f4-111">-Force</span></span>
<span data-ttu-id="3c5f4-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c5f4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c5f4-113">-Name</span></span>
<span data-ttu-id="3c5f4-114">Namnet på ExpressRoute-kretsen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="3c5f4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c5f4-115">-PassThru</span></span>
<span data-ttu-id="3c5f4-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3c5f4-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c5f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c5f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c5f4-119">Anger namnet på den resurs grupp som den här ExpressRoute-kretsen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="3c5f4-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c5f4-120">-Confirm</span></span>
<span data-ttu-id="3c5f4-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c5f4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c5f4-122">-WhatIf</span></span>
<span data-ttu-id="3c5f4-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c5f4-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c5f4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5f4-125">-DefaultProfile</span></span>
<span data-ttu-id="3c5f4-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c5f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5f4-127">CommonParameters</span></span>
<span data-ttu-id="3c5f4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c5f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5f4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c5f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5f4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c5f4-130">INPUTS</span></span>

## <span data-ttu-id="3c5f4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c5f4-131">OUTPUTS</span></span>

## <span data-ttu-id="3c5f4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c5f4-132">NOTES</span></span>

## <span data-ttu-id="3c5f4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c5f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c5f4-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c5f4-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3c5f4-135">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c5f4-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3c5f4-136">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c5f4-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3c5f4-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c5f4-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)