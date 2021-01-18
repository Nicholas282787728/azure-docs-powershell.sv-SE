---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527448"
---
# <span data-ttu-id="a966d-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a966d-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="a966d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a966d-102">SYNOPSIS</span></span>
<span data-ttu-id="a966d-103">Uppdatera en peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a966d-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="a966d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a966d-104">SYNTAX</span></span>

### <span data-ttu-id="a966d-105">VirtualRouterNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a966d-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a966d-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a966d-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a966d-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a966d-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a966d-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a966d-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a966d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a966d-109">DESCRIPTION</span></span>
<span data-ttu-id="a966d-110">Cmdleten **Update-AzVirtualRouterPeer** uppdaterar en VirtualRouter-peer till en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a966d-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="a966d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a966d-111">EXAMPLES</span></span>

### <span data-ttu-id="a966d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a966d-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="a966d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a966d-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="a966d-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a966d-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="a966d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a966d-115">PARAMETERS</span></span>

### <span data-ttu-id="a966d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a966d-116">-AsJob</span></span>
<span data-ttu-id="a966d-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a966d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a966d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a966d-118">-DefaultProfile</span></span>
<span data-ttu-id="a966d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a966d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a966d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a966d-120">-Force</span></span>
<span data-ttu-id="a966d-121">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="a966d-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a966d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a966d-122">-InputObject</span></span>
<span data-ttu-id="a966d-123">Peer-indatavärdet för virtuella routrar.</span><span class="sxs-lookup"><span data-stu-id="a966d-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="a966d-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a966d-124">-PeerAsn</span></span>
<span data-ttu-id="a966d-125">ASN med motpart.</span><span class="sxs-lookup"><span data-stu-id="a966d-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a966d-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="a966d-126">-PeerIp</span></span>
<span data-ttu-id="a966d-127">Peer-IP.</span><span class="sxs-lookup"><span data-stu-id="a966d-127">Peer Ip.</span></span>

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

### <span data-ttu-id="a966d-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a966d-128">-PeerName</span></span>
<span data-ttu-id="a966d-129">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="a966d-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="a966d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a966d-130">-ResourceGroupName</span></span>
<span data-ttu-id="a966d-131">Namnet på den virtuella routern/peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="a966d-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="a966d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a966d-132">-ResourceId</span></span>
<span data-ttu-id="a966d-133">Resurs-ID för virtuell router-peer.</span><span class="sxs-lookup"><span data-stu-id="a966d-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="a966d-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="a966d-134">-VirtualRouterName</span></span>
<span data-ttu-id="a966d-135">Den virtuella router där peer finns.</span><span class="sxs-lookup"><span data-stu-id="a966d-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="a966d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a966d-136">-Confirm</span></span>
<span data-ttu-id="a966d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a966d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a966d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a966d-138">-WhatIf</span></span>
<span data-ttu-id="a966d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a966d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a966d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a966d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a966d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a966d-141">CommonParameters</span></span>
<span data-ttu-id="a966d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a966d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a966d-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a966d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a966d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a966d-144">INPUTS</span></span>

### <span data-ttu-id="a966d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a966d-145">System.String</span></span>

### <span data-ttu-id="a966d-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="a966d-146">System.UInt32</span></span>

### <span data-ttu-id="a966d-147">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a966d-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="a966d-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a966d-148">OUTPUTS</span></span>

### <span data-ttu-id="a966d-149">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a966d-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a966d-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a966d-150">NOTES</span></span>

## <span data-ttu-id="a966d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a966d-151">RELATED LINKS</span></span>
