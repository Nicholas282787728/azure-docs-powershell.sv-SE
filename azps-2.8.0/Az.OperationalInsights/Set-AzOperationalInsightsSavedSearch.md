---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928517"
---
# <span data-ttu-id="40932-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="40932-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="40932-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40932-102">SYNOPSIS</span></span>
<span data-ttu-id="40932-103">Uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="40932-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="40932-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40932-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40932-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40932-105">DESCRIPTION</span></span>
<span data-ttu-id="40932-106">Cmdleten **set-AzOperationalInsightsSavedSearch** uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="40932-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="40932-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40932-107">EXAMPLES</span></span>

### <span data-ttu-id="40932-108">Exempel 1: anger en sparad sökning med uppdaterade egenskaper</span><span class="sxs-lookup"><span data-stu-id="40932-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="40932-109">Det här kommandot ställer in en sparad sökning med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="40932-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="40932-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40932-110">PARAMETERS</span></span>

### <span data-ttu-id="40932-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="40932-111">-Category</span></span>
<span data-ttu-id="40932-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="40932-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40932-113">-DefaultProfile</span></span>
<span data-ttu-id="40932-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40932-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40932-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="40932-115">-DisplayName</span></span>
<span data-ttu-id="40932-116">Anger visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="40932-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="40932-117">-ETag</span></span>
<span data-ttu-id="40932-118">Anger ETag-namnet.</span><span class="sxs-lookup"><span data-stu-id="40932-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="40932-119">-Query</span></span>
<span data-ttu-id="40932-120">Anger frågans namn.</span><span class="sxs-lookup"><span data-stu-id="40932-120">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40932-121">-ResourceGroupName</span></span>
<span data-ttu-id="40932-122">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="40932-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="40932-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="40932-123">-SavedSearchId</span></span>
<span data-ttu-id="40932-124">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="40932-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="40932-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="40932-125">-Tag</span></span>
<span data-ttu-id="40932-126">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="40932-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-127">-Version</span><span class="sxs-lookup"><span data-stu-id="40932-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40932-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="40932-128">-WorkspaceName</span></span>
<span data-ttu-id="40932-129">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="40932-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="40932-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40932-130">CommonParameters</span></span>
<span data-ttu-id="40932-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40932-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40932-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40932-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40932-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40932-133">INPUTS</span></span>

### <span data-ttu-id="40932-134">System. String</span><span class="sxs-lookup"><span data-stu-id="40932-134">System.String</span></span>

### <span data-ttu-id="40932-135">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="40932-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="40932-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="40932-136">System.Int64</span></span>

## <span data-ttu-id="40932-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40932-137">OUTPUTS</span></span>

### <span data-ttu-id="40932-138">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="40932-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="40932-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40932-139">NOTES</span></span>

## <span data-ttu-id="40932-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40932-140">RELATED LINKS</span></span>

[<span data-ttu-id="40932-141">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="40932-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


