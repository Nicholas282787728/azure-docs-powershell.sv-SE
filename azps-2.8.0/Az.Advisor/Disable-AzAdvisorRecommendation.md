---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745945"
---
# <span data-ttu-id="1f143-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="1f143-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="1f143-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f143-102">SYNOPSIS</span></span>
<span data-ttu-id="1f143-103">Inaktivera en Azure Advisor-rekommendation.</span><span class="sxs-lookup"><span data-stu-id="1f143-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="1f143-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f143-104">SYNTAX</span></span>

### <span data-ttu-id="1f143-105">IdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1f143-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f143-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f143-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f143-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f143-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f143-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f143-108">DESCRIPTION</span></span>
<span data-ttu-id="1f143-109">En Undertryckning för rekommendation (er) skapas gör det möjligt för en särskild rekommendation att senareläggas under en viss varaktighet eller oändligt.</span><span class="sxs-lookup"><span data-stu-id="1f143-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="1f143-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f143-110">EXAMPLES</span></span>

### <span data-ttu-id="1f143-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f143-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1f143-112">Skapa en Undertryckning för den angivna rekommendations namnet med standard-SuppressionName och standard dagar som-1.</span><span class="sxs-lookup"><span data-stu-id="1f143-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="1f143-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1f143-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1f143-114">En Undertryckning skapas för angiven rekommendation-ID.</span><span class="sxs-lookup"><span data-stu-id="1f143-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="1f143-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1f143-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1f143-116">Skapa en Undertryckning, rör dragning från Get-AzAdvisorRecommendation till Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="1f143-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="1f143-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f143-117">PARAMETERS</span></span>

### <span data-ttu-id="1f143-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f143-118">-Confirm</span></span>
<span data-ttu-id="1f143-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f143-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f143-120">-Dagar</span><span class="sxs-lookup"><span data-stu-id="1f143-120">-Days</span></span>
<span data-ttu-id="1f143-121">Dagar att inaktivera.</span><span class="sxs-lookup"><span data-stu-id="1f143-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f143-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f143-122">-DefaultProfile</span></span>
<span data-ttu-id="1f143-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f143-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f143-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f143-124">-InputObject</span></span>
<span data-ttu-id="1f143-125">PowerShell-objekttypen PsAzureAdvisorResourceRecommendationBase returneras av Get-AzAdvisorRecommendation-samtal.</span><span class="sxs-lookup"><span data-stu-id="1f143-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="1f143-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="1f143-126">-RecommendationName</span></span>
<span data-ttu-id="1f143-127">ResourceName</span><span class="sxs-lookup"><span data-stu-id="1f143-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="1f143-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f143-128">-ResourceId</span></span>
<span data-ttu-id="1f143-129">ID för rekommendationen som ska utelämnas.</span><span class="sxs-lookup"><span data-stu-id="1f143-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f143-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f143-130">-WhatIf</span></span>
<span data-ttu-id="1f143-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f143-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f143-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f143-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f143-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f143-133">CommonParameters</span></span>
<span data-ttu-id="1f143-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f143-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f143-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f143-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f143-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f143-136">INPUTS</span></span>

### <span data-ttu-id="1f143-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1f143-137">System.String</span></span>

### <span data-ttu-id="1f143-138">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="1f143-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="1f143-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f143-139">OUTPUTS</span></span>

### <span data-ttu-id="1f143-140">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="1f143-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="1f143-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f143-141">NOTES</span></span>

## <span data-ttu-id="1f143-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f143-142">RELATED LINKS</span></span>