---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399491"
---
# <span data-ttu-id="4ace6-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ace6-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="4ace6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ace6-102">SYNOPSIS</span></span>
<span data-ttu-id="4ace6-103">Hämtar en lista med rekommendationer för Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="4ace6-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="4ace6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ace6-104">SYNTAX</span></span>

### <span data-ttu-id="4ace6-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4ace6-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ace6-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ace6-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ace6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ace6-107">DESCRIPTION</span></span>
<span data-ttu-id="4ace6-108">Erhåller listan med rekommendationer för Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="4ace6-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="4ace6-109">Kan filtreras efter kategori, resurs-ID, namn etc.</span><span class="sxs-lookup"><span data-stu-id="4ace6-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="4ace6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ace6-110">EXAMPLES</span></span>

### <span data-ttu-id="4ace6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ace6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="4ace6-112">Hämtar en lista över alla rekommendationer.</span><span class="sxs-lookup"><span data-stu-id="4ace6-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="4ace6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ace6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="4ace6-114">Hämtar listan över alla rekommendationer som filtrerats efter kategori prestanda.</span><span class="sxs-lookup"><span data-stu-id="4ace6-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="4ace6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ace6-115">PARAMETERS</span></span>

### <span data-ttu-id="4ace6-116">-Kategori</span><span class="sxs-lookup"><span data-stu-id="4ace6-116">-Category</span></span>
<span data-ttu-id="4ace6-117">Rekommendations kategori</span><span class="sxs-lookup"><span data-stu-id="4ace6-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ace6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ace6-118">-DefaultProfile</span></span>
<span data-ttu-id="4ace6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ace6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ace6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ace6-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ace6-121">Rekommendationens ResourceGroup-namn</span><span class="sxs-lookup"><span data-stu-id="4ace6-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ace6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ace6-122">-ResourceId</span></span>
<span data-ttu-id="4ace6-123">ResourceId för rekommendationen</span><span class="sxs-lookup"><span data-stu-id="4ace6-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="4ace6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ace6-124">CommonParameters</span></span>
<span data-ttu-id="4ace6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ace6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ace6-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ace6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ace6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ace6-127">INPUTS</span></span>

### <span data-ttu-id="4ace6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ace6-128">System.String</span></span>

## <span data-ttu-id="4ace6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ace6-129">OUTPUTS</span></span>

### <span data-ttu-id="4ace6-130">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="4ace6-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="4ace6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ace6-131">NOTES</span></span>

## <span data-ttu-id="4ace6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ace6-132">RELATED LINKS</span></span>
