---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 97f8cba0641ed576cb187f3b995d400bc7f521a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578807"
---
# <span data-ttu-id="18b97-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="18b97-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="18b97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18b97-102">SYNOPSIS</span></span>
<span data-ttu-id="18b97-103">Skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="18b97-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18b97-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18b97-105">DESCRIPTION</span></span>
<span data-ttu-id="18b97-106">Cmdleten **New-AzureRmOperationalInsightsWorkspace** skapar en arbets yta i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="18b97-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="18b97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18b97-107">EXAMPLES</span></span>

### <span data-ttu-id="18b97-108">Exempel 1: skapa en arbets yta med namn</span><span class="sxs-lookup"><span data-stu-id="18b97-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="18b97-109">Det här kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="18b97-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="18b97-110">Exempel 2: skapa en arbets yta och länka den till ett befintligt konto</span><span class="sxs-lookup"><span data-stu-id="18b97-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="18b97-111">I det första kommandot används cmdleten Get-AzureRmOperationalInsightsLinkTargets för att skapa länk mål för operationella Insights och sedan lagras de i $OILinkTargets-variabeln.</span><span class="sxs-lookup"><span data-stu-id="18b97-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="18b97-112">Det andra kommandot skickar det första konto länks målet i $OILinkTargets till cmdleten **New-AzureRmOperationalInsightsWorkspace** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="18b97-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18b97-113">Kommandot skapar en standard-SKU-arbetsyta med namnet min arbets yta som är länkad till det första kontot för drift insikter i $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="18b97-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="18b97-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18b97-114">PARAMETERS</span></span>

### <span data-ttu-id="18b97-115">-Kundnr</span><span class="sxs-lookup"><span data-stu-id="18b97-115">-CustomerId</span></span>
<span data-ttu-id="18b97-116">Anger det konto som arbets ytan ska länkas till.</span><span class="sxs-lookup"><span data-stu-id="18b97-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="18b97-117">Get-AzureRmOperationalInsightsLinkTargets-cmdleten kan också användas för att lista de potentiella kontona.</span><span class="sxs-lookup"><span data-stu-id="18b97-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="18b97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b97-118">-DefaultProfile</span></span>
<span data-ttu-id="18b97-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="18b97-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18b97-120">-Force</span><span class="sxs-lookup"><span data-stu-id="18b97-120">-Force</span></span>
<span data-ttu-id="18b97-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="18b97-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18b97-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="18b97-122">-Location</span></span>
<span data-ttu-id="18b97-123">Anger den plats där arbets ytan ska skapas, till exempel öst eller Västeuropa.</span><span class="sxs-lookup"><span data-stu-id="18b97-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="18b97-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="18b97-124">-Name</span></span>
<span data-ttu-id="18b97-125">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="18b97-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="18b97-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b97-126">-ResourceGroupName</span></span>
<span data-ttu-id="18b97-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="18b97-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="18b97-128">Arbets ytan skapas i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="18b97-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="18b97-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="18b97-129">-RetentionInDays</span></span>
<span data-ttu-id="18b97-130">Arbets ytans data lagring i dagar.</span><span class="sxs-lookup"><span data-stu-id="18b97-130">The workspace data retention in days.</span></span> <span data-ttu-id="18b97-131">730 dagar är det högsta tillåtna antalet för alla andra SKU: er</span><span class="sxs-lookup"><span data-stu-id="18b97-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="18b97-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="18b97-132">-Sku</span></span>
<span data-ttu-id="18b97-133">Anger arbets ytans tjänste nivå.</span><span class="sxs-lookup"><span data-stu-id="18b97-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="18b97-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="18b97-134">Valid values are:</span></span> 
- <span data-ttu-id="18b97-135">gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="18b97-135">free</span></span>
- <span data-ttu-id="18b97-136">standar</span><span class="sxs-lookup"><span data-stu-id="18b97-136">standard</span></span>
- <span data-ttu-id="18b97-137">Beta</span><span class="sxs-lookup"><span data-stu-id="18b97-137">premium</span></span>

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

### <span data-ttu-id="18b97-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="18b97-138">-Tag</span></span>
<span data-ttu-id="18b97-139">Resurs märkningen för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="18b97-139">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="18b97-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18b97-140">-Confirm</span></span>
<span data-ttu-id="18b97-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18b97-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b97-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b97-142">-WhatIf</span></span>
<span data-ttu-id="18b97-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18b97-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b97-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18b97-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b97-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b97-145">CommonParameters</span></span>
<span data-ttu-id="18b97-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b97-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b97-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b97-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b97-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18b97-148">INPUTS</span></span>

### <span data-ttu-id="18b97-149">System. String</span><span class="sxs-lookup"><span data-stu-id="18b97-149">System.String</span></span>

### <span data-ttu-id="18b97-150">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="18b97-150">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="18b97-151">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="18b97-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18b97-152">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="18b97-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="18b97-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18b97-153">OUTPUTS</span></span>

### <span data-ttu-id="18b97-154">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="18b97-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="18b97-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18b97-155">NOTES</span></span>

## <span data-ttu-id="18b97-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18b97-156">RELATED LINKS</span></span>

[<span data-ttu-id="18b97-157">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="18b97-157">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="18b97-158">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="18b97-158">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


