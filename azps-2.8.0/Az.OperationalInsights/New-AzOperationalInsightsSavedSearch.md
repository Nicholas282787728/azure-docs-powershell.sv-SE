---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7e93042ab376ff0020067a29f9b0642e0ab04de9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928282"
---
# <span data-ttu-id="78e19-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="78e19-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="78e19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78e19-102">SYNOPSIS</span></span>
<span data-ttu-id="78e19-103">Skapar en ny Sparad sökning med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="78e19-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="78e19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78e19-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78e19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78e19-105">DESCRIPTION</span></span>
<span data-ttu-id="78e19-106">Cmdleten **New-AzOperationalInsightsSavedSearch** skapar en ny Sparad sökning med de angivna parametrarna för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="78e19-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="78e19-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78e19-107">EXAMPLES</span></span>

### <span data-ttu-id="78e19-108">Exempel 1: skapa en ny Sparad sökning</span><span class="sxs-lookup"><span data-stu-id="78e19-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="78e19-109">Det här kommandot skapar en ny Sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="78e19-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="78e19-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78e19-110">PARAMETERS</span></span>

### <span data-ttu-id="78e19-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="78e19-111">-Category</span></span>
<span data-ttu-id="78e19-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="78e19-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="78e19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e19-113">-DefaultProfile</span></span>
<span data-ttu-id="78e19-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="78e19-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78e19-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78e19-115">-DisplayName</span></span>
<span data-ttu-id="78e19-116">Anger det sparade visnings namnet för sökning.</span><span class="sxs-lookup"><span data-stu-id="78e19-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="78e19-117">-Force</span><span class="sxs-lookup"><span data-stu-id="78e19-117">-Force</span></span>
<span data-ttu-id="78e19-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="78e19-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78e19-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="78e19-119">-Query</span></span>
<span data-ttu-id="78e19-120">Anger frågeuttrycket för den sparade sökningen.</span><span class="sxs-lookup"><span data-stu-id="78e19-120">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="78e19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e19-121">-ResourceGroupName</span></span>
<span data-ttu-id="78e19-122">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="78e19-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="78e19-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="78e19-123">-SavedSearchId</span></span>
<span data-ttu-id="78e19-124">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="78e19-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="78e19-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="78e19-125">-Tag</span></span>
<span data-ttu-id="78e19-126">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="78e19-126">The saved search tags.</span></span>

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

### <span data-ttu-id="78e19-127">-Version</span><span class="sxs-lookup"><span data-stu-id="78e19-127">-Version</span></span>
<span data-ttu-id="78e19-128">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="78e19-128">Specifies the version.</span></span>

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

### <span data-ttu-id="78e19-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78e19-129">-WorkspaceName</span></span>
<span data-ttu-id="78e19-130">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="78e19-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="78e19-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78e19-131">-Confirm</span></span>
<span data-ttu-id="78e19-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78e19-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e19-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e19-133">-WhatIf</span></span>
<span data-ttu-id="78e19-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78e19-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e19-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78e19-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e19-136">CommonParameters</span></span>
<span data-ttu-id="78e19-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e19-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e19-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e19-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78e19-139">INPUTS</span></span>

### <span data-ttu-id="78e19-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78e19-140">System.String</span></span>

### <span data-ttu-id="78e19-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="78e19-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="78e19-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="78e19-142">System.Int64</span></span>

## <span data-ttu-id="78e19-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78e19-143">OUTPUTS</span></span>

### <span data-ttu-id="78e19-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="78e19-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="78e19-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78e19-145">NOTES</span></span>

## <span data-ttu-id="78e19-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78e19-146">RELATED LINKS</span></span>

[<span data-ttu-id="78e19-147">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="78e19-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


