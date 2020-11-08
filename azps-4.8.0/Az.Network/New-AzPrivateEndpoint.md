---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260714"
---
# <span data-ttu-id="21fc5-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fc5-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="21fc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="21fc5-103">Skapar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="21fc5-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="21fc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21fc5-104">SYNTAX</span></span>

### <span data-ttu-id="21fc5-105">Alla</span><span class="sxs-lookup"><span data-stu-id="21fc5-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21fc5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21fc5-106">DESCRIPTION</span></span>

<span data-ttu-id="21fc5-107">Cmdleten **New-AzPrivateEndpoint** skapar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="21fc5-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="21fc5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21fc5-108">EXAMPLES</span></span>

### <span data-ttu-id="21fc5-109">Exempel 1: skapa en privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="21fc5-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="21fc5-110">I följande exempel skapas en privat slut punkt med ett angivet ID för privat länk tjänst i det angivna under nätet i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="21fc5-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="21fc5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21fc5-111">PARAMETERS</span></span>

### <span data-ttu-id="21fc5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21fc5-112">-AsJob</span></span>

<span data-ttu-id="21fc5-113">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="21fc5-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="21fc5-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="21fc5-114">-ByManualRequest</span></span>

<span data-ttu-id="21fc5-115">Använd manuell begäran för att upprätta anslutningen.</span><span class="sxs-lookup"><span data-stu-id="21fc5-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="21fc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fc5-116">-DefaultProfile</span></span>

<span data-ttu-id="21fc5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21fc5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fc5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="21fc5-118">-Force</span></span>

<span data-ttu-id="21fc5-119">Fråga inte efter bekräftelse för att skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="21fc5-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="21fc5-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="21fc5-120">-Location</span></span>

<span data-ttu-id="21fc5-121">Anger en plats för den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="21fc5-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="21fc5-122">Använd [Get-AzLocation](/powershell/module/az.resources/get-azlocation) för att bestämma giltiga värden för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="21fc5-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="21fc5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="21fc5-123">-Name</span></span>

<span data-ttu-id="21fc5-124">Namn på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="21fc5-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="21fc5-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="21fc5-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="21fc5-126">Resurs-ID för att ansluta den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="21fc5-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="21fc5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fc5-127">-ResourceGroupName</span></span>

<span data-ttu-id="21fc5-128">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="21fc5-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="21fc5-129">-Undernät</span><span class="sxs-lookup"><span data-stu-id="21fc5-129">-Subnet</span></span>

<span data-ttu-id="21fc5-130">Under nätet för den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="21fc5-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="21fc5-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="21fc5-131">-Tag</span></span>

<span data-ttu-id="21fc5-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="21fc5-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21fc5-133">Till exempel: @ {key0 = ' value0 '; KEY1 = $null; key2 = ' värde2 '}</span><span class="sxs-lookup"><span data-stu-id="21fc5-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="21fc5-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21fc5-134">-Confirm</span></span>

<span data-ttu-id="21fc5-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21fc5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21fc5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21fc5-136">-WhatIf</span></span>

<span data-ttu-id="21fc5-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21fc5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fc5-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21fc5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21fc5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fc5-139">CommonParameters</span></span>

<span data-ttu-id="21fc5-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21fc5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fc5-141">Mer information finns i [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="21fc5-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="21fc5-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21fc5-142">INPUTS</span></span>

### <span data-ttu-id="21fc5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="21fc5-143">System.String</span></span>

### <span data-ttu-id="21fc5-144">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="21fc5-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="21fc5-145">Microsoft. Azure. commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="21fc5-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="21fc5-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21fc5-146">OUTPUTS</span></span>

### <span data-ttu-id="21fc5-147">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fc5-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="21fc5-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21fc5-148">NOTES</span></span>

## <span data-ttu-id="21fc5-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21fc5-149">RELATED LINKS</span></span>

[<span data-ttu-id="21fc5-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fc5-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="21fc5-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fc5-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="21fc5-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="21fc5-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)