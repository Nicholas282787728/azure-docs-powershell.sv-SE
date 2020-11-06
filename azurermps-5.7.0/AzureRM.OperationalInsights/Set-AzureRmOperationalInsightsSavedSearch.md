---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: fdfe52151346bbf173226213c9450484d49fe040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574868"
---
# <span data-ttu-id="4a8c2-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4a8c2-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="4a8c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8c2-103">Uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a8c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a8c2-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a8c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a8c2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8c2-106">Cmdleten **set-AzureRmOperationalInsightsSavedSearch** uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="4a8c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a8c2-107">EXAMPLES</span></span>

### <span data-ttu-id="4a8c2-108">Exempel 1: anger en sparad sökning med uppdaterade egenskaper</span><span class="sxs-lookup"><span data-stu-id="4a8c2-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="4a8c2-109">Det här kommandot ställer in en sparad sökning med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="4a8c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a8c2-110">PARAMETERS</span></span>

### <span data-ttu-id="4a8c2-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="4a8c2-111">-Category</span></span>
<span data-ttu-id="4a8c2-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8c2-113">-DefaultProfile</span></span>
<span data-ttu-id="4a8c2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4a8c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a8c2-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4a8c2-115">-DisplayName</span></span>
<span data-ttu-id="4a8c2-116">Anger visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-116">Specifies the display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="4a8c2-117">-ETag</span></span>
<span data-ttu-id="4a8c2-118">Anger ETag-namnet.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-118">Specifies the ETag name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="4a8c2-119">-Query</span></span>
<span data-ttu-id="4a8c2-120">Anger frågans namn.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a8c2-122">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="4a8c2-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="4a8c2-123">-SavedSearchId</span></span>
<span data-ttu-id="4a8c2-124">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="4a8c2-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4a8c2-125">-Tag</span></span>
<span data-ttu-id="4a8c2-126">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-127">-Version</span><span class="sxs-lookup"><span data-stu-id="4a8c2-127">-Version</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8c2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4a8c2-128">-WorkspaceName</span></span>
<span data-ttu-id="4a8c2-129">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4a8c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8c2-130">CommonParameters</span></span>
<span data-ttu-id="4a8c2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8c2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8c2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8c2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a8c2-133">INPUTS</span></span>

### <span data-ttu-id="4a8c2-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="4a8c2-134">None</span></span>
<span data-ttu-id="4a8c2-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4a8c2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a8c2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a8c2-136">OUTPUTS</span></span>

## <span data-ttu-id="4a8c2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a8c2-137">NOTES</span></span>

## <span data-ttu-id="4a8c2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a8c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="4a8c2-139">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="4a8c2-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


