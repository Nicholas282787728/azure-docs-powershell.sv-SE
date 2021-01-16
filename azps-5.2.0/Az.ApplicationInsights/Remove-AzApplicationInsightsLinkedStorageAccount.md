---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406760"
---
# <span data-ttu-id="caae4-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="caae4-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="caae4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="caae4-102">SYNOPSIS</span></span>
<span data-ttu-id="caae4-103">Ta bort Application Insights-länkat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="caae4-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="caae4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="caae4-104">SYNTAX</span></span>

### <span data-ttu-id="caae4-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="caae4-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caae4-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caae4-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caae4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caae4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caae4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="caae4-108">DESCRIPTION</span></span>
<span data-ttu-id="caae4-109">Ta bort Application Insights-länkat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="caae4-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="caae4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="caae4-110">EXAMPLES</span></span>

### <span data-ttu-id="caae4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="caae4-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="caae4-112">Ta bort länkat lagrings konto som är associerat med Application Insights-komponenten "componentName"</span><span class="sxs-lookup"><span data-stu-id="caae4-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="caae4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="caae4-113">PARAMETERS</span></span>

### <span data-ttu-id="caae4-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="caae4-114">-ComponentName</span></span>
<span data-ttu-id="caae4-115">Komponent namn</span><span class="sxs-lookup"><span data-stu-id="caae4-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caae4-116">-DefaultProfile</span></span>
<span data-ttu-id="caae4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="caae4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caae4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caae4-118">-InputObject</span></span>
<span data-ttu-id="caae4-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="caae4-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caae4-120">-ResourceGroupName</span></span>
<span data-ttu-id="caae4-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="caae4-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caae4-122">-ResourceId</span></span>
<span data-ttu-id="caae4-123">Komponent-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caae4-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="caae4-124">-Confirm</span></span>
<span data-ttu-id="caae4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="caae4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caae4-126">-WhatIf</span></span>
<span data-ttu-id="caae4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="caae4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caae4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="caae4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caae4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caae4-129">CommonParameters</span></span>
<span data-ttu-id="caae4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caae4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caae4-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caae4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caae4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="caae4-132">INPUTS</span></span>

### <span data-ttu-id="caae4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="caae4-133">System.String</span></span>

### <span data-ttu-id="caae4-134">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="caae4-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="caae4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="caae4-135">OUTPUTS</span></span>

### <span data-ttu-id="caae4-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="caae4-136">System.Boolean</span></span>

## <span data-ttu-id="caae4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="caae4-137">NOTES</span></span>

## <span data-ttu-id="caae4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="caae4-138">RELATED LINKS</span></span>
