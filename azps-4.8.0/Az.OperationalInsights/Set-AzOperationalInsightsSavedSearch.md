---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260671"
---
# <span data-ttu-id="abb17-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="abb17-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="abb17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abb17-102">SYNOPSIS</span></span>
<span data-ttu-id="abb17-103">Uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="abb17-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="abb17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abb17-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abb17-105">DESCRIPTION</span></span>
<span data-ttu-id="abb17-106">Cmdleten **set-AzOperationalInsightsSavedSearch** uppdaterar en sparad sökning som redan finns.</span><span class="sxs-lookup"><span data-stu-id="abb17-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="abb17-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abb17-107">EXAMPLES</span></span>

### <span data-ttu-id="abb17-108">Exempel 1: anger en sparad sökning med uppdaterade egenskaper</span><span class="sxs-lookup"><span data-stu-id="abb17-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="abb17-109">Det här kommandot ställer in en sparad sökning med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="abb17-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="abb17-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abb17-110">PARAMETERS</span></span>

### <span data-ttu-id="abb17-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="abb17-111">-Category</span></span>
<span data-ttu-id="abb17-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="abb17-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="abb17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb17-113">-DefaultProfile</span></span>
<span data-ttu-id="abb17-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="abb17-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abb17-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="abb17-115">-DisplayName</span></span>
<span data-ttu-id="abb17-116">Anger visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="abb17-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="abb17-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="abb17-117">-ETag</span></span>
<span data-ttu-id="abb17-118">Anger ETag-namnet.</span><span class="sxs-lookup"><span data-stu-id="abb17-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="abb17-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="abb17-119">-FunctionAlias</span></span>
<span data-ttu-id="abb17-120">Funktionen alias om Query fungerar som en funktion.</span><span class="sxs-lookup"><span data-stu-id="abb17-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb17-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="abb17-121">-FunctionParameter</span></span>
<span data-ttu-id="abb17-122">Valfria funktions parametrar om Query fungerar som en funktion.</span><span class="sxs-lookup"><span data-stu-id="abb17-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="abb17-123">Värdet ska vara i följande format: ' param-name1: Type1 = default_value1, param-name2: TYPE2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="abb17-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="abb17-124">Fler exempel och en lämplig syntax finns i https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="abb17-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb17-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="abb17-125">-Query</span></span>
<span data-ttu-id="abb17-126">Anger frågans namn.</span><span class="sxs-lookup"><span data-stu-id="abb17-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="abb17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb17-127">-ResourceGroupName</span></span>
<span data-ttu-id="abb17-128">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="abb17-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="abb17-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="abb17-129">-SavedSearchId</span></span>
<span data-ttu-id="abb17-130">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="abb17-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="abb17-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abb17-131">-Tag</span></span>
<span data-ttu-id="abb17-132">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="abb17-132">The saved search tags.</span></span>

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

### <span data-ttu-id="abb17-133">-Version</span><span class="sxs-lookup"><span data-stu-id="abb17-133">-Version</span></span>
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

### <span data-ttu-id="abb17-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="abb17-134">-WorkspaceName</span></span>
<span data-ttu-id="abb17-135">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="abb17-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="abb17-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb17-136">CommonParameters</span></span>
<span data-ttu-id="abb17-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb17-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb17-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abb17-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb17-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abb17-139">INPUTS</span></span>

### <span data-ttu-id="abb17-140">System. String</span><span class="sxs-lookup"><span data-stu-id="abb17-140">System.String</span></span>

### <span data-ttu-id="abb17-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="abb17-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="abb17-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="abb17-142">System.Int64</span></span>

## <span data-ttu-id="abb17-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abb17-143">OUTPUTS</span></span>

### <span data-ttu-id="abb17-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="abb17-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="abb17-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abb17-145">NOTES</span></span>

## <span data-ttu-id="abb17-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abb17-146">RELATED LINKS</span></span>

[<span data-ttu-id="abb17-147">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="abb17-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

