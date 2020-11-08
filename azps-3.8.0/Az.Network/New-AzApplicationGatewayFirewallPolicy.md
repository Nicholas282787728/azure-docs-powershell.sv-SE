---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: da83c8cd863d8d3cfa62d47c7a4126d15c4dd670
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092544"
---
# <span data-ttu-id="0d78f-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0d78f-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="0d78f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d78f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d78f-103">Skapar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0d78f-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="0d78f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d78f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d78f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d78f-105">DESCRIPTION</span></span>
<span data-ttu-id="0d78f-106">Cmdleten **New-AzApplicationGatewayFirewallPolicy** skapar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0d78f-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="0d78f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d78f-107">EXAMPLES</span></span>

### <span data-ttu-id="0d78f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d78f-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="0d78f-109">Det här kommandot skapar en ny Azure Application Gateway-brandvägg med namnet "wafResource1" i resurs gruppen "RG1" i plats "väst" med anpassade regler definierade i variabeln $customRule</span><span class="sxs-lookup"><span data-stu-id="0d78f-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="0d78f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d78f-110">PARAMETERS</span></span>

### <span data-ttu-id="0d78f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d78f-111">-AsJob</span></span>
<span data-ttu-id="0d78f-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0d78f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d78f-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="0d78f-113">-CustomRule</span></span>
<span data-ttu-id="0d78f-114">Listan med CustomRules</span><span class="sxs-lookup"><span data-stu-id="0d78f-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d78f-115">-DefaultProfile</span></span>
<span data-ttu-id="0d78f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d78f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d78f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0d78f-117">-Force</span></span>
<span data-ttu-id="0d78f-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="0d78f-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0d78f-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0d78f-119">-Location</span></span>
<span data-ttu-id="0d78f-120">plats.</span><span class="sxs-lookup"><span data-stu-id="0d78f-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0d78f-121">-ManagedRule</span></span>
<span data-ttu-id="0d78f-122">Hanterad regel inställning</span><span class="sxs-lookup"><span data-stu-id="0d78f-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d78f-123">-Name</span></span>
<span data-ttu-id="0d78f-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0d78f-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="0d78f-125">-PolicySetting</span></span>
<span data-ttu-id="0d78f-126">Princip inställningar för webb programs brand vägg</span><span class="sxs-lookup"><span data-stu-id="0d78f-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d78f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d78f-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0d78f-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d78f-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0d78f-129">-Tag</span></span>
<span data-ttu-id="0d78f-130">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="0d78f-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0d78f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d78f-131">-Confirm</span></span>
<span data-ttu-id="0d78f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d78f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d78f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d78f-133">-WhatIf</span></span>
<span data-ttu-id="0d78f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d78f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d78f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d78f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d78f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d78f-136">CommonParameters</span></span>
<span data-ttu-id="0d78f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d78f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d78f-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d78f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d78f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d78f-139">INPUTS</span></span>

### <span data-ttu-id="0d78f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d78f-140">System.String</span></span>

### <span data-ttu-id="0d78f-141">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="0d78f-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="0d78f-142">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="0d78f-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="0d78f-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="0d78f-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="0d78f-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0d78f-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0d78f-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d78f-145">OUTPUTS</span></span>

### <span data-ttu-id="0d78f-146">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0d78f-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="0d78f-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d78f-147">NOTES</span></span>

## <span data-ttu-id="0d78f-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d78f-148">RELATED LINKS</span></span>
