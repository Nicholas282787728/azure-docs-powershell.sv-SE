---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416627"
---
# <span data-ttu-id="20912-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="20912-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="20912-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20912-102">SYNOPSIS</span></span>
<span data-ttu-id="20912-103">Returnerar alla sparade sökningar för en viss arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20912-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="20912-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20912-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20912-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20912-105">DESCRIPTION</span></span>
<span data-ttu-id="20912-106">Cmdleten **Get-AzOperationalInsightsSavedSearch** returnerar alla sparade sökningar för en viss arbets yta i den angivna resurs gruppen om du inte anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="20912-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="20912-107">Om du anger ett sparat Sök-ID returneras den sparade sökningen för detta ID.</span><span class="sxs-lookup"><span data-stu-id="20912-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="20912-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20912-108">EXAMPLES</span></span>

### <span data-ttu-id="20912-109">Exempel 1: Hämta alla sparade sökningar för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="20912-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="20912-110">Med det här kommandot får alla sparade resurser associerade till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20912-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="20912-111">Exempel 2: Hämta en specifik Sparad sökning utifrån ID</span><span class="sxs-lookup"><span data-stu-id="20912-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="20912-112">Det här kommandot får en specifik Sparad sökning baserat på dess ID.</span><span class="sxs-lookup"><span data-stu-id="20912-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="20912-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20912-113">PARAMETERS</span></span>

### <span data-ttu-id="20912-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20912-114">-DefaultProfile</span></span>
<span data-ttu-id="20912-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20912-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20912-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20912-116">-ResourceGroupName</span></span>
<span data-ttu-id="20912-117">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20912-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="20912-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="20912-118">-SavedSearchId</span></span>
<span data-ttu-id="20912-119">Anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="20912-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20912-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20912-120">-WorkspaceName</span></span>
<span data-ttu-id="20912-121">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20912-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="20912-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20912-122">CommonParameters</span></span>
<span data-ttu-id="20912-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20912-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20912-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20912-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20912-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20912-125">INPUTS</span></span>

### <span data-ttu-id="20912-126">System. String</span><span class="sxs-lookup"><span data-stu-id="20912-126">System.String</span></span>

## <span data-ttu-id="20912-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20912-127">OUTPUTS</span></span>

### <span data-ttu-id="20912-128">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="20912-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="20912-129">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="20912-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="20912-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20912-130">NOTES</span></span>

## <span data-ttu-id="20912-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20912-131">RELATED LINKS</span></span>

[<span data-ttu-id="20912-132">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="20912-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


