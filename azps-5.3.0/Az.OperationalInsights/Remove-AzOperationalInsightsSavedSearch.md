---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527323"
---
# <span data-ttu-id="50ce2-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="50ce2-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="50ce2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="50ce2-103">Tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="50ce2-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="50ce2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50ce2-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50ce2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="50ce2-106">Cmdleten **Remove-AzOperationalInsightsSavedSearch** tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="50ce2-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="50ce2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="50ce2-108">Exempel 1: ta bort en sparad sökning</span><span class="sxs-lookup"><span data-stu-id="50ce2-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="50ce2-109">Det här kommandot tar bort en sparad sökning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="50ce2-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="50ce2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50ce2-110">PARAMETERS</span></span>

### <span data-ttu-id="50ce2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ce2-111">-DefaultProfile</span></span>
<span data-ttu-id="50ce2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50ce2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50ce2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ce2-113">-ResourceGroupName</span></span>
<span data-ttu-id="50ce2-114">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="50ce2-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="50ce2-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="50ce2-115">-SavedSearchId</span></span>
<span data-ttu-id="50ce2-116">Anger det sparade Sök-ID: t.</span><span class="sxs-lookup"><span data-stu-id="50ce2-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="50ce2-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50ce2-117">-WorkspaceName</span></span>
<span data-ttu-id="50ce2-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="50ce2-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="50ce2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50ce2-119">-Confirm</span></span>
<span data-ttu-id="50ce2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50ce2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ce2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ce2-121">-WhatIf</span></span>
<span data-ttu-id="50ce2-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50ce2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50ce2-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50ce2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50ce2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ce2-124">CommonParameters</span></span>
<span data-ttu-id="50ce2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ce2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ce2-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ce2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ce2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50ce2-127">INPUTS</span></span>

### <span data-ttu-id="50ce2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="50ce2-128">System.String</span></span>

## <span data-ttu-id="50ce2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50ce2-129">OUTPUTS</span></span>

### <span data-ttu-id="50ce2-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="50ce2-130">System.Void</span></span>

## <span data-ttu-id="50ce2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50ce2-131">NOTES</span></span>

## <span data-ttu-id="50ce2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50ce2-132">RELATED LINKS</span></span>

[<span data-ttu-id="50ce2-133">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="50ce2-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


