---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089496"
---
# <span data-ttu-id="505b2-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="505b2-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="505b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="505b2-102">SYNOPSIS</span></span>
<span data-ttu-id="505b2-103">Skapar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="505b2-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="505b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="505b2-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="505b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="505b2-105">DESCRIPTION</span></span>
<span data-ttu-id="505b2-106">Cmdleten **New-AzPrivateEndpoint** skapar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="505b2-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="505b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="505b2-107">EXAMPLES</span></span>

### <span data-ttu-id="505b2-108">1: skapa en privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="505b2-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="505b2-109">I det här exemplet skapas en privat slut punkt med angivet ID för privat länk tjänst i ett specifikt undernät i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="505b2-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="505b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="505b2-110">PARAMETERS</span></span>

### <span data-ttu-id="505b2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="505b2-111">-AsJob</span></span>
<span data-ttu-id="505b2-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="505b2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="505b2-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="505b2-113">-ByManualRequest</span></span>
<span data-ttu-id="505b2-114">Med manuell begäran.</span><span class="sxs-lookup"><span data-stu-id="505b2-114">Using manual request.</span></span>

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

### <span data-ttu-id="505b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505b2-115">-DefaultProfile</span></span>
<span data-ttu-id="505b2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="505b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="505b2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="505b2-117">-Force</span></span>
<span data-ttu-id="505b2-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="505b2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="505b2-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="505b2-119">-Location</span></span>
<span data-ttu-id="505b2-120">plats.</span><span class="sxs-lookup"><span data-stu-id="505b2-120">location.</span></span>

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

### <span data-ttu-id="505b2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="505b2-121">-Name</span></span>
<span data-ttu-id="505b2-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="505b2-122">The resource name.</span></span>

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

### <span data-ttu-id="505b2-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="505b2-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="505b2-124">Anslutningen till den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="505b2-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="505b2-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="505b2-126">The resource group name.</span></span>

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

### <span data-ttu-id="505b2-127">-Undernät</span><span class="sxs-lookup"><span data-stu-id="505b2-127">-Subnet</span></span>
<span data-ttu-id="505b2-128">Under nätet för den privata slut punkten</span><span class="sxs-lookup"><span data-stu-id="505b2-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505b2-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="505b2-129">-Tag</span></span>
<span data-ttu-id="505b2-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="505b2-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="505b2-131">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="505b2-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="505b2-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="505b2-132">-Confirm</span></span>
<span data-ttu-id="505b2-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="505b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505b2-134">-WhatIf</span></span>
<span data-ttu-id="505b2-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="505b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="505b2-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="505b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="505b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505b2-137">CommonParameters</span></span>
<span data-ttu-id="505b2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505b2-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="505b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505b2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="505b2-140">INPUTS</span></span>

### <span data-ttu-id="505b2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="505b2-141">System.String</span></span>

### <span data-ttu-id="505b2-142">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="505b2-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="505b2-143">Microsoft. Azure. commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="505b2-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="505b2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="505b2-144">OUTPUTS</span></span>

### <span data-ttu-id="505b2-145">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="505b2-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="505b2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="505b2-146">NOTES</span></span>

## <span data-ttu-id="505b2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="505b2-147">RELATED LINKS</span></span>

[<span data-ttu-id="505b2-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="505b2-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="505b2-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="505b2-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="505b2-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="505b2-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)