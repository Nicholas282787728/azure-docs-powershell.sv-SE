---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930954"
---
# <span data-ttu-id="f2d83-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d83-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f2d83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2d83-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d83-103">Skapar en rutt filter regel för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="f2d83-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2d83-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2d83-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d83-106">New-AzureRmRouteFilterRuleConfig cmdlet skapar en regel för flödes filter för ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="f2d83-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="f2d83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2d83-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d83-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2d83-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f2d83-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="f2d83-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f2d83-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2d83-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d83-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="f2d83-111">-Access</span></span>
<span data-ttu-id="f2d83-112">Åtkomst för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="f2d83-112">Access for route filter rule.</span></span>
<span data-ttu-id="f2d83-113">Giltiga värden är tillåta eller neka.</span><span class="sxs-lookup"><span data-stu-id="f2d83-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="f2d83-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f2d83-114">-CommunityList</span></span>
<span data-ttu-id="f2d83-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="f2d83-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="f2d83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d83-116">-DefaultProfile</span></span>
<span data-ttu-id="f2d83-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2d83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f2d83-118">-Force</span></span>
<span data-ttu-id="f2d83-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="f2d83-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f2d83-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2d83-120">-Name</span></span>
<span data-ttu-id="f2d83-121">Anger ett namn för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="f2d83-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="f2d83-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f2d83-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="f2d83-123">Typ av regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="f2d83-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="f2d83-124">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="f2d83-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="f2d83-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2d83-125">-Confirm</span></span>
<span data-ttu-id="f2d83-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2d83-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d83-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d83-127">-WhatIf</span></span>
<span data-ttu-id="f2d83-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2d83-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2d83-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2d83-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d83-130">CommonParameters</span></span>
<span data-ttu-id="f2d83-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d83-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d83-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d83-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2d83-133">INPUTS</span></span>

## <span data-ttu-id="f2d83-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2d83-134">OUTPUTS</span></span>

### <span data-ttu-id="f2d83-135">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="f2d83-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="f2d83-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2d83-136">NOTES</span></span>
<span data-ttu-id="f2d83-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="f2d83-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f2d83-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2d83-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2d83-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d83-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f2d83-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d83-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f2d83-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d83-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f2d83-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d83-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

