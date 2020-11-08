---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262538"
---
# <span data-ttu-id="49fcc-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="49fcc-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="49fcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="49fcc-103">Skapar en Azure-VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="49fcc-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="49fcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49fcc-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49fcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="49fcc-106">Cmdleten **New-AzVirtualRouter** skapar en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="49fcc-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="49fcc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="49fcc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49fcc-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="49fcc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49fcc-109">PARAMETERS</span></span>

### <span data-ttu-id="49fcc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49fcc-110">-AsJob</span></span>
<span data-ttu-id="49fcc-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="49fcc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49fcc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fcc-112">-DefaultProfile</span></span>
<span data-ttu-id="49fcc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49fcc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49fcc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="49fcc-114">-Force</span></span>
<span data-ttu-id="49fcc-115">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="49fcc-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="49fcc-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="49fcc-116">-HostedSubnet</span></span>
<span data-ttu-id="49fcc-117">Det undernät där den virtuella routern är värd.</span><span class="sxs-lookup"><span data-stu-id="49fcc-117">The subnet where the virtual router is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fcc-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="49fcc-118">-Location</span></span>
<span data-ttu-id="49fcc-119">Platsen.</span><span class="sxs-lookup"><span data-stu-id="49fcc-119">The location.</span></span>

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

### <span data-ttu-id="49fcc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="49fcc-120">-Name</span></span>
<span data-ttu-id="49fcc-121">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="49fcc-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="49fcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49fcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="49fcc-123">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="49fcc-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="49fcc-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="49fcc-124">-Tag</span></span>
<span data-ttu-id="49fcc-125">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="49fcc-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fcc-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49fcc-126">-Confirm</span></span>
<span data-ttu-id="49fcc-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49fcc-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fcc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fcc-128">-WhatIf</span></span>
<span data-ttu-id="49fcc-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49fcc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49fcc-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49fcc-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fcc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fcc-131">CommonParameters</span></span>
<span data-ttu-id="49fcc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49fcc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fcc-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49fcc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fcc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49fcc-134">INPUTS</span></span>

### <span data-ttu-id="49fcc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="49fcc-135">System.String</span></span>

### <span data-ttu-id="49fcc-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="49fcc-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49fcc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49fcc-137">OUTPUTS</span></span>

### <span data-ttu-id="49fcc-138">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="49fcc-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="49fcc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49fcc-139">NOTES</span></span>

## <span data-ttu-id="49fcc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49fcc-140">RELATED LINKS</span></span>
