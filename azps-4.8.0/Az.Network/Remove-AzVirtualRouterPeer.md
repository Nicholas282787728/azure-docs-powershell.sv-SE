---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259248"
---
# <span data-ttu-id="2ac46-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2ac46-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="2ac46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ac46-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac46-103">Tar bort en peer från en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2ac46-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="2ac46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ac46-104">SYNTAX</span></span>

### <span data-ttu-id="2ac46-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2ac46-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac46-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac46-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac46-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac46-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac46-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ac46-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac46-109">Cmdleten **Remove-AzVirtualRouterPeer** tar bort en VirtualRouter-peer från en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2ac46-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="2ac46-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ac46-110">EXAMPLES</span></span>

### <span data-ttu-id="2ac46-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ac46-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="2ac46-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2ac46-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="2ac46-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2ac46-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="2ac46-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ac46-114">PARAMETERS</span></span>

### <span data-ttu-id="2ac46-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ac46-115">-AsJob</span></span>
<span data-ttu-id="2ac46-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2ac46-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ac46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac46-117">-DefaultProfile</span></span>
<span data-ttu-id="2ac46-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac46-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2ac46-119">-Force</span></span>
<span data-ttu-id="2ac46-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="2ac46-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2ac46-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac46-121">-InputObject</span></span>
<span data-ttu-id="2ac46-122">Peer-indatavärdet för virtuella routrar.</span><span class="sxs-lookup"><span data-stu-id="2ac46-122">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac46-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2ac46-123">-PeerName</span></span>
<span data-ttu-id="2ac46-124">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="2ac46-124">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac46-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ac46-126">Namnet på den virtuella routern/peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="2ac46-126">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac46-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac46-127">-ResourceId</span></span>
<span data-ttu-id="2ac46-128">Resurs-ID för virtuell router-peer.</span><span class="sxs-lookup"><span data-stu-id="2ac46-128">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac46-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="2ac46-129">-VirtualRouterName</span></span>
<span data-ttu-id="2ac46-130">Den virtuella router där peer finns.</span><span class="sxs-lookup"><span data-stu-id="2ac46-130">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac46-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ac46-131">-Confirm</span></span>
<span data-ttu-id="2ac46-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ac46-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac46-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac46-133">-WhatIf</span></span>
<span data-ttu-id="2ac46-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ac46-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac46-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ac46-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac46-136">CommonParameters</span></span>
<span data-ttu-id="2ac46-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac46-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ac46-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac46-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ac46-139">INPUTS</span></span>

### <span data-ttu-id="2ac46-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac46-140">System.String</span></span>

### <span data-ttu-id="2ac46-141">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2ac46-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="2ac46-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ac46-142">OUTPUTS</span></span>

### <span data-ttu-id="2ac46-143">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2ac46-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="2ac46-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ac46-144">NOTES</span></span>

## <span data-ttu-id="2ac46-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ac46-145">RELATED LINKS</span></span>
