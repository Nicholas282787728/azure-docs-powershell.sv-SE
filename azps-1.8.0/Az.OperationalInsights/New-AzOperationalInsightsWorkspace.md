---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 863b83cbab64d791e55f8cfc2719d66be64fcac6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928521"
---
# <span data-ttu-id="969fc-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="969fc-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="969fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="969fc-102">SYNOPSIS</span></span>
<span data-ttu-id="969fc-103">Skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="969fc-103">Creates a workspace.</span></span>

## <span data-ttu-id="969fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="969fc-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="969fc-105">DESCRIPTION</span></span>
<span data-ttu-id="969fc-106">Cmdleten **New-AzOperationalInsightsWorkspace** skapar en arbets yta i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="969fc-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="969fc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="969fc-107">EXAMPLES</span></span>

### <span data-ttu-id="969fc-108">Exempel 1: skapa en arbets yta med namn</span><span class="sxs-lookup"><span data-stu-id="969fc-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="969fc-109">Det här kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="969fc-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="969fc-110">Exempel 2: skapa en arbets yta och länka den till ett befintligt konto</span><span class="sxs-lookup"><span data-stu-id="969fc-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="969fc-111">I det första kommandot används cmdleten Get-AzOperationalInsightsLinkTargets för att skapa länk mål för operationella Insights och sedan lagras de i $OILinkTargets-variabeln.</span><span class="sxs-lookup"><span data-stu-id="969fc-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="969fc-112">Det andra kommandot skickar det första konto länks målet i $OILinkTargets till cmdleten **New-AzOperationalInsightsWorkspace** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="969fc-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="969fc-113">Kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta som är länkad till det första kontot för drift insikter i $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="969fc-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="969fc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="969fc-114">PARAMETERS</span></span>

### <span data-ttu-id="969fc-115">-Kundnr</span><span class="sxs-lookup"><span data-stu-id="969fc-115">-CustomerId</span></span>
<span data-ttu-id="969fc-116">Anger det konto som arbets ytan ska länkas till.</span><span class="sxs-lookup"><span data-stu-id="969fc-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="969fc-117">Get-AzOperationalInsightsLinkTargets-cmdleten kan också användas för att lista de potentiella kontona.</span><span class="sxs-lookup"><span data-stu-id="969fc-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969fc-118">-DefaultProfile</span></span>
<span data-ttu-id="969fc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="969fc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="969fc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="969fc-120">-Force</span></span>
<span data-ttu-id="969fc-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="969fc-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="969fc-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="969fc-122">-Location</span></span>
<span data-ttu-id="969fc-123">Anger den plats där arbets ytan ska skapas, till exempel öst eller Västeuropa.</span><span class="sxs-lookup"><span data-stu-id="969fc-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="969fc-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="969fc-124">-Name</span></span>
<span data-ttu-id="969fc-125">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="969fc-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="969fc-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="969fc-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="969fc-128">Arbets ytan skapas i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="969fc-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="969fc-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="969fc-129">-RetentionInDays</span></span>
<span data-ttu-id="969fc-130">Arbets ytans data lagring i dagar.</span><span class="sxs-lookup"><span data-stu-id="969fc-130">The workspace data retention in days.</span></span> <span data-ttu-id="969fc-131">730 dagar är det högsta tillåtna antalet för alla andra SKU: er</span><span class="sxs-lookup"><span data-stu-id="969fc-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969fc-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="969fc-132">-Sku</span></span>
<span data-ttu-id="969fc-133">Anger arbets ytans tjänste nivå.</span><span class="sxs-lookup"><span data-stu-id="969fc-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="969fc-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="969fc-134">Valid values are:</span></span>
- <span data-ttu-id="969fc-135">gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="969fc-135">free</span></span>
- <span data-ttu-id="969fc-136">standar</span><span class="sxs-lookup"><span data-stu-id="969fc-136">standard</span></span>
- <span data-ttu-id="969fc-137">fristående</span><span class="sxs-lookup"><span data-stu-id="969fc-137">standalone</span></span>
- <span data-ttu-id="969fc-138">Beta</span><span class="sxs-lookup"><span data-stu-id="969fc-138">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969fc-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="969fc-139">-Tag</span></span>
<span data-ttu-id="969fc-140">Resurs märkningen för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="969fc-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969fc-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="969fc-141">-Confirm</span></span>
<span data-ttu-id="969fc-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="969fc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969fc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969fc-143">-WhatIf</span></span>
<span data-ttu-id="969fc-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="969fc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969fc-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="969fc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969fc-146">CommonParameters</span></span>
<span data-ttu-id="969fc-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969fc-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969fc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969fc-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="969fc-149">INPUTS</span></span>

### <span data-ttu-id="969fc-150">System. String</span><span class="sxs-lookup"><span data-stu-id="969fc-150">System.String</span></span>

### <span data-ttu-id="969fc-151">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="969fc-151">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="969fc-152">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="969fc-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="969fc-153">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="969fc-153">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="969fc-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="969fc-154">OUTPUTS</span></span>

### <span data-ttu-id="969fc-155">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="969fc-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="969fc-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="969fc-156">NOTES</span></span>

<span data-ttu-id="969fc-157">En ny pris modell har frisläppts.</span><span class="sxs-lookup"><span data-stu-id="969fc-157">A new pricing model has been released.</span></span> <span data-ttu-id="969fc-158">Om du är en CSP som innebär att du måste använda "fristående" för SKU: n.</span><span class="sxs-lookup"><span data-stu-id="969fc-158">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="969fc-159">Från kulisserna ändras SKU till pergb2018.</span><span class="sxs-lookup"><span data-stu-id="969fc-159">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="969fc-160">För mer information, se följande: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="969fc-160">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="969fc-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="969fc-161">RELATED LINKS</span></span>

[<span data-ttu-id="969fc-162">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="969fc-162">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
