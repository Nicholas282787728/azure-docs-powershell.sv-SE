---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102646"
---
# <span data-ttu-id="d69ee-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d69ee-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="d69ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d69ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d69ee-103">Skapar en ny Sparad sökning med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="d69ee-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="d69ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d69ee-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d69ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d69ee-106">Cmdleten **New-AzOperationalInsightsSavedSearch** skapar en ny Sparad sökning med de angivna parametrarna för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d69ee-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="d69ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d69ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d69ee-108">Exempel 1: skapa en ny Sparad sökning</span><span class="sxs-lookup"><span data-stu-id="d69ee-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="d69ee-109">Det här kommandot skapar en ny Sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="d69ee-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="d69ee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d69ee-110">PARAMETERS</span></span>

### <span data-ttu-id="d69ee-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="d69ee-111">-Category</span></span>
<span data-ttu-id="d69ee-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="d69ee-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="d69ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69ee-113">-DefaultProfile</span></span>
<span data-ttu-id="d69ee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d69ee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d69ee-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d69ee-115">-DisplayName</span></span>
<span data-ttu-id="d69ee-116">Anger det sparade visnings namnet för sökning.</span><span class="sxs-lookup"><span data-stu-id="d69ee-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="d69ee-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d69ee-117">-Force</span></span>
<span data-ttu-id="d69ee-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d69ee-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69ee-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="d69ee-119">-FunctionAlias</span></span>
<span data-ttu-id="d69ee-120">Funktionen alias om Query fungerar som en funktion.</span><span class="sxs-lookup"><span data-stu-id="d69ee-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69ee-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="d69ee-121">-FunctionParameter</span></span>
<span data-ttu-id="d69ee-122">Valfria funktions parametrar om Query fungerar som en funktion.</span><span class="sxs-lookup"><span data-stu-id="d69ee-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="d69ee-123">Värdet ska vara i följande format: ' param-name1: Type1 = default_value1, param-name2: TYPE2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="d69ee-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="d69ee-124">Fler exempel och en lämplig syntax finns i https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="d69ee-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69ee-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="d69ee-125">-Query</span></span>
<span data-ttu-id="d69ee-126">Anger frågeuttrycket för den sparade sökningen.</span><span class="sxs-lookup"><span data-stu-id="d69ee-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="d69ee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69ee-127">-ResourceGroupName</span></span>
<span data-ttu-id="d69ee-128">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d69ee-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="d69ee-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d69ee-129">-SavedSearchId</span></span>
<span data-ttu-id="d69ee-130">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="d69ee-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="d69ee-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d69ee-131">-Tag</span></span>
<span data-ttu-id="d69ee-132">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="d69ee-132">The saved search tags.</span></span>

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

### <span data-ttu-id="d69ee-133">-Version</span><span class="sxs-lookup"><span data-stu-id="d69ee-133">-Version</span></span>
<span data-ttu-id="d69ee-134">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="d69ee-134">Specifies the version.</span></span>

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

### <span data-ttu-id="d69ee-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d69ee-135">-WorkspaceName</span></span>
<span data-ttu-id="d69ee-136">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="d69ee-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d69ee-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d69ee-137">-Confirm</span></span>
<span data-ttu-id="d69ee-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d69ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69ee-139">-WhatIf</span></span>
<span data-ttu-id="d69ee-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d69ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69ee-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d69ee-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69ee-142">CommonParameters</span></span>
<span data-ttu-id="d69ee-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69ee-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d69ee-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69ee-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d69ee-145">INPUTS</span></span>

### <span data-ttu-id="d69ee-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d69ee-146">System.String</span></span>

### <span data-ttu-id="d69ee-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d69ee-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d69ee-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="d69ee-148">System.Int64</span></span>

## <span data-ttu-id="d69ee-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d69ee-149">OUTPUTS</span></span>

### <span data-ttu-id="d69ee-150">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="d69ee-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="d69ee-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d69ee-151">NOTES</span></span>

## <span data-ttu-id="d69ee-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d69ee-152">RELATED LINKS</span></span>

[<span data-ttu-id="d69ee-153">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="d69ee-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


