---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: dc6005c77a72b3965f2fca670c1d729fc7c7bd07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918671"
---
# <span data-ttu-id="7d2c7-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7d2c7-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="7d2c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2c7-103">Skapar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="7d2c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d2c7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2c7-106">Cmdleten **New-AzApplicationGatewayFirewallPolicy** skapar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="7d2c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2c7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d2c7-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="7d2c7-109">Det här kommandot skapar en ny Azure Application Gateway-brandvägg med namnet "wafResource1" i resurs gruppen "RG1" i plats "väst" med anpassade regler definierade i variabeln $customRule</span><span class="sxs-lookup"><span data-stu-id="7d2c7-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="7d2c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d2c7-110">PARAMETERS</span></span>

### <span data-ttu-id="7d2c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d2c7-111">-AsJob</span></span>
<span data-ttu-id="7d2c7-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7d2c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d2c7-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="7d2c7-113">-CustomRule</span></span>
<span data-ttu-id="7d2c7-114">Listan med CustomRules</span><span class="sxs-lookup"><span data-stu-id="7d2c7-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="7d2c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2c7-115">-DefaultProfile</span></span>
<span data-ttu-id="7d2c7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d2c7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7d2c7-117">-Force</span></span>
<span data-ttu-id="7d2c7-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="7d2c7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7d2c7-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7d2c7-119">-Location</span></span>
<span data-ttu-id="7d2c7-120">plats.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-120">location.</span></span>

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

### <span data-ttu-id="7d2c7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d2c7-121">-Name</span></span>
<span data-ttu-id="7d2c7-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-122">The resource name.</span></span>

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

### <span data-ttu-id="7d2c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d2c7-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-124">The resource group name.</span></span>

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

### <span data-ttu-id="7d2c7-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7d2c7-125">-Tag</span></span>
<span data-ttu-id="7d2c7-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7d2c7-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d2c7-127">-Confirm</span></span>
<span data-ttu-id="7d2c7-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2c7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2c7-129">-WhatIf</span></span>
<span data-ttu-id="7d2c7-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2c7-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2c7-132">CommonParameters</span></span>
<span data-ttu-id="7d2c7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2c7-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2c7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2c7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d2c7-135">INPUTS</span></span>

### <span data-ttu-id="7d2c7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c7-136">System.String</span></span>

### <span data-ttu-id="7d2c7-137">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="7d2c7-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="7d2c7-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7d2c7-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7d2c7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d2c7-139">OUTPUTS</span></span>

### <span data-ttu-id="7d2c7-140">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7d2c7-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="7d2c7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d2c7-141">NOTES</span></span>

## <span data-ttu-id="7d2c7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d2c7-142">RELATED LINKS</span></span>
