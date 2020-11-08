---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090236"
---
# <span data-ttu-id="064c5-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="064c5-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="064c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="064c5-102">SYNOPSIS</span></span>
<span data-ttu-id="064c5-103">Sparar en ändrad Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="064c5-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="064c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="064c5-104">SYNTAX</span></span>

### <span data-ttu-id="064c5-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="064c5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="064c5-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="064c5-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="064c5-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="064c5-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="064c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="064c5-108">DESCRIPTION</span></span>
<span data-ttu-id="064c5-109">Cmdleten **set-AzFirewallPolicy** uppdaterar en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="064c5-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="064c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="064c5-110">EXAMPLES</span></span>

### <span data-ttu-id="064c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="064c5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="064c5-112">I det här exemplet anges brand Väggs principen med det nya värdet för brand Väggs princip</span><span class="sxs-lookup"><span data-stu-id="064c5-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="064c5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="064c5-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="064c5-114">I det här exemplet anges brand Väggs principen med det nya hotets-Intel-läget</span><span class="sxs-lookup"><span data-stu-id="064c5-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="064c5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="064c5-115">PARAMETERS</span></span>

### <span data-ttu-id="064c5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="064c5-116">-AsJob</span></span>
<span data-ttu-id="064c5-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="064c5-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="064c5-118">-BasePolicy</span></span>
<span data-ttu-id="064c5-119">Bas policy att ärva från</span><span class="sxs-lookup"><span data-stu-id="064c5-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064c5-120">-DefaultProfile</span></span>
<span data-ttu-id="064c5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="064c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="064c5-122">-InputObject</span></span>
<span data-ttu-id="064c5-123">AzureFirewall policy</span><span class="sxs-lookup"><span data-stu-id="064c5-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="064c5-124">-Location</span></span>
<span data-ttu-id="064c5-125">plats.</span><span class="sxs-lookup"><span data-stu-id="064c5-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="064c5-126">-Name</span></span>
<span data-ttu-id="064c5-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="064c5-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="064c5-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="064c5-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="064c5-130">-ResourceId</span></span>
<span data-ttu-id="064c5-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="064c5-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="064c5-132">-Tag</span></span>
<span data-ttu-id="064c5-133">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="064c5-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="064c5-134">-ThreatIntelMode</span></span>
<span data-ttu-id="064c5-135">Åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="064c5-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="064c5-136">-Confirm</span></span>
<span data-ttu-id="064c5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="064c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064c5-138">-WhatIf</span></span>
<span data-ttu-id="064c5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="064c5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064c5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="064c5-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064c5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064c5-141">CommonParameters</span></span>
<span data-ttu-id="064c5-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064c5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064c5-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="064c5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064c5-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="064c5-144">INPUTS</span></span>

### <span data-ttu-id="064c5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="064c5-145">System.String</span></span>

### <span data-ttu-id="064c5-146">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="064c5-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="064c5-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="064c5-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="064c5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="064c5-148">OUTPUTS</span></span>

### <span data-ttu-id="064c5-149">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="064c5-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="064c5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="064c5-150">NOTES</span></span>

## <span data-ttu-id="064c5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="064c5-151">RELATED LINKS</span></span>
