---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 247589f50028fb8d4cebf78f0ad45bb2124e43cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576138"
---
# <span data-ttu-id="cf7d9-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cf7d9-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="cf7d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7d9-103">Skapar en ny Sparad sökning med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf7d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf7d9-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf7d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf7d9-105">DESCRIPTION</span></span>
<span data-ttu-id="cf7d9-106">Cmdleten **New-AzureRmOperationalInsightsSavedSearch** skapar en ny Sparad sökning med de angivna parametrarna för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="cf7d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf7d9-107">EXAMPLES</span></span>

### <span data-ttu-id="cf7d9-108">Exempel 1: skapa en ny Sparad sökning</span><span class="sxs-lookup"><span data-stu-id="cf7d9-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="cf7d9-109">Det här kommandot skapar en ny Sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="cf7d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf7d9-110">PARAMETERS</span></span>

### <span data-ttu-id="cf7d9-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="cf7d9-111">-Category</span></span>
<span data-ttu-id="cf7d9-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="cf7d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7d9-113">-DefaultProfile</span></span>
<span data-ttu-id="cf7d9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cf7d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7d9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cf7d9-115">-DisplayName</span></span>
<span data-ttu-id="cf7d9-116">Anger det sparade visnings namnet för sökning.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="cf7d9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf7d9-117">-Force</span></span>
<span data-ttu-id="cf7d9-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf7d9-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="cf7d9-119">-Query</span></span>
<span data-ttu-id="cf7d9-120">Anger frågans namn.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="cf7d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf7d9-122">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="cf7d9-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="cf7d9-123">-SavedSearchId</span></span>
<span data-ttu-id="cf7d9-124">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="cf7d9-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cf7d9-125">-Tag</span></span>
<span data-ttu-id="cf7d9-126">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-126">The saved search tags.</span></span>

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

### <span data-ttu-id="cf7d9-127">-Version</span><span class="sxs-lookup"><span data-stu-id="cf7d9-127">-Version</span></span>
<span data-ttu-id="cf7d9-128">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7d9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf7d9-129">-WorkspaceName</span></span>
<span data-ttu-id="cf7d9-130">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="cf7d9-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf7d9-131">-Confirm</span></span>
<span data-ttu-id="cf7d9-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf7d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf7d9-133">-WhatIf</span></span>
<span data-ttu-id="cf7d9-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf7d9-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf7d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7d9-136">CommonParameters</span></span>
<span data-ttu-id="cf7d9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7d9-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7d9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7d9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf7d9-139">INPUTS</span></span>

### <span data-ttu-id="cf7d9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cf7d9-140">System.String</span></span>

### <span data-ttu-id="cf7d9-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cf7d9-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cf7d9-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="cf7d9-142">System.Int64</span></span>

## <span data-ttu-id="cf7d9-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf7d9-143">OUTPUTS</span></span>

### <span data-ttu-id="cf7d9-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="cf7d9-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="cf7d9-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf7d9-145">NOTES</span></span>

## <span data-ttu-id="cf7d9-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf7d9-146">RELATED LINKS</span></span>

[<span data-ttu-id="cf7d9-147">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="cf7d9-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


