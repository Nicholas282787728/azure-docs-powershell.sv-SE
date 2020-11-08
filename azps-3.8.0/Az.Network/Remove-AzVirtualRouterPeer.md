---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 871a06a2bbd3a844dd758dbc16189afdb261db2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091691"
---
# <span data-ttu-id="bfaa7-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="bfaa7-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="bfaa7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfaa7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfaa7-103">Tar bort en peer från en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bfaa7-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="bfaa7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfaa7-104">SYNTAX</span></span>

### <span data-ttu-id="bfaa7-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bfaa7-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfaa7-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfaa7-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfaa7-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfaa7-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfaa7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfaa7-108">DESCRIPTION</span></span>
<span data-ttu-id="bfaa7-109">Cmdleten **Remove-AzVirtualRouterPeer** tar bort en VirtualRouter-peer från en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bfaa7-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="bfaa7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfaa7-110">EXAMPLES</span></span>

### <span data-ttu-id="bfaa7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bfaa7-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="bfaa7-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bfaa7-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="bfaa7-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bfaa7-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="bfaa7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfaa7-114">PARAMETERS</span></span>

### <span data-ttu-id="bfaa7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfaa7-115">-AsJob</span></span>
<span data-ttu-id="bfaa7-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bfaa7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfaa7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfaa7-117">-DefaultProfile</span></span>
<span data-ttu-id="bfaa7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfaa7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bfaa7-119">-Force</span></span>
<span data-ttu-id="bfaa7-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="bfaa7-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bfaa7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfaa7-121">-InputObject</span></span>
<span data-ttu-id="bfaa7-122">Peer-indatavärdet för virtuella routrar.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-122">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaa7-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-123">-PeerName</span></span>
<span data-ttu-id="bfaa7-124">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-124">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaa7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-125">-ResourceGroupName</span></span>
<span data-ttu-id="bfaa7-126">Namnet på den virtuella routern/peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-126">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaa7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfaa7-127">-ResourceId</span></span>
<span data-ttu-id="bfaa7-128">Resurs-ID för virtuell router-peer.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-128">The virtual router peer resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaa7-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-129">-VirtualRouterName</span></span>
<span data-ttu-id="bfaa7-130">Den virtuella router där peer finns.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-130">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaa7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bfaa7-131">-Confirm</span></span>
<span data-ttu-id="bfaa7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfaa7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfaa7-133">-WhatIf</span></span>
<span data-ttu-id="bfaa7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfaa7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfaa7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaa7-136">CommonParameters</span></span>
<span data-ttu-id="bfaa7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaa7-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfaa7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaa7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfaa7-139">INPUTS</span></span>

### <span data-ttu-id="bfaa7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bfaa7-140">System.String</span></span>

### <span data-ttu-id="bfaa7-141">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="bfaa7-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="bfaa7-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfaa7-142">OUTPUTS</span></span>

### <span data-ttu-id="bfaa7-143">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bfaa7-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="bfaa7-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfaa7-144">NOTES</span></span>

## <span data-ttu-id="bfaa7-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfaa7-145">RELATED LINKS</span></span>
