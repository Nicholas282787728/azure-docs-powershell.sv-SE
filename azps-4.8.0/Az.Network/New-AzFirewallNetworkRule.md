---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262572"
---
# <span data-ttu-id="8c5f9-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8c5f9-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="8c5f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5f9-103">Skapar en brand Väggs nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="8c5f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c5f9-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c5f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c5f9-105">DESCRIPTION</span></span>
<span data-ttu-id="8c5f9-106">Cmdleten **New-AzFirewallNetworkRule** skapar en nätverks regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="8c5f9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c5f9-107">EXAMPLES</span></span>

### <span data-ttu-id="8c5f9-108">Exempel 1: skapa en regel för all TCP-trafik</span><span class="sxs-lookup"><span data-stu-id="8c5f9-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="8c5f9-109">I det här exemplet skapas en regel för all TCP-trafik.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="8c5f9-110">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="8c5f9-111">Exempel 2: skapa en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="8c5f9-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="8c5f9-112">I det här exemplet skapas en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="8c5f9-113">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="8c5f9-114">Exempel 3: skapa en regel för all TCP-och ICMP-trafik från valfri källa till 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="8c5f9-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="8c5f9-115">I det här exemplet skapas en regel för all TCP-trafik från valfri källa till 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="8c5f9-116">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="8c5f9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c5f9-117">PARAMETERS</span></span>

### <span data-ttu-id="8c5f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c5f9-118">-DefaultProfile</span></span>
<span data-ttu-id="8c5f9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c5f9-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8c5f9-120">-Description</span></span>
<span data-ttu-id="8c5f9-121">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8c5f9-122">-DestinationAddress</span></span>
<span data-ttu-id="8c5f9-123">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="8c5f9-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="8c5f9-124">-DestinationFqdn</span></span>
<span data-ttu-id="8c5f9-125">Mål-FQDN för regeln</span><span class="sxs-lookup"><span data-stu-id="8c5f9-125">The destination FQDN of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5f9-126">-DestinationIpGroup</span></span>
<span data-ttu-id="8c5f9-127">Mål ipgroup för regeln</span><span class="sxs-lookup"><span data-stu-id="8c5f9-127">The destination ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8c5f9-128">-DestinationPort</span></span>
<span data-ttu-id="8c5f9-129">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="8c5f9-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c5f9-130">-Name</span></span>
<span data-ttu-id="8c5f9-131">Anger namnet på den här nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="8c5f9-132">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="8c5f9-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8c5f9-133">-Protocol</span></span>
<span data-ttu-id="8c5f9-134">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="8c5f9-135">Möjliga värden är TCP, UDP, ICMP och any.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="8c5f9-136">-SourceAddress</span></span>
<span data-ttu-id="8c5f9-137">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="8c5f9-137">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5f9-138">-SourceIpGroup</span></span>
<span data-ttu-id="8c5f9-139">Ipgroup regelns källkod</span><span class="sxs-lookup"><span data-stu-id="8c5f9-139">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c5f9-140">-Confirm</span></span>
<span data-ttu-id="8c5f9-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5f9-142">-WhatIf</span></span>
<span data-ttu-id="8c5f9-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c5f9-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5f9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5f9-145">CommonParameters</span></span>
<span data-ttu-id="8c5f9-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c5f9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5f9-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5f9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5f9-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c5f9-148">INPUTS</span></span>

### <span data-ttu-id="8c5f9-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="8c5f9-149">None</span></span>

## <span data-ttu-id="8c5f9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c5f9-150">OUTPUTS</span></span>

### <span data-ttu-id="8c5f9-151">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8c5f9-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="8c5f9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c5f9-152">NOTES</span></span>

## <span data-ttu-id="8c5f9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c5f9-153">RELATED LINKS</span></span>

[<span data-ttu-id="8c5f9-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8c5f9-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="8c5f9-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8c5f9-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="8c5f9-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8c5f9-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
