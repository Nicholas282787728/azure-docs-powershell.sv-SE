---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575203"
---
# <span data-ttu-id="7c17d-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7c17d-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="7c17d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c17d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c17d-103">Skapar en brand Väggs nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="7c17d-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c17d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c17d-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c17d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c17d-105">DESCRIPTION</span></span>
<span data-ttu-id="7c17d-106">Cmdleten **New-AzureRmFirewallNetworkRule** skapar en nätverks regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="7c17d-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="7c17d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c17d-107">EXAMPLES</span></span>

### <span data-ttu-id="7c17d-108">1: skapa en regel för all TCP-trafik</span><span class="sxs-lookup"><span data-stu-id="7c17d-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="7c17d-109">I det här exemplet skapas en regel för all TCP-trafik.</span><span class="sxs-lookup"><span data-stu-id="7c17d-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="7c17d-110">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="7c17d-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="7c17d-111">2: skapa en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="7c17d-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="7c17d-112">I det här exemplet skapas en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="7c17d-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="7c17d-113">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="7c17d-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="7c17d-114">3: skapa en regel för all TCP-och ICMP-trafik från valfri källa till 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="7c17d-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="7c17d-115">I det här exemplet skapas en regel för all TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="7c17d-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="7c17d-116">Användaren styr om trafik ska tillåtas eller nekas för en regel baserat på den regel samling den är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="7c17d-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="7c17d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c17d-117">PARAMETERS</span></span>

### <span data-ttu-id="7c17d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c17d-118">-DefaultProfile</span></span>
<span data-ttu-id="7c17d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c17d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7c17d-120">-Description</span></span>
<span data-ttu-id="7c17d-121">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="7c17d-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="7c17d-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7c17d-122">-DestinationAddress</span></span>
<span data-ttu-id="7c17d-123">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="7c17d-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7c17d-124">-DestinationPort</span></span>
<span data-ttu-id="7c17d-125">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="7c17d-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c17d-126">-Name</span></span>
<span data-ttu-id="7c17d-127">Anger namnet på den här nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7c17d-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="7c17d-128">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="7c17d-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="7c17d-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7c17d-129">-Protocol</span></span>
<span data-ttu-id="7c17d-130">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="7c17d-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="7c17d-131">Möjliga värden är TCP, UDP, ICMP och any.</span><span class="sxs-lookup"><span data-stu-id="7c17d-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7c17d-132">-SourceAddress</span></span>
<span data-ttu-id="7c17d-133">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="7c17d-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c17d-134">-Confirm</span></span>
<span data-ttu-id="7c17d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c17d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c17d-136">-WhatIf</span></span>
<span data-ttu-id="7c17d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c17d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c17d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c17d-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c17d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c17d-139">CommonParameters</span></span>
<span data-ttu-id="7c17d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c17d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c17d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c17d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c17d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c17d-142">INPUTS</span></span>

### <span data-ttu-id="7c17d-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="7c17d-143">None</span></span>
<span data-ttu-id="7c17d-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7c17d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c17d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c17d-145">OUTPUTS</span></span>

### <span data-ttu-id="7c17d-146">Microsoft. Azure. commands. Networks. Models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7c17d-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="7c17d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c17d-147">NOTES</span></span>

## <span data-ttu-id="7c17d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c17d-148">RELATED LINKS</span></span>

[<span data-ttu-id="7c17d-149">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7c17d-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="7c17d-150">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7c17d-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="7c17d-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7c17d-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
