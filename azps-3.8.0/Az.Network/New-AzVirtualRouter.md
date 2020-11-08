---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090948"
---
# <span data-ttu-id="de331-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="de331-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="de331-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de331-102">SYNOPSIS</span></span>
<span data-ttu-id="de331-103">Skapar en Azure-VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="de331-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="de331-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de331-104">SYNTAX</span></span>

### <span data-ttu-id="de331-105">HostedGatewayParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="de331-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de331-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de331-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de331-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de331-107">DESCRIPTION</span></span>
<span data-ttu-id="de331-108">Cmdleten **New-AzVirtualRouter** skapar en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="de331-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="de331-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de331-109">EXAMPLES</span></span>

### <span data-ttu-id="de331-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de331-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="de331-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="de331-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="de331-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de331-112">PARAMETERS</span></span>

### <span data-ttu-id="de331-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de331-113">-AsJob</span></span>
<span data-ttu-id="de331-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="de331-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de331-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de331-115">-DefaultProfile</span></span>
<span data-ttu-id="de331-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de331-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de331-117">-Force</span><span class="sxs-lookup"><span data-stu-id="de331-117">-Force</span></span>
<span data-ttu-id="de331-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="de331-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de331-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="de331-119">-HostedGateway</span></span>
<span data-ttu-id="de331-120">Den gateway där virtuella router måste finnas.</span><span class="sxs-lookup"><span data-stu-id="de331-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="de331-121">-HostedGatewayId</span></span>
<span data-ttu-id="de331-122">ID för den gateway där virtuella router måste finnas.</span><span class="sxs-lookup"><span data-stu-id="de331-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="de331-123">-Location</span></span>
<span data-ttu-id="de331-124">Platsen.</span><span class="sxs-lookup"><span data-stu-id="de331-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="de331-125">-Name</span></span>
<span data-ttu-id="de331-126">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="de331-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de331-127">-ResourceGroupName</span></span>
<span data-ttu-id="de331-128">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="de331-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="de331-129">-Tag</span></span>
<span data-ttu-id="de331-130">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="de331-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de331-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de331-131">-Confirm</span></span>
<span data-ttu-id="de331-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de331-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de331-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de331-133">-WhatIf</span></span>
<span data-ttu-id="de331-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de331-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de331-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de331-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de331-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de331-136">CommonParameters</span></span>
<span data-ttu-id="de331-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de331-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="de331-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de331-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de331-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de331-139">INPUTS</span></span>

### <span data-ttu-id="de331-140">System. String</span><span class="sxs-lookup"><span data-stu-id="de331-140">System.String</span></span>

### <span data-ttu-id="de331-141">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de331-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="de331-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="de331-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de331-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de331-143">OUTPUTS</span></span>

### <span data-ttu-id="de331-144">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="de331-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="de331-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de331-145">NOTES</span></span>

## <span data-ttu-id="de331-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de331-146">RELATED LINKS</span></span>
