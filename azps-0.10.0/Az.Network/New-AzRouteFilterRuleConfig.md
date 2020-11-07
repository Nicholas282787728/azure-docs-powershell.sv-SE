---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922098"
---
# <span data-ttu-id="2f0a8-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f0a8-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2f0a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0a8-103">Skapar en rutt filter regel för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="2f0a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f0a8-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0a8-106">New-AzRouteFilterRuleConfig cmdlet skapar en regel för flödes filter för ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="2f0a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f0a8-107">EXAMPLES</span></span>

### <span data-ttu-id="2f0a8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f0a8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2f0a8-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="2f0a8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2f0a8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f0a8-110">PARAMETERS</span></span>

### <span data-ttu-id="2f0a8-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="2f0a8-111">-Access</span></span>
<span data-ttu-id="2f0a8-112">Åtkomst för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-112">Access for route filter rule.</span></span>
<span data-ttu-id="2f0a8-113">Giltiga värden är tillåta eller neka.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="2f0a8-114">-CommunityList</span></span>
<span data-ttu-id="2f0a8-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="2f0a8-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0a8-116">-DefaultProfile</span></span>
<span data-ttu-id="2f0a8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2f0a8-118">-Force</span></span>
<span data-ttu-id="2f0a8-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="2f0a8-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="2f0a8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f0a8-120">-Name</span></span>
<span data-ttu-id="2f0a8-121">Anger ett namn för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="2f0a8-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="2f0a8-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="2f0a8-123">Typ av regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="2f0a8-124">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="2f0a8-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f0a8-125">-Confirm</span></span>
<span data-ttu-id="2f0a8-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0a8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0a8-127">-WhatIf</span></span>
<span data-ttu-id="2f0a8-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f0a8-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0a8-130">CommonParameters</span></span>
<span data-ttu-id="2f0a8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0a8-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0a8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0a8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f0a8-133">INPUTS</span></span>

## <span data-ttu-id="2f0a8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f0a8-134">OUTPUTS</span></span>

### <span data-ttu-id="2f0a8-135">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="2f0a8-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="2f0a8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f0a8-136">NOTES</span></span>
<span data-ttu-id="2f0a8-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="2f0a8-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2f0a8-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f0a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="2f0a8-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f0a8-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2f0a8-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f0a8-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2f0a8-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f0a8-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2f0a8-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f0a8-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

