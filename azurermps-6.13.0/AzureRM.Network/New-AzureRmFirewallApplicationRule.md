---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757846"
---
# <span data-ttu-id="22c6c-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="22c6c-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="22c6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="22c6c-103">Skapar en regel för brand Väggs program.</span><span class="sxs-lookup"><span data-stu-id="22c6c-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22c6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22c6c-104">SYNTAX</span></span>

### <span data-ttu-id="22c6c-105">TargetFqdn (standard)</span><span class="sxs-lookup"><span data-stu-id="22c6c-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c6c-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="22c6c-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="22c6c-108">Cmdleten **New-AzureRmFirewallApplicationRule** skapar en program regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="22c6c-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="22c6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22c6c-109">EXAMPLES</span></span>

### <span data-ttu-id="22c6c-110">1: skapa en regel för att tillåta all HTTPS-trafik från 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="22c6c-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="22c6c-111">I det här exemplet skapas en regel som tillåter all HTTPS-trafik på port 443 från 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="22c6c-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="22c6c-112">2: skapa en regel för att tillåta WindowsUpdate för 10.0.0.0/24 under nätet</span><span class="sxs-lookup"><span data-stu-id="22c6c-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="22c6c-113">I det här exemplet skapas en regel som tillåter trafik för Windows-uppdateringar för 10.0.0.0/24-domän.</span><span class="sxs-lookup"><span data-stu-id="22c6c-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="22c6c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22c6c-114">PARAMETERS</span></span>

### <span data-ttu-id="22c6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c6c-115">-DefaultProfile</span></span>
<span data-ttu-id="22c6c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22c6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6c-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="22c6c-117">-Description</span></span>
<span data-ttu-id="22c6c-118">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="22c6c-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="22c6c-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="22c6c-119">-FqdnTag</span></span>
<span data-ttu-id="22c6c-120">Anger en lista med FQDN-taggar för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="22c6c-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="22c6c-121">Tillgängliga taggar kan hämtas med cmdleten [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="22c6c-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="22c6c-122">-Name</span></span>
<span data-ttu-id="22c6c-123">Anger namnet på den här program regeln.</span><span class="sxs-lookup"><span data-stu-id="22c6c-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="22c6c-124">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="22c6c-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="22c6c-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="22c6c-125">-Protocol</span></span>
<span data-ttu-id="22c6c-126">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="22c6c-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="22c6c-127">Formatet är <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="22c6c-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="22c6c-128">Till exempel "http: 80" eller "https: 443".</span><span class="sxs-lookup"><span data-stu-id="22c6c-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="22c6c-129">Protokoll är obligatoriskt när TargetFqdn används, men det går inte att använda det med FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="22c6c-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="22c6c-130">De protokoll som stöds är HTTP och HTTPS.</span><span class="sxs-lookup"><span data-stu-id="22c6c-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6c-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="22c6c-131">-SourceAddress</span></span>
<span data-ttu-id="22c6c-132">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="22c6c-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6c-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="22c6c-133">-TargetFqdn</span></span>
<span data-ttu-id="22c6c-134">Visar en lista över domän namn som filtrerats efter den här regeln.</span><span class="sxs-lookup"><span data-stu-id="22c6c-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="22c6c-135">Asterisk och tecken, " *', accepteras endast som det första tecknet i ett FQDN i listan. Vid användning matchar asterisk och ett obegränsat antal tecken. (till exempel "* MSN.com" matchar MSN.com och alla dess under domäner)</span><span class="sxs-lookup"><span data-stu-id="22c6c-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6c-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22c6c-136">-Confirm</span></span>
<span data-ttu-id="22c6c-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22c6c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c6c-138">-WhatIf</span></span>
<span data-ttu-id="22c6c-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22c6c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c6c-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22c6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c6c-141">CommonParameters</span></span>
<span data-ttu-id="22c6c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c6c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c6c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c6c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22c6c-144">INPUTS</span></span>

### <span data-ttu-id="22c6c-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="22c6c-145">None</span></span>
<span data-ttu-id="22c6c-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="22c6c-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22c6c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22c6c-147">OUTPUTS</span></span>

### <span data-ttu-id="22c6c-148">Microsoft. Azure. commands. Networks. Models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="22c6c-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="22c6c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22c6c-149">NOTES</span></span>

## <span data-ttu-id="22c6c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22c6c-150">RELATED LINKS</span></span>

[<span data-ttu-id="22c6c-151">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="22c6c-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="22c6c-152">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="22c6c-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="22c6c-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="22c6c-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="22c6c-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="22c6c-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
