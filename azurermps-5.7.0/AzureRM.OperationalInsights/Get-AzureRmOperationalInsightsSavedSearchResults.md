---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755593"
---
# <span data-ttu-id="3b569-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="3b569-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="3b569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b569-102">SYNOPSIS</span></span>
<span data-ttu-id="3b569-103">Returnerar resultatet från en fråga.</span><span class="sxs-lookup"><span data-stu-id="3b569-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b569-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b569-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b569-105">DESCRIPTION</span></span>
<span data-ttu-id="3b569-106">Cmdleten **Get-AzureRmOperationalInsightsSavedSearchResults** returnerar resultaten från frågan som anges av Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="3b569-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="3b569-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b569-107">EXAMPLES</span></span>

### <span data-ttu-id="3b569-108">Exempel 1: få alla Sök Resultat för en sparad sökning</span><span class="sxs-lookup"><span data-stu-id="3b569-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="3b569-109">Det här kommandot får alla Sök Resultat för en sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="3b569-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="3b569-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b569-110">PARAMETERS</span></span>

### <span data-ttu-id="3b569-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b569-111">-DefaultProfile</span></span>
<span data-ttu-id="3b569-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3b569-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b569-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b569-113">-ResourceGroupName</span></span>
<span data-ttu-id="3b569-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3b569-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b569-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3b569-115">-SavedSearchId</span></span>
<span data-ttu-id="3b569-116">Anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="3b569-116">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b569-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b569-117">-WorkspaceName</span></span>
<span data-ttu-id="3b569-118">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3b569-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b569-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b569-119">CommonParameters</span></span>
<span data-ttu-id="3b569-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b569-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b569-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b569-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b569-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b569-122">INPUTS</span></span>

### <span data-ttu-id="3b569-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b569-123">None</span></span>
<span data-ttu-id="3b569-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3b569-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b569-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b569-125">OUTPUTS</span></span>

### <span data-ttu-id="3b569-126">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="3b569-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="3b569-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b569-127">NOTES</span></span>

## <span data-ttu-id="3b569-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b569-128">RELATED LINKS</span></span>

[<span data-ttu-id="3b569-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="3b569-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


