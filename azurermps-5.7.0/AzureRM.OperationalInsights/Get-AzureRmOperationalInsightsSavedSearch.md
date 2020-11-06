---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575586"
---
# <span data-ttu-id="20f92-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="20f92-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="20f92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20f92-102">SYNOPSIS</span></span>
<span data-ttu-id="20f92-103">Returnerar alla sparade sökningar för en viss arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20f92-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20f92-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20f92-105">DESCRIPTION</span></span>
<span data-ttu-id="20f92-106">Cmdleten **Get-AzureRmOperationalInsightsSavedSearch** returnerar alla sparade sökningar för en viss arbets yta i den angivna resurs gruppen om du inte anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="20f92-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="20f92-107">Om du anger ett sparat Sök-ID returneras den sparade sökningen för detta ID.</span><span class="sxs-lookup"><span data-stu-id="20f92-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="20f92-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20f92-108">EXAMPLES</span></span>

### <span data-ttu-id="20f92-109">Exempel 1: Hämta alla sparade sökningar för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="20f92-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="20f92-110">Med det här kommandot får alla sparade resurser associerade till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20f92-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="20f92-111">Exempel 2: Hämta en specifik Sparad sökning utifrån ID</span><span class="sxs-lookup"><span data-stu-id="20f92-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="20f92-112">Det här kommandot får en specifik Sparad sökning baserat på dess ID.</span><span class="sxs-lookup"><span data-stu-id="20f92-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="20f92-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20f92-113">PARAMETERS</span></span>

### <span data-ttu-id="20f92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f92-114">-DefaultProfile</span></span>
<span data-ttu-id="20f92-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20f92-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20f92-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f92-116">-ResourceGroupName</span></span>
<span data-ttu-id="20f92-117">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20f92-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="20f92-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="20f92-118">-SavedSearchId</span></span>
<span data-ttu-id="20f92-119">Anger ett sparat Sök-ID.</span><span class="sxs-lookup"><span data-stu-id="20f92-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f92-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20f92-120">-WorkspaceName</span></span>
<span data-ttu-id="20f92-121">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="20f92-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="20f92-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f92-122">CommonParameters</span></span>
<span data-ttu-id="20f92-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f92-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f92-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f92-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f92-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20f92-125">INPUTS</span></span>

### <span data-ttu-id="20f92-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="20f92-126">None</span></span>
<span data-ttu-id="20f92-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="20f92-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20f92-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20f92-128">OUTPUTS</span></span>

### <span data-ttu-id="20f92-129">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="20f92-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="20f92-130">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="20f92-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="20f92-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20f92-131">NOTES</span></span>

## <span data-ttu-id="20f92-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20f92-132">RELATED LINKS</span></span>

[<span data-ttu-id="20f92-133">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="20f92-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


