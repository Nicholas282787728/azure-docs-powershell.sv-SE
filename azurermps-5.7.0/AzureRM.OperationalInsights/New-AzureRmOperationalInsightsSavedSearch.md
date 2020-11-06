---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: c8ad9196cd0f89670de38f6c99550e397016661e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585987"
---
# <span data-ttu-id="69ff7-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="69ff7-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="69ff7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="69ff7-103">Skapar en ny Sparad sökning med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="69ff7-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ff7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69ff7-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69ff7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="69ff7-106">Cmdleten **New-AzureRmOperationalInsightsSavedSearch** skapar en ny Sparad sökning med de angivna parametrarna för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="69ff7-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="69ff7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="69ff7-108">Exempel 1: skapa en ny Sparad sökning</span><span class="sxs-lookup"><span data-stu-id="69ff7-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="69ff7-109">Det här kommandot skapar en ny Sparad sökning.</span><span class="sxs-lookup"><span data-stu-id="69ff7-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="69ff7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69ff7-110">PARAMETERS</span></span>

### <span data-ttu-id="69ff7-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="69ff7-111">-Category</span></span>
<span data-ttu-id="69ff7-112">Anger kategori namnet.</span><span class="sxs-lookup"><span data-stu-id="69ff7-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="69ff7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ff7-113">-DefaultProfile</span></span>
<span data-ttu-id="69ff7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69ff7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69ff7-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="69ff7-115">-DisplayName</span></span>
<span data-ttu-id="69ff7-116">Anger det sparade visnings namnet för sökning.</span><span class="sxs-lookup"><span data-stu-id="69ff7-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="69ff7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="69ff7-117">-Force</span></span>
<span data-ttu-id="69ff7-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="69ff7-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ff7-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="69ff7-119">-Query</span></span>
<span data-ttu-id="69ff7-120">Anger frågans namn.</span><span class="sxs-lookup"><span data-stu-id="69ff7-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="69ff7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ff7-121">-ResourceGroupName</span></span>
<span data-ttu-id="69ff7-122">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="69ff7-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="69ff7-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="69ff7-123">-SavedSearchId</span></span>
<span data-ttu-id="69ff7-124">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="69ff7-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="69ff7-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="69ff7-125">-Tag</span></span>
<span data-ttu-id="69ff7-126">De sparade Sök etiketterna.</span><span class="sxs-lookup"><span data-stu-id="69ff7-126">The saved search tags.</span></span>

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

### <span data-ttu-id="69ff7-127">-Version</span><span class="sxs-lookup"><span data-stu-id="69ff7-127">-Version</span></span>
<span data-ttu-id="69ff7-128">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="69ff7-128">Specifies the version.</span></span>

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

### <span data-ttu-id="69ff7-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69ff7-129">-WorkspaceName</span></span>
<span data-ttu-id="69ff7-130">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="69ff7-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="69ff7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69ff7-131">-Confirm</span></span>
<span data-ttu-id="69ff7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69ff7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ff7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ff7-133">-WhatIf</span></span>
<span data-ttu-id="69ff7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69ff7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ff7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69ff7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ff7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ff7-136">CommonParameters</span></span>
<span data-ttu-id="69ff7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ff7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ff7-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ff7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ff7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69ff7-139">INPUTS</span></span>

### <span data-ttu-id="69ff7-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="69ff7-140">None</span></span>
<span data-ttu-id="69ff7-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="69ff7-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69ff7-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69ff7-142">OUTPUTS</span></span>

## <span data-ttu-id="69ff7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69ff7-143">NOTES</span></span>

## <span data-ttu-id="69ff7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69ff7-144">RELATED LINKS</span></span>

[<span data-ttu-id="69ff7-145">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="69ff7-145">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


