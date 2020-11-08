---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101269"
---
# <span data-ttu-id="a1579-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="a1579-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="a1579-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1579-102">SYNOPSIS</span></span>
<span data-ttu-id="a1579-103">Möjliggör Azure Advisor-rekommendation (er).</span><span class="sxs-lookup"><span data-stu-id="a1579-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="a1579-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1579-104">SYNTAX</span></span>

### <span data-ttu-id="a1579-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a1579-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1579-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1579-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1579-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1579-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1579-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1579-108">DESCRIPTION</span></span>
<span data-ttu-id="a1579-109">Denna cmdlet aktiverar en tidigare undertryckt rekommendation.</span><span class="sxs-lookup"><span data-stu-id="a1579-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="a1579-110">Du kan också ta bort alla undervisningar som är kopplade till en rekommendation.</span><span class="sxs-lookup"><span data-stu-id="a1579-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="a1579-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1579-111">EXAMPLES</span></span>

### <span data-ttu-id="a1579-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1579-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="a1579-113">Tar bort alla undertrycken för den rekommendationen med namnet "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="a1579-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="a1579-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a1579-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="a1579-115">Tar bort alla undervisningar för de rekommendationer som skickas från pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1579-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="a1579-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1579-116">PARAMETERS</span></span>

### <span data-ttu-id="a1579-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1579-117">-Confirm</span></span>
<span data-ttu-id="a1579-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1579-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1579-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1579-119">-DefaultProfile</span></span>
<span data-ttu-id="a1579-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1579-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1579-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1579-121">-InputObject</span></span>
<span data-ttu-id="a1579-122">PowerShell-objekttypen PsAzureAdvisorResourceRecommendationBase returneras av Get-AzAdvisorRecommendation-samtal.</span><span class="sxs-lookup"><span data-stu-id="a1579-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1579-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="a1579-123">-RecommendationName</span></span>
<span data-ttu-id="a1579-124">ResourceName i rekommendationen.</span><span class="sxs-lookup"><span data-stu-id="a1579-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1579-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1579-125">-ResourceId</span></span>
<span data-ttu-id="a1579-126">ID för rekommendationen som ska utelämnas.</span><span class="sxs-lookup"><span data-stu-id="a1579-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1579-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1579-127">-WhatIf</span></span>
<span data-ttu-id="a1579-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1579-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1579-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1579-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1579-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1579-130">CommonParameters</span></span>
<span data-ttu-id="a1579-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1579-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a1579-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1579-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1579-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1579-133">INPUTS</span></span>

### <span data-ttu-id="a1579-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a1579-134">System.String</span></span>

### <span data-ttu-id="a1579-135">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="a1579-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a1579-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1579-136">OUTPUTS</span></span>

### <span data-ttu-id="a1579-137">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="a1579-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a1579-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1579-138">NOTES</span></span>

## <span data-ttu-id="a1579-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1579-139">RELATED LINKS</span></span>
