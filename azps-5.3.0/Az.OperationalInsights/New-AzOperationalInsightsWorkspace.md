---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523153"
---
# <span data-ttu-id="c6f5d-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6f5d-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c6f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f5d-103">Skapar en arbets yta eller återställer en arbets yta som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="c6f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6f5d-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f5d-106">Cmdleten **New-AzOperationalInsightsWorkspace** skapar en arbets yta i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="c6f5d-107">Eller återställa en arbets yta som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="c6f5d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6f5d-108">EXAMPLES</span></span>

### <span data-ttu-id="c6f5d-109">Exempel 1: skapa en arbets yta med namn</span><span class="sxs-lookup"><span data-stu-id="c6f5d-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="c6f5d-110">Det här kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c6f5d-111">Exempel 2: skapa en arbets yta och länka den till ett befintligt konto</span><span class="sxs-lookup"><span data-stu-id="c6f5d-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="c6f5d-112">I det första kommandot används cmdleten Get-AzOperationalInsightsLinkTargets för att skapa länk mål för operationella Insights och sedan lagras de i $OILinkTargets-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="c6f5d-113">Det andra kommandot skickar det första konto länks målet i $OILinkTargets till cmdleten **New-AzOperationalInsightsWorkspace** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c6f5d-114">Kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta som är länkad till det första kontot för drift insikter i $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="c6f5d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6f5d-115">PARAMETERS</span></span>

### <span data-ttu-id="c6f5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f5d-116">-DefaultProfile</span></span>
<span data-ttu-id="c6f5d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c6f5d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6f5d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c6f5d-118">-Force</span></span>
<span data-ttu-id="c6f5d-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6f5d-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c6f5d-120">-Location</span></span>
<span data-ttu-id="c6f5d-121">Anger den plats där arbets ytan ska skapas, till exempel öst eller Västeuropa.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="c6f5d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6f5d-122">-Name</span></span>
<span data-ttu-id="c6f5d-123">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c6f5d-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c6f5d-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c6f5d-125">Nätverks åtkomst typen för att komma åt arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="c6f5d-126">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="c6f5d-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5d-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c6f5d-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c6f5d-128">Nätverks åtkomst typen för åtkomst till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="c6f5d-129">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="c6f5d-129">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="c6f5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="c6f5d-131">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6f5d-132">Arbets ytan skapas i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="c6f5d-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c6f5d-133">-RetentionInDays</span></span>
<span data-ttu-id="c6f5d-134">Arbets ytans data lagring i dagar.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-134">The workspace data retention in days.</span></span> <span data-ttu-id="c6f5d-135">730 dagar är det högsta tillåtna antalet för alla andra SKU: er</span><span class="sxs-lookup"><span data-stu-id="c6f5d-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="c6f5d-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6f5d-136">-Sku</span></span>
<span data-ttu-id="c6f5d-137">Anger arbets ytans tjänste nivå.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="c6f5d-138">Mer information om vilka värden som ska användas finns i https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="c6f5d-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="c6f5d-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="c6f5d-139">Valid values are:</span></span>
- <span data-ttu-id="c6f5d-140">gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="c6f5d-140">free</span></span>
- <span data-ttu-id="c6f5d-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="c6f5d-141">pergb2018</span></span>
- <span data-ttu-id="c6f5d-142">pernode</span><span class="sxs-lookup"><span data-stu-id="c6f5d-142">pernode</span></span>
- <span data-ttu-id="c6f5d-143">Beta</span><span class="sxs-lookup"><span data-stu-id="c6f5d-143">premium</span></span>
- <span data-ttu-id="c6f5d-144">fristående</span><span class="sxs-lookup"><span data-stu-id="c6f5d-144">standalone</span></span>
- <span data-ttu-id="c6f5d-145">standar</span><span class="sxs-lookup"><span data-stu-id="c6f5d-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5d-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c6f5d-146">-Tag</span></span>
<span data-ttu-id="c6f5d-147">Resurs märkningen för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="c6f5d-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6f5d-148">-Confirm</span></span>
<span data-ttu-id="c6f5d-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f5d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f5d-150">-WhatIf</span></span>
<span data-ttu-id="c6f5d-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6f5d-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f5d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f5d-153">CommonParameters</span></span>
<span data-ttu-id="c6f5d-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f5d-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6f5d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f5d-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6f5d-156">INPUTS</span></span>

### <span data-ttu-id="c6f5d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f5d-157">System.String</span></span>

### <span data-ttu-id="c6f5d-158">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6f5d-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c6f5d-159">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c6f5d-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c6f5d-160">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6f5d-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c6f5d-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6f5d-161">OUTPUTS</span></span>

### <span data-ttu-id="c6f5d-162">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6f5d-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c6f5d-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6f5d-163">NOTES</span></span>

<span data-ttu-id="c6f5d-164">En ny pris modell har frisläppts.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-164">A new pricing model has been released.</span></span> <span data-ttu-id="c6f5d-165">Om du är en CSP som innebär att du måste använda "fristående" för SKU: n.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="c6f5d-166">Från kulisserna ändras SKU till pergb2018.</span><span class="sxs-lookup"><span data-stu-id="c6f5d-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="c6f5d-167">För mer information, se följande: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="c6f5d-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="c6f5d-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6f5d-168">RELATED LINKS</span></span>

[<span data-ttu-id="c6f5d-169">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="c6f5d-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="c6f5d-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="c6f5d-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


