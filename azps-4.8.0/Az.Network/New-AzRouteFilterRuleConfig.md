---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259282"
---
# <span data-ttu-id="79f23-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79f23-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="79f23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79f23-102">SYNOPSIS</span></span>
<span data-ttu-id="79f23-103">Skapar en rutt filter regel för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="79f23-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="79f23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79f23-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79f23-105">DESCRIPTION</span></span>
<span data-ttu-id="79f23-106">New-AzRouteFilterRuleConfig cmdlet skapar en regel för flödes filter för ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="79f23-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="79f23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79f23-107">EXAMPLES</span></span>

### <span data-ttu-id="79f23-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79f23-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="79f23-109">Kommandot skapar en ny regel för flödes filter och lagrar den i variabeln $rule 1.</span><span class="sxs-lookup"><span data-stu-id="79f23-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="79f23-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79f23-110">PARAMETERS</span></span>

### <span data-ttu-id="79f23-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="79f23-111">-Access</span></span>
<span data-ttu-id="79f23-112">Åtkomst för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="79f23-112">Access for route filter rule.</span></span>
<span data-ttu-id="79f23-113">Giltiga värden är tillåta eller neka.</span><span class="sxs-lookup"><span data-stu-id="79f23-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f23-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="79f23-114">-CommunityList</span></span>
<span data-ttu-id="79f23-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="79f23-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="79f23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f23-116">-DefaultProfile</span></span>
<span data-ttu-id="79f23-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79f23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79f23-118">-Force</span><span class="sxs-lookup"><span data-stu-id="79f23-118">-Force</span></span>
<span data-ttu-id="79f23-119">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="79f23-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="79f23-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="79f23-120">-Name</span></span>
<span data-ttu-id="79f23-121">Anger ett namn för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="79f23-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="79f23-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="79f23-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="79f23-123">Typ av regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="79f23-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="79f23-124">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="79f23-124">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f23-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79f23-125">-Confirm</span></span>
<span data-ttu-id="79f23-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79f23-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f23-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f23-127">-WhatIf</span></span>
<span data-ttu-id="79f23-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79f23-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79f23-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79f23-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f23-130">CommonParameters</span></span>
<span data-ttu-id="79f23-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f23-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f23-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f23-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79f23-133">INPUTS</span></span>

### <span data-ttu-id="79f23-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="79f23-134">None</span></span>

## <span data-ttu-id="79f23-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79f23-135">OUTPUTS</span></span>

### <span data-ttu-id="79f23-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="79f23-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="79f23-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79f23-137">NOTES</span></span>
<span data-ttu-id="79f23-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="79f23-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="79f23-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79f23-139">RELATED LINKS</span></span>

[<span data-ttu-id="79f23-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79f23-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="79f23-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79f23-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="79f23-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79f23-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="79f23-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79f23-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="79f23-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="79f23-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="79f23-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="79f23-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="79f23-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="79f23-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="79f23-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="79f23-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
