---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755167"
---
# <span data-ttu-id="af54a-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="af54a-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="af54a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af54a-102">SYNOPSIS</span></span>
<span data-ttu-id="af54a-103">Returnerar resultatet från en fråga.</span><span class="sxs-lookup"><span data-stu-id="af54a-103">Returns the results from a query.</span></span>

## <span data-ttu-id="af54a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af54a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af54a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af54a-105">DESCRIPTION</span></span>
<span data-ttu-id="af54a-106">Cmdleten **Get-AzOperationalInsightsSavedSearchResult** returnerar resultaten från frågan som anges av Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="af54a-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="af54a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af54a-107">EXAMPLES</span></span>

### <span data-ttu-id="af54a-108">Exempel 1: få alla Sök Resultat för en sparad sökning</span><span class="sxs-lookup"><span data-stu-id="af54a-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="af54a-109">Det här kommandot får alla Sök Resultat för en sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="af54a-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="af54a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af54a-110">PARAMETERS</span></span>

### <span data-ttu-id="af54a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af54a-111">-DefaultProfile</span></span>
<span data-ttu-id="af54a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af54a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af54a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af54a-113">-ResourceGroupName</span></span>
<span data-ttu-id="af54a-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="af54a-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af54a-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="af54a-115">-SavedSearchId</span></span>
<span data-ttu-id="af54a-116">Anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="af54a-116">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af54a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af54a-117">-WorkspaceName</span></span>
<span data-ttu-id="af54a-118">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="af54a-118">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af54a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af54a-119">CommonParameters</span></span>
<span data-ttu-id="af54a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af54a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af54a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af54a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af54a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af54a-122">INPUTS</span></span>

### <span data-ttu-id="af54a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="af54a-123">System.String</span></span>

## <span data-ttu-id="af54a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af54a-124">OUTPUTS</span></span>

### <span data-ttu-id="af54a-125">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="af54a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="af54a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af54a-126">NOTES</span></span>

## <span data-ttu-id="af54a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af54a-127">RELATED LINKS</span></span>

[<span data-ttu-id="af54a-128">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="af54a-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


