---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578791"
---
# <span data-ttu-id="2a381-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2a381-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2a381-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a381-102">SYNOPSIS</span></span>
<span data-ttu-id="2a381-103">Tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2a381-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a381-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a381-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a381-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a381-105">DESCRIPTION</span></span>
<span data-ttu-id="2a381-106">Cmdleten **Remove-AzureRmOperationalInsightsSavedSearch** tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2a381-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="2a381-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a381-107">EXAMPLES</span></span>

### <span data-ttu-id="2a381-108">Exempel 1: ta bort en sparad sökning</span><span class="sxs-lookup"><span data-stu-id="2a381-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="2a381-109">Det här kommandot tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2a381-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="2a381-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a381-110">PARAMETERS</span></span>

### <span data-ttu-id="2a381-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a381-111">-DefaultProfile</span></span>
<span data-ttu-id="2a381-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2a381-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a381-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a381-113">-ResourceGroupName</span></span>
<span data-ttu-id="2a381-114">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="2a381-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2a381-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="2a381-115">-SavedSearchId</span></span>
<span data-ttu-id="2a381-116">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="2a381-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="2a381-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2a381-117">-WorkspaceName</span></span>
<span data-ttu-id="2a381-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="2a381-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2a381-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a381-119">-Confirm</span></span>
<span data-ttu-id="2a381-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a381-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a381-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a381-121">-WhatIf</span></span>
<span data-ttu-id="2a381-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a381-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a381-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a381-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a381-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a381-124">CommonParameters</span></span>
<span data-ttu-id="2a381-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a381-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a381-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a381-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a381-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a381-127">INPUTS</span></span>

### <span data-ttu-id="2a381-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2a381-128">System.String</span></span>

## <span data-ttu-id="2a381-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a381-129">OUTPUTS</span></span>

### <span data-ttu-id="2a381-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="2a381-130">System.Void</span></span>

## <span data-ttu-id="2a381-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a381-131">NOTES</span></span>

## <span data-ttu-id="2a381-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a381-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a381-133">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="2a381-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


