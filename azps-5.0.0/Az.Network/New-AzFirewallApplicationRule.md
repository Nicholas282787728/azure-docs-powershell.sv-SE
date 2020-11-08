---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271557"
---
# <span data-ttu-id="ae9d5-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ae9d5-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="ae9d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9d5-103">Skapar en regel för brand Väggs program.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="ae9d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae9d5-104">SYNTAX</span></span>

### <span data-ttu-id="ae9d5-105">TargetFqdn (standard)</span><span class="sxs-lookup"><span data-stu-id="ae9d5-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9d5-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="ae9d5-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="ae9d5-108">Cmdleten **New-AzFirewallApplicationRule** skapar en program regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="ae9d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae9d5-109">EXAMPLES</span></span>

### <span data-ttu-id="ae9d5-110">Exempel 1: skapa en regel för att tillåta all HTTPS-trafik från 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="ae9d5-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="ae9d5-111">I det här exemplet skapas en regel som tillåter all HTTPS-trafik på port 443 från 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="ae9d5-112">Exempel 2: skapa en regel för att tillåta WindowsUpdate för 10.0.0.0/24 under nätet</span><span class="sxs-lookup"><span data-stu-id="ae9d5-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="ae9d5-113">I det här exemplet skapas en regel som tillåter trafik för Windows-uppdateringar för 10.0.0.0/24-domän.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="ae9d5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae9d5-114">PARAMETERS</span></span>

### <span data-ttu-id="ae9d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9d5-115">-DefaultProfile</span></span>
<span data-ttu-id="ae9d5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae9d5-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ae9d5-117">-Description</span></span>
<span data-ttu-id="ae9d5-118">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ae9d5-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="ae9d5-119">-FqdnTag</span></span>
<span data-ttu-id="ae9d5-120">Anger en lista med FQDN-taggar för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="ae9d5-121">Tillgängliga taggar kan hämtas med cmdleten [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="ae9d5-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9d5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae9d5-122">-Name</span></span>
<span data-ttu-id="ae9d5-123">Anger namnet på den här program regeln.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="ae9d5-124">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ae9d5-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ae9d5-125">-Protocol</span></span>
<span data-ttu-id="ae9d5-126">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="ae9d5-127">Formatet är <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="ae9d5-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="ae9d5-128">Till exempel "http: 80" eller "https: 443".</span><span class="sxs-lookup"><span data-stu-id="ae9d5-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="ae9d5-129">Protokoll är obligatoriskt när TargetFqdn används, men det går inte att använda det med FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="ae9d5-130">De protokoll som stöds är HTTP och HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9d5-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ae9d5-131">-SourceAddress</span></span>
<span data-ttu-id="ae9d5-132">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="ae9d5-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ae9d5-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="ae9d5-133">-SourceIpGroup</span></span>
<span data-ttu-id="ae9d5-134">Ipgroup regelns källkod</span><span class="sxs-lookup"><span data-stu-id="ae9d5-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="ae9d5-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="ae9d5-135">-TargetFqdn</span></span>
<span data-ttu-id="ae9d5-136">Visar en lista över domän namn som filtrerats efter den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="ae9d5-137">Asterisken, " *', accepteras endast som det första tecknet i ett FQDN i listan. När den används matchar asterisken ett obegränsat antal tecken. (till exempel "* MSN.com" matchar MSN.com och alla dess under domäner)</span><span class="sxs-lookup"><span data-stu-id="ae9d5-137">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9d5-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae9d5-138">-Confirm</span></span>
<span data-ttu-id="ae9d5-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9d5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9d5-140">-WhatIf</span></span>
<span data-ttu-id="ae9d5-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9d5-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9d5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9d5-143">CommonParameters</span></span>
<span data-ttu-id="ae9d5-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9d5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9d5-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae9d5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9d5-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae9d5-146">INPUTS</span></span>

### <span data-ttu-id="ae9d5-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae9d5-147">None</span></span>

## <span data-ttu-id="ae9d5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae9d5-148">OUTPUTS</span></span>

### <span data-ttu-id="ae9d5-149">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ae9d5-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="ae9d5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae9d5-150">NOTES</span></span>

## <span data-ttu-id="ae9d5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae9d5-151">RELATED LINKS</span></span>

[<span data-ttu-id="ae9d5-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ae9d5-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="ae9d5-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ae9d5-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ae9d5-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ae9d5-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ae9d5-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="ae9d5-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
