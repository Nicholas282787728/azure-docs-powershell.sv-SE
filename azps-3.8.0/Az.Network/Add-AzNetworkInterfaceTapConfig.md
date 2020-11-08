---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925821"
---
# <span data-ttu-id="7cad9-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7cad9-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="7cad9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cad9-102">SYNOPSIS</span></span>
<span data-ttu-id="7cad9-103">Skapar en TapConfiguration resurs kopplad till en NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="7cad9-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="7cad9-104">Detta hänvisar till en befintlig VirtualNetworkTap-resurs.</span><span class="sxs-lookup"><span data-stu-id="7cad9-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="7cad9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cad9-105">SYNTAX</span></span>

### <span data-ttu-id="7cad9-106">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7cad9-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cad9-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cad9-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cad9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cad9-108">DESCRIPTION</span></span>
<span data-ttu-id="7cad9-109">Cmdleten **Add-AzNetworkInterfaceTapConfig** skapar en TapConfiguration-resurs som är kopplad till en NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="7cad9-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="7cad9-110">Detta hänvisar till en befintlig VirtualNetworkTap-resurs.</span><span class="sxs-lookup"><span data-stu-id="7cad9-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="7cad9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cad9-111">EXAMPLES</span></span>

### <span data-ttu-id="7cad9-112">Exempel 1: lägga till TapConfiguration i en given NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7cad9-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="7cad9-113">Lägg till TapConfiguration på en sourceNic.</span><span class="sxs-lookup"><span data-stu-id="7cad9-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="7cad9-114">Trafiken från sourceNic virtuella dator kommer att speglas till den virtuella dator som hänvisas till i vVirtualNetworkTap-resursen.</span><span class="sxs-lookup"><span data-stu-id="7cad9-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="7cad9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cad9-115">PARAMETERS</span></span>

### <span data-ttu-id="7cad9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cad9-116">-DefaultProfile</span></span>
<span data-ttu-id="7cad9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cad9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cad9-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cad9-118">-Name</span></span>
<span data-ttu-id="7cad9-119">Namnet på tryck konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7cad9-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="7cad9-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7cad9-120">-NetworkInterface</span></span>
<span data-ttu-id="7cad9-121">Referensen för nätverks gränssnitts resursen.</span><span class="sxs-lookup"><span data-stu-id="7cad9-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cad9-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7cad9-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="7cad9-123">Referensen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="7cad9-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cad9-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="7cad9-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="7cad9-125">Referensen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="7cad9-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cad9-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cad9-126">-Confirm</span></span>
<span data-ttu-id="7cad9-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cad9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cad9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cad9-128">-WhatIf</span></span>
<span data-ttu-id="7cad9-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cad9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cad9-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cad9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cad9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cad9-131">CommonParameters</span></span>
<span data-ttu-id="7cad9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cad9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cad9-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cad9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cad9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cad9-134">INPUTS</span></span>

### <span data-ttu-id="7cad9-135">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7cad9-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="7cad9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7cad9-136">System.String</span></span>

### <span data-ttu-id="7cad9-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7cad9-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="7cad9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cad9-138">OUTPUTS</span></span>

### <span data-ttu-id="7cad9-139">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7cad9-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7cad9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cad9-140">NOTES</span></span>

## <span data-ttu-id="7cad9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cad9-141">RELATED LINKS</span></span>

[<span data-ttu-id="7cad9-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7cad9-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7cad9-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7cad9-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7cad9-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7cad9-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)