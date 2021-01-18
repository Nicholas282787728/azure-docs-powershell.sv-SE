---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523256"
---
# <span data-ttu-id="9b9bd-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b9bd-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="9b9bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9bd-103">Skapa en ny Azure Firewall-brandväggsregel</span><span class="sxs-lookup"><span data-stu-id="9b9bd-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="9b9bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b9bd-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b9bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b9bd-105">DESCRIPTION</span></span>
<span data-ttu-id="9b9bd-106">Cmdleten **New-AzFirewallPolicyNetworkRule** skapar en nätverks regel för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="9b9bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b9bd-107">EXAMPLES</span></span>

### <span data-ttu-id="9b9bd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b9bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="9b9bd-109">I det här exemplet skapas en nätverks regel med käll adress, protokoll, mål adress och målport</span><span class="sxs-lookup"><span data-stu-id="9b9bd-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="9b9bd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b9bd-110">PARAMETERS</span></span>

### <span data-ttu-id="9b9bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9bd-111">-DefaultProfile</span></span>
<span data-ttu-id="9b9bd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b9bd-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9b9bd-113">-Description</span></span>
<span data-ttu-id="9b9bd-114">Beskrivning av regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9b9bd-115">-DestinationAddress</span></span>
<span data-ttu-id="9b9bd-116">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="9b9bd-117">-DestinationFqdn</span></span>
<span data-ttu-id="9b9bd-118">Mål-FQDN för regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="9b9bd-119">-DestinationIpGroup</span></span>
<span data-ttu-id="9b9bd-120">Mål ipgroups för regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9b9bd-121">-DestinationPort</span></span>
<span data-ttu-id="9b9bd-122">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b9bd-123">-Name</span></span>
<span data-ttu-id="9b9bd-124">Namnet på nätverks regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-124">The name of the Network Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9b9bd-125">-Protocol</span></span>
<span data-ttu-id="9b9bd-126">Regelns protokoll</span><span class="sxs-lookup"><span data-stu-id="9b9bd-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9b9bd-127">-SourceAddress</span></span>
<span data-ttu-id="9b9bd-128">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="9b9bd-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9b9bd-129">-SourceIpGroup</span></span>
<span data-ttu-id="9b9bd-130">Ipgroups regelns källkod</span><span class="sxs-lookup"><span data-stu-id="9b9bd-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9bd-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b9bd-131">-Confirm</span></span>
<span data-ttu-id="9b9bd-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b9bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b9bd-133">-WhatIf</span></span>
<span data-ttu-id="9b9bd-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b9bd-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b9bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9bd-136">CommonParameters</span></span>
<span data-ttu-id="9b9bd-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b9bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9bd-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b9bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9bd-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b9bd-139">INPUTS</span></span>

### <span data-ttu-id="9b9bd-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="9b9bd-140">None</span></span>

## <span data-ttu-id="9b9bd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b9bd-141">OUTPUTS</span></span>

### <span data-ttu-id="9b9bd-142">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b9bd-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="9b9bd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b9bd-143">NOTES</span></span>

## <span data-ttu-id="9b9bd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b9bd-144">RELATED LINKS</span></span>
