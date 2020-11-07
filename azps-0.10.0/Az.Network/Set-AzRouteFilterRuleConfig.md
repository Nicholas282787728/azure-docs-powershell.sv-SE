---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 8ab95789b73623716edc818c8092c8c0cd58c534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924154"
---
# <span data-ttu-id="e7d7b-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7d7b-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="e7d7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d7b-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="e7d7b-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="e7d7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7d7b-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d7b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d7b-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="e7d7b-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e7d7b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d7b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7d7b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e7d7b-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="e7d7b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e7d7b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d7b-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="e7d7b-111">-Access</span></span>
<span data-ttu-id="e7d7b-112">Åtkomst typen för regeln.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-112">The access type of the rule.</span></span>
<span data-ttu-id="e7d7b-113">Möjliga värden är: ' Allow ', ' neka '</span><span class="sxs-lookup"><span data-stu-id="e7d7b-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="e7d7b-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="e7d7b-114">-CommunityList</span></span>
<span data-ttu-id="e7d7b-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="e7d7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d7b-116">-DefaultProfile</span></span>
<span data-ttu-id="e7d7b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d7b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d7b-118">-Force</span></span>
<span data-ttu-id="e7d7b-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="e7d7b-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="e7d7b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7d7b-120">-Name</span></span>
<span data-ttu-id="e7d7b-121">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="e7d7b-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-122">-RouteFilter</span></span>
<span data-ttu-id="e7d7b-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-123">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d7b-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="e7d7b-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="e7d7b-125">Regel typen för flödes filter regeln.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="e7d7b-126">Möjliga värden är: ' community '</span><span class="sxs-lookup"><span data-stu-id="e7d7b-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="e7d7b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7d7b-127">-Confirm</span></span>
<span data-ttu-id="e7d7b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d7b-129">-WhatIf</span></span>
<span data-ttu-id="e7d7b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7d7b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d7b-132">CommonParameters</span></span>
<span data-ttu-id="e7d7b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d7b-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d7b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d7b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7d7b-135">INPUTS</span></span>

### <span data-ttu-id="e7d7b-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e7d7b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7d7b-137">OUTPUTS</span></span>

### <span data-ttu-id="e7d7b-138">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7d7b-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e7d7b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7d7b-139">NOTES</span></span>

## <span data-ttu-id="e7d7b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7d7b-140">RELATED LINKS</span></span>

