---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262504"
---
# <span data-ttu-id="6273f-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6273f-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="6273f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6273f-102">SYNOPSIS</span></span>
<span data-ttu-id="6273f-103">Sparar en ändrad Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="6273f-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="6273f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6273f-104">SYNTAX</span></span>

### <span data-ttu-id="6273f-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6273f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6273f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6273f-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6273f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6273f-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6273f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6273f-108">DESCRIPTION</span></span>
<span data-ttu-id="6273f-109">Cmdleten **set-AzFirewallPolicy** uppdaterar en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="6273f-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="6273f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6273f-110">EXAMPLES</span></span>

### <span data-ttu-id="6273f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6273f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="6273f-112">I det här exemplet anges brand Väggs principen med det nya värdet för brand Väggs princip</span><span class="sxs-lookup"><span data-stu-id="6273f-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="6273f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6273f-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="6273f-114">I det här exemplet anges brand Väggs principen med det nya hotets-Intel-läget</span><span class="sxs-lookup"><span data-stu-id="6273f-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="6273f-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6273f-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="6273f-116">I det här exemplet anges brand Väggs principen med det nya hotet Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="6273f-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="6273f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6273f-117">PARAMETERS</span></span>

### <span data-ttu-id="6273f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6273f-118">-AsJob</span></span>
<span data-ttu-id="6273f-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6273f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6273f-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="6273f-120">-BasePolicy</span></span>
<span data-ttu-id="6273f-121">Bas policy att ärva från</span><span class="sxs-lookup"><span data-stu-id="6273f-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="6273f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6273f-122">-DefaultProfile</span></span>
<span data-ttu-id="6273f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6273f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6273f-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="6273f-124">-DnsSetting</span></span>
<span data-ttu-id="6273f-125">DNS-inställningen</span><span class="sxs-lookup"><span data-stu-id="6273f-125">The DNS Setting</span></span>

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

### <span data-ttu-id="6273f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6273f-126">-InputObject</span></span>
<span data-ttu-id="6273f-127">AzureFirewall policy</span><span class="sxs-lookup"><span data-stu-id="6273f-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6273f-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="6273f-128">-Location</span></span>
<span data-ttu-id="6273f-129">plats.</span><span class="sxs-lookup"><span data-stu-id="6273f-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6273f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="6273f-130">-Name</span></span>
<span data-ttu-id="6273f-131">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="6273f-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6273f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6273f-132">-ResourceGroupName</span></span>
<span data-ttu-id="6273f-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6273f-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6273f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6273f-134">-ResourceId</span></span>
<span data-ttu-id="6273f-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6273f-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6273f-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6273f-136">-Tag</span></span>
<span data-ttu-id="6273f-137">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="6273f-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6273f-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="6273f-138">-ThreatIntelMode</span></span>
<span data-ttu-id="6273f-139">Åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="6273f-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="6273f-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="6273f-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="6273f-141">Lägg för Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="6273f-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="6273f-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6273f-142">-Confirm</span></span>
<span data-ttu-id="6273f-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6273f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6273f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6273f-144">-WhatIf</span></span>
<span data-ttu-id="6273f-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6273f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6273f-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6273f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6273f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6273f-147">CommonParameters</span></span>
<span data-ttu-id="6273f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6273f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6273f-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6273f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6273f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6273f-150">INPUTS</span></span>

### <span data-ttu-id="6273f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6273f-151">System.String</span></span>

### <span data-ttu-id="6273f-152">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6273f-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="6273f-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6273f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6273f-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6273f-154">OUTPUTS</span></span>

### <span data-ttu-id="6273f-155">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6273f-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="6273f-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6273f-156">NOTES</span></span>

## <span data-ttu-id="6273f-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6273f-157">RELATED LINKS</span></span>