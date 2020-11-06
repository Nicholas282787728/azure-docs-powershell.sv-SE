---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 6e0ff70671ceff4094d7f1a48bbebcc81398d5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574264"
---
# <span data-ttu-id="43a47-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43a47-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="43a47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43a47-102">SYNOPSIS</span></span>
<span data-ttu-id="43a47-103">Skapar en rutt filter regel för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="43a47-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43a47-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43a47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43a47-105">DESCRIPTION</span></span>
<span data-ttu-id="43a47-106">New-AzureRmRouteFilterRuleConfig cmdlet skapar en regel för flödes filter för ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="43a47-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="43a47-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43a47-107">EXAMPLES</span></span>

### <span data-ttu-id="43a47-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43a47-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="43a47-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="43a47-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="43a47-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43a47-110">PARAMETERS</span></span>

### <span data-ttu-id="43a47-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="43a47-111">-Access</span></span>
<span data-ttu-id="43a47-112">Åtkomst för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="43a47-112">Access for route filter rule.</span></span>
<span data-ttu-id="43a47-113">Giltiga värden är tillåta eller neka.</span><span class="sxs-lookup"><span data-stu-id="43a47-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="43a47-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="43a47-114">-CommunityList</span></span>
<span data-ttu-id="43a47-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="43a47-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="43a47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a47-116">-DefaultProfile</span></span>
<span data-ttu-id="43a47-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43a47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a47-118">-Force</span><span class="sxs-lookup"><span data-stu-id="43a47-118">-Force</span></span>
<span data-ttu-id="43a47-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="43a47-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="43a47-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="43a47-120">-Name</span></span>
<span data-ttu-id="43a47-121">Anger ett namn för regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="43a47-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="43a47-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="43a47-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="43a47-123">Typ av regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="43a47-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="43a47-124">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="43a47-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="43a47-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43a47-125">-Confirm</span></span>
<span data-ttu-id="43a47-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43a47-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a47-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a47-127">-WhatIf</span></span>
<span data-ttu-id="43a47-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43a47-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43a47-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43a47-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a47-130">CommonParameters</span></span>
<span data-ttu-id="43a47-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a47-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a47-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a47-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43a47-133">INPUTS</span></span>

### <span data-ttu-id="43a47-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="43a47-134">None</span></span>
<span data-ttu-id="43a47-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="43a47-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43a47-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43a47-136">OUTPUTS</span></span>

### <span data-ttu-id="43a47-137">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="43a47-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="43a47-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43a47-138">NOTES</span></span>
<span data-ttu-id="43a47-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="43a47-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="43a47-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43a47-140">RELATED LINKS</span></span>

[<span data-ttu-id="43a47-141">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43a47-141">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="43a47-142">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43a47-142">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="43a47-143">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43a47-143">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="43a47-144">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43a47-144">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

