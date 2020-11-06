---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575951"
---
# <span data-ttu-id="210e3-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210e3-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="210e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="210e3-102">SYNOPSIS</span></span>
<span data-ttu-id="210e3-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="210e3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="210e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="210e3-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="210e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="210e3-105">DESCRIPTION</span></span>
<span data-ttu-id="210e3-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="210e3-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="210e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="210e3-107">EXAMPLES</span></span>

### <span data-ttu-id="210e3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="210e3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="210e3-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="210e3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="210e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="210e3-110">PARAMETERS</span></span>

### <span data-ttu-id="210e3-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="210e3-111">-Access</span></span>
<span data-ttu-id="210e3-112">Åtkomst typen för regeln.</span><span class="sxs-lookup"><span data-stu-id="210e3-112">The access type of the rule.</span></span>
<span data-ttu-id="210e3-113">Möjliga värden är: ' Allow ', ' neka '</span><span class="sxs-lookup"><span data-stu-id="210e3-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="210e3-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="210e3-114">-CommunityList</span></span>
<span data-ttu-id="210e3-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="210e3-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="210e3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="210e3-116">-Force</span></span>
<span data-ttu-id="210e3-117">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="210e3-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="210e3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="210e3-118">-Name</span></span>
<span data-ttu-id="210e3-119">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="210e3-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="210e3-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="210e3-120">-RouteFilter</span></span>
<span data-ttu-id="210e3-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="210e3-121">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="210e3-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="210e3-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="210e3-123">Regel typen för flödes filter regeln.</span><span class="sxs-lookup"><span data-stu-id="210e3-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="210e3-124">Möjliga värden är: ' community '</span><span class="sxs-lookup"><span data-stu-id="210e3-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="210e3-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="210e3-125">-Confirm</span></span>
<span data-ttu-id="210e3-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="210e3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="210e3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="210e3-127">-WhatIf</span></span>
<span data-ttu-id="210e3-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="210e3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="210e3-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="210e3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="210e3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210e3-130">-DefaultProfile</span></span>
<span data-ttu-id="210e3-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="210e3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="210e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210e3-132">CommonParameters</span></span>
<span data-ttu-id="210e3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210e3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="210e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210e3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="210e3-135">INPUTS</span></span>

### <span data-ttu-id="210e3-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="210e3-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="210e3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="210e3-137">OUTPUTS</span></span>

### <span data-ttu-id="210e3-138">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="210e3-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="210e3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="210e3-139">NOTES</span></span>

## <span data-ttu-id="210e3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="210e3-140">RELATED LINKS</span></span>

