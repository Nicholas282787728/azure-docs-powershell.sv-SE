---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324624"
---
# <span data-ttu-id="7d2dc-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="7d2dc-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="7d2dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2dc-103">Skapa en ny NAT-regel för Azure Firewall policy</span><span class="sxs-lookup"><span data-stu-id="7d2dc-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="7d2dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d2dc-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d2dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2dc-106">Cmdleten **New-AzFirewallPolicyNatRule** skapar en NAT-regel för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7d2dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d2dc-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2dc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d2dc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="7d2dc-109">I det här exemplet skapas en NAT-regel med käll adress, protokoll, mål adress, målport, översatt adress och översatt port.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="7d2dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d2dc-110">PARAMETERS</span></span>

### <span data-ttu-id="7d2dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2dc-111">-DefaultProfile</span></span>
<span data-ttu-id="7d2dc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d2dc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d2dc-113">-Name</span></span>
<span data-ttu-id="7d2dc-114">Namnet på listan över NAT-regler</span><span class="sxs-lookup"><span data-stu-id="7d2dc-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="7d2dc-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7d2dc-115">-Description</span></span>
<span data-ttu-id="7d2dc-116">Beskrivning av regeln</span><span class="sxs-lookup"><span data-stu-id="7d2dc-116">The description of the rule</span></span>

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

### <span data-ttu-id="7d2dc-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7d2dc-117">-DestinationAddress</span></span>
<span data-ttu-id="7d2dc-118">Mål adresser för regeln.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-118">The destination addresses of the rule.</span></span> <span data-ttu-id="7d2dc-119">Detta måste vara en offentlig IP-brand vägg.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="7d2dc-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7d2dc-120">-DestinationPort</span></span>
<span data-ttu-id="7d2dc-121">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="7d2dc-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="7d2dc-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7d2dc-122">-Protocols</span></span>
<span data-ttu-id="7d2dc-123">Regelns protokoll</span><span class="sxs-lookup"><span data-stu-id="7d2dc-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="7d2dc-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7d2dc-124">-SourceAddress</span></span>
<span data-ttu-id="7d2dc-125">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="7d2dc-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="7d2dc-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d2dc-126">-SourceIpGroup</span></span>
<span data-ttu-id="7d2dc-127">Ipgroups regelns källkod</span><span class="sxs-lookup"><span data-stu-id="7d2dc-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="7d2dc-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7d2dc-128">-TranslatedAddress</span></span>
<span data-ttu-id="7d2dc-129">Den översatta adressen för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="7d2dc-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="7d2dc-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="7d2dc-130">-TranslatedPort</span></span>
<span data-ttu-id="7d2dc-131">Den översatta porten för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="7d2dc-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="7d2dc-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d2dc-132">-Confirm</span></span>
<span data-ttu-id="7d2dc-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2dc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2dc-134">-WhatIf</span></span>
<span data-ttu-id="7d2dc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2dc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2dc-137">CommonParameters</span></span>
<span data-ttu-id="7d2dc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2dc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d2dc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2dc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d2dc-140">INPUTS</span></span>

### <span data-ttu-id="7d2dc-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d2dc-141">None</span></span>

## <span data-ttu-id="7d2dc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d2dc-142">OUTPUTS</span></span>

### <span data-ttu-id="7d2dc-143">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="7d2dc-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="7d2dc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d2dc-144">NOTES</span></span>

## <span data-ttu-id="7d2dc-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d2dc-145">RELATED LINKS</span></span>
