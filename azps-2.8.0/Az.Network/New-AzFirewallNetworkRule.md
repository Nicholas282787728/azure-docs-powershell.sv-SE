---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 06cac261d368dfafa19b96b42945ed9cda613122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918289"
---
# <span data-ttu-id="ee76e-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ee76e-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="ee76e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee76e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee76e-103">Skapar en brand Väggs nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="ee76e-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="ee76e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee76e-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee76e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee76e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee76e-106">Cmdleten **New-AzFirewallNetworkRule** skapar en nätverks regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ee76e-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="ee76e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee76e-107">EXAMPLES</span></span>

### <span data-ttu-id="ee76e-108">1: skapa en regel för all TCP-trafik</span><span class="sxs-lookup"><span data-stu-id="ee76e-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="ee76e-109">I det här exemplet skapas en regel för all TCP-trafik.</span><span class="sxs-lookup"><span data-stu-id="ee76e-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="ee76e-110">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="ee76e-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ee76e-111">2: skapa en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="ee76e-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="ee76e-112">I det här exemplet skapas en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="ee76e-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="ee76e-113">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="ee76e-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ee76e-114">3: skapa en regel för all TCP-och ICMP-trafik från valfri källa till 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="ee76e-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="ee76e-115">I det här exemplet skapas en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="ee76e-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="ee76e-116">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="ee76e-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="ee76e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee76e-117">PARAMETERS</span></span>

### <span data-ttu-id="ee76e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee76e-118">-DefaultProfile</span></span>
<span data-ttu-id="ee76e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee76e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee76e-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ee76e-120">-Description</span></span>
<span data-ttu-id="ee76e-121">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ee76e-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ee76e-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ee76e-122">-DestinationAddress</span></span>
<span data-ttu-id="ee76e-123">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="ee76e-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ee76e-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ee76e-124">-DestinationPort</span></span>
<span data-ttu-id="ee76e-125">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="ee76e-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ee76e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee76e-126">-Name</span></span>
<span data-ttu-id="ee76e-127">Anger namnet på den här nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="ee76e-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="ee76e-128">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="ee76e-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ee76e-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ee76e-129">-Protocol</span></span>
<span data-ttu-id="ee76e-130">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ee76e-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="ee76e-131">Möjliga värden är TCP, UDP, ICMP och any.</span><span class="sxs-lookup"><span data-stu-id="ee76e-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="ee76e-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ee76e-132">-SourceAddress</span></span>
<span data-ttu-id="ee76e-133">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="ee76e-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ee76e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee76e-134">-Confirm</span></span>
<span data-ttu-id="ee76e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee76e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee76e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee76e-136">-WhatIf</span></span>
<span data-ttu-id="ee76e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee76e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee76e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee76e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee76e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee76e-139">CommonParameters</span></span>
<span data-ttu-id="ee76e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee76e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee76e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee76e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee76e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee76e-142">INPUTS</span></span>

### <span data-ttu-id="ee76e-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="ee76e-143">None</span></span>

## <span data-ttu-id="ee76e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee76e-144">OUTPUTS</span></span>

### <span data-ttu-id="ee76e-145">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ee76e-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ee76e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee76e-146">NOTES</span></span>

## <span data-ttu-id="ee76e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee76e-147">RELATED LINKS</span></span>

[<span data-ttu-id="ee76e-148">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ee76e-148">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="ee76e-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ee76e-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ee76e-150">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ee76e-150">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
