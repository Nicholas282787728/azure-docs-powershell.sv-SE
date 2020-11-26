---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272080"
---
# <span data-ttu-id="1bf2d-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="1bf2d-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="1bf2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf2d-103">Lägga till en peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1bf2d-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="1bf2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bf2d-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bf2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bf2d-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf2d-106">Cmdleten **Add-AzVirtualRouterPeer** lägger till en VirtualRouter-peer till en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1bf2d-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="1bf2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bf2d-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf2d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bf2d-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="1bf2d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bf2d-109">PARAMETERS</span></span>

### <span data-ttu-id="1bf2d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bf2d-110">-AsJob</span></span>
<span data-ttu-id="1bf2d-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1bf2d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bf2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf2d-112">-DefaultProfile</span></span>
<span data-ttu-id="1bf2d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf2d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1bf2d-114">-Force</span></span>
<span data-ttu-id="1bf2d-115">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="1bf2d-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1bf2d-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="1bf2d-116">-PeerAsn</span></span>
<span data-ttu-id="1bf2d-117">ASN med motpart.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf2d-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="1bf2d-118">-PeerIp</span></span>
<span data-ttu-id="1bf2d-119">Peer-IP.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-119">Peer Ip.</span></span>

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

### <span data-ttu-id="1bf2d-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="1bf2d-120">-PeerName</span></span>
<span data-ttu-id="1bf2d-121">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="1bf2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1bf2d-123">Namnet på den virtuella routern/peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="1bf2d-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="1bf2d-124">-VirtualRouterName</span></span>
<span data-ttu-id="1bf2d-125">Den virtuella router där peer finns.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="1bf2d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bf2d-126">-Confirm</span></span>
<span data-ttu-id="1bf2d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf2d-128">-WhatIf</span></span>
<span data-ttu-id="1bf2d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf2d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf2d-131">CommonParameters</span></span>
<span data-ttu-id="1bf2d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf2d-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bf2d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf2d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bf2d-134">INPUTS</span></span>

### <span data-ttu-id="1bf2d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1bf2d-135">System.String</span></span>

### <span data-ttu-id="1bf2d-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1bf2d-136">System.UInt32</span></span>

## <span data-ttu-id="1bf2d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bf2d-137">OUTPUTS</span></span>

### <span data-ttu-id="1bf2d-138">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1bf2d-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1bf2d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bf2d-139">NOTES</span></span>

## <span data-ttu-id="1bf2d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bf2d-140">RELATED LINKS</span></span>