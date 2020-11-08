---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271551"
---
# <span data-ttu-id="4046d-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="4046d-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="4046d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4046d-102">SYNOPSIS</span></span>
<span data-ttu-id="4046d-103">Skapar en brand Väggs NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="4046d-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="4046d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4046d-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4046d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4046d-105">DESCRIPTION</span></span>
<span data-ttu-id="4046d-106">Cmdleten **New-AzFirewallNatRule** skapar en NAT-regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="4046d-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="4046d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4046d-107">EXAMPLES</span></span>

### <span data-ttu-id="4046d-108">Exempel 1: skapa en regel för att DNAT alla TCP-trafik från 10.0.0.0/24 med mål 10.1.2.3:80 till destination 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="4046d-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="4046d-109">I det här exemplet skapas en regel som kommer att DNAT all trafik från 10.0.0.0/24 med mål 10.1.2.3:80 till 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="4046d-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="4046d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4046d-110">PARAMETERS</span></span>

### <span data-ttu-id="4046d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4046d-111">-DefaultProfile</span></span>
<span data-ttu-id="4046d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4046d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4046d-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4046d-113">-Description</span></span>
<span data-ttu-id="4046d-114">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="4046d-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4046d-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4046d-115">-DestinationAddress</span></span>
<span data-ttu-id="4046d-116">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="4046d-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="4046d-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4046d-117">-DestinationPort</span></span>
<span data-ttu-id="4046d-118">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="4046d-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="4046d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4046d-119">-Name</span></span>
<span data-ttu-id="4046d-120">Anger namnet på denna NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="4046d-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="4046d-121">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="4046d-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4046d-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4046d-122">-Protocol</span></span>
<span data-ttu-id="4046d-123">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="4046d-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="4046d-124">De protokoll som stöds är TCP och UDP.</span><span class="sxs-lookup"><span data-stu-id="4046d-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="4046d-125">Ett speciellt värde "any" tillåts, vilket betyder att det stämmer överens med både TCP och UDP men inte andra protokoll.</span><span class="sxs-lookup"><span data-stu-id="4046d-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4046d-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4046d-126">-SourceAddress</span></span>
<span data-ttu-id="4046d-127">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="4046d-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="4046d-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="4046d-128">-SourceIpGroup</span></span>
<span data-ttu-id="4046d-129">Ipgroup regelns källkod</span><span class="sxs-lookup"><span data-stu-id="4046d-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="4046d-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="4046d-130">-TranslatedAddress</span></span>
<span data-ttu-id="4046d-131">Anger önskat resultat för adress översättningen</span><span class="sxs-lookup"><span data-stu-id="4046d-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="4046d-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="4046d-132">-TranslatedFqdn</span></span>
<span data-ttu-id="4046d-133">Den översatta FQDN för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="4046d-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="4046d-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="4046d-134">-TranslatedPort</span></span>
<span data-ttu-id="4046d-135">Anger önskat resultat för port översättningen</span><span class="sxs-lookup"><span data-stu-id="4046d-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="4046d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4046d-136">-Confirm</span></span>
<span data-ttu-id="4046d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4046d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4046d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4046d-138">-WhatIf</span></span>
<span data-ttu-id="4046d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4046d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4046d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4046d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4046d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4046d-141">CommonParameters</span></span>
<span data-ttu-id="4046d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4046d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4046d-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4046d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4046d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4046d-144">INPUTS</span></span>

### <span data-ttu-id="4046d-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="4046d-145">None</span></span>

## <span data-ttu-id="4046d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4046d-146">OUTPUTS</span></span>

### <span data-ttu-id="4046d-147">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="4046d-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="4046d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4046d-148">NOTES</span></span>

## <span data-ttu-id="4046d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4046d-149">RELATED LINKS</span></span>

[<span data-ttu-id="4046d-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4046d-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="4046d-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4046d-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4046d-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4046d-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
