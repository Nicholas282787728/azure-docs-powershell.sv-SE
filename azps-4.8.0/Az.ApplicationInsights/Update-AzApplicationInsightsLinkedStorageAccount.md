---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103330"
---
# <span data-ttu-id="afc8d-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="afc8d-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="afc8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="afc8d-103">Uppdatera Application Insights Linked Storage-konto</span><span class="sxs-lookup"><span data-stu-id="afc8d-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="afc8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afc8d-104">SYNTAX</span></span>

### <span data-ttu-id="afc8d-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="afc8d-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc8d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc8d-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc8d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc8d-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc8d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afc8d-108">DESCRIPTION</span></span>
<span data-ttu-id="afc8d-109">Uppdatera Application Insights Linked Storage-konto</span><span class="sxs-lookup"><span data-stu-id="afc8d-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="afc8d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afc8d-110">EXAMPLES</span></span>

### <span data-ttu-id="afc8d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afc8d-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="afc8d-112">Uppdatera länkat lagrings konto under komponenten "componentName" för att associera med $account</span><span class="sxs-lookup"><span data-stu-id="afc8d-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="afc8d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afc8d-113">PARAMETERS</span></span>

### <span data-ttu-id="afc8d-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="afc8d-114">-ComponentName</span></span>
<span data-ttu-id="afc8d-115">Komponent namn</span><span class="sxs-lookup"><span data-stu-id="afc8d-115">Component Name</span></span>

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

### <span data-ttu-id="afc8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc8d-116">-DefaultProfile</span></span>
<span data-ttu-id="afc8d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afc8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc8d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afc8d-118">-InputObject</span></span>
<span data-ttu-id="afc8d-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="afc8d-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="afc8d-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="afc8d-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="afc8d-121">Lagrings konto ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc8d-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc8d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc8d-122">-ResourceGroupName</span></span>
<span data-ttu-id="afc8d-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="afc8d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="afc8d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc8d-124">-ResourceId</span></span>
<span data-ttu-id="afc8d-125">Komponent-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc8d-125">Component ResourceId</span></span>

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

### <span data-ttu-id="afc8d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afc8d-126">-Confirm</span></span>
<span data-ttu-id="afc8d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afc8d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc8d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc8d-128">-WhatIf</span></span>
<span data-ttu-id="afc8d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afc8d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc8d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afc8d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc8d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc8d-131">CommonParameters</span></span>
<span data-ttu-id="afc8d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc8d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc8d-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afc8d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc8d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afc8d-134">INPUTS</span></span>

### <span data-ttu-id="afc8d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="afc8d-135">System.String</span></span>

### <span data-ttu-id="afc8d-136">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="afc8d-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="afc8d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afc8d-137">OUTPUTS</span></span>

### <span data-ttu-id="afc8d-138">Microsoft. Azure. commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="afc8d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="afc8d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afc8d-139">NOTES</span></span>

## <span data-ttu-id="afc8d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afc8d-140">RELATED LINKS</span></span>