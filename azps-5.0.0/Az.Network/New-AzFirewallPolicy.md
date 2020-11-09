---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323808"
---
# <span data-ttu-id="1dea7-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1dea7-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="1dea7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dea7-102">SYNOPSIS</span></span>
<span data-ttu-id="1dea7-103">Skapar en ny Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="1dea7-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="1dea7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dea7-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dea7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dea7-105">DESCRIPTION</span></span>
<span data-ttu-id="1dea7-106">Cmdleten **New-AzFirewallPolicy** skapar en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="1dea7-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="1dea7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dea7-107">EXAMPLES</span></span>

### <span data-ttu-id="1dea7-108">Exempel 1:1.</span><span class="sxs-lookup"><span data-stu-id="1dea7-108">Example 1: 1.</span></span> <span data-ttu-id="1dea7-109">Skapa en tom princip</span><span class="sxs-lookup"><span data-stu-id="1dea7-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="1dea7-110">I det här exemplet skapas en Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="1dea7-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="1dea7-111">Exempel 2:2.</span><span class="sxs-lookup"><span data-stu-id="1dea7-111">Example 2: 2.</span></span> <span data-ttu-id="1dea7-112">Skapa en tom princip med ThreatIntel-läge</span><span class="sxs-lookup"><span data-stu-id="1dea7-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="1dea7-113">I det här exemplet skapas en Azure Firewall-princip med ett hot Intel-läge</span><span class="sxs-lookup"><span data-stu-id="1dea7-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="1dea7-114">Exempel 3:3.</span><span class="sxs-lookup"><span data-stu-id="1dea7-114">Example 3: 3.</span></span> <span data-ttu-id="1dea7-115">Skapa en tom princip med ThreatIntel Lägg</span><span class="sxs-lookup"><span data-stu-id="1dea7-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="1dea7-116">I det här exemplet skapas en Azure Firewall-princip med ett hot Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="1dea7-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="1dea7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dea7-117">PARAMETERS</span></span>

### <span data-ttu-id="1dea7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dea7-118">-AsJob</span></span>
<span data-ttu-id="1dea7-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1dea7-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="1dea7-120">-BasePolicy</span></span>
<span data-ttu-id="1dea7-121">Bas policy att ärva från</span><span class="sxs-lookup"><span data-stu-id="1dea7-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dea7-122">-DefaultProfile</span></span>
<span data-ttu-id="1dea7-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dea7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dea7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1dea7-124">-Force</span></span>
<span data-ttu-id="1dea7-125">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="1dea7-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="1dea7-126">-Location</span></span>
<span data-ttu-id="1dea7-127">plats.</span><span class="sxs-lookup"><span data-stu-id="1dea7-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dea7-128">-Name</span></span>
<span data-ttu-id="1dea7-129">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1dea7-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dea7-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dea7-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1dea7-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1dea7-132">-Tag</span></span>
<span data-ttu-id="1dea7-133">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="1dea7-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1dea7-134">-ThreatIntelMode</span></span>
<span data-ttu-id="1dea7-135">Åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="1dea7-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1dea7-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="1dea7-137">Lägg för Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="1dea7-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="1dea7-138">-DnsSetting</span></span>
<span data-ttu-id="1dea7-139">DNS-inställningen</span><span class="sxs-lookup"><span data-stu-id="1dea7-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dea7-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dea7-140">-Confirm</span></span>
<span data-ttu-id="1dea7-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dea7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dea7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dea7-142">-WhatIf</span></span>
<span data-ttu-id="1dea7-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dea7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dea7-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dea7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dea7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dea7-145">CommonParameters</span></span>
<span data-ttu-id="1dea7-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dea7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dea7-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dea7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dea7-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dea7-148">INPUTS</span></span>

### <span data-ttu-id="1dea7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1dea7-149">System.String</span></span>

### <span data-ttu-id="1dea7-150">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1dea7-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dea7-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dea7-151">OUTPUTS</span></span>

### <span data-ttu-id="1dea7-152">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1dea7-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1dea7-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dea7-153">NOTES</span></span>

## <span data-ttu-id="1dea7-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dea7-154">RELATED LINKS</span></span>
