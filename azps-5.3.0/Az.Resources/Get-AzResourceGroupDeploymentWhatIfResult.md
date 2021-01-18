---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521503"
---
# <span data-ttu-id="e05a4-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e05a4-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="e05a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e05a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e05a4-103">Hämtar en ARM-mall What-If resultatet för en distribution i resurs gruppens omfång.</span><span class="sxs-lookup"><span data-stu-id="e05a4-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="e05a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e05a4-104">SYNTAX</span></span>

### <span data-ttu-id="e05a4-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="e05a4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e05a4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e05a4-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e05a4-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e05a4-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e05a4-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e05a4-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e05a4-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e05a4-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e05a4-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e05a4-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e05a4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e05a4-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e05a4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e05a4-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e05a4-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e05a4-117">DESCRIPTION</span></span>
<span data-ttu-id="e05a4-118">Cmdleten **Get-AzResourceGroupDeploymentWhatIfResult** får arm-mallen What-If resultat för en mall distribution i den angivna resurs grupps omfattningen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="e05a4-119">Den returnerar en lista över ändringar som visar vilka resurser som kommer att uppdateras om distributionen tillämpas utan att du behöver göra några ändringar i verkliga resurser.</span><span class="sxs-lookup"><span data-stu-id="e05a4-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="e05a4-120">Om du vill ange formatet för det resulterande resultatet kan du använda parametern *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="e05a4-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="e05a4-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e05a4-121">EXAMPLES</span></span>

### <span data-ttu-id="e05a4-122">Exempel 1: få en What-If resultat i resurs gruppens omfång</span><span class="sxs-lookup"><span data-stu-id="e05a4-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="e05a4-123">Det här kommandot får en What-If resultat i den angivna resurs grupps omfattningen genom att använda en anpassad mallfil och en parameter fil på disken.</span><span class="sxs-lookup"><span data-stu-id="e05a4-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="e05a4-124">Kommandot använder parametern *ResourceGroupName* för att ange en resurs grupp där mallen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="e05a4-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="e05a4-125">Kommandot använder parametern *TemplateFile* för att ange en mallfil.</span><span class="sxs-lookup"><span data-stu-id="e05a4-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="e05a4-126">Kommandot använder parametern *TemplateParameterFile* för att ange en mallparameter.</span><span class="sxs-lookup"><span data-stu-id="e05a4-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="e05a4-127">Kommandot använder parametern *ResultFormat* för att ange What-If resultatet ska inkludera fullständiga resurs nytto laster.</span><span class="sxs-lookup"><span data-stu-id="e05a4-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="e05a4-128">Exempel 2: få ett What-If resultat i resurs gruppens omfattning med ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="e05a4-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="e05a4-129">Det här kommandot får en What-If resultat i den angivna resurs grupps omfattningen genom att använda en anpassad mallfil och en parameter fil på disken.</span><span class="sxs-lookup"><span data-stu-id="e05a4-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="e05a4-130">Kommandot använder parametern *ResourceGroupName* för att ange en resurs grupp där mallen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="e05a4-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="e05a4-131">Kommandot använder parametern *TemplateFile* för att ange en mallfil.</span><span class="sxs-lookup"><span data-stu-id="e05a4-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="e05a4-132">Kommandot använder parametern *TemplateParameterFile* för att ange en mallparameter.</span><span class="sxs-lookup"><span data-stu-id="e05a4-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="e05a4-133">Kommandot använder parametern *ResultFormat* för att ange What-If-resultatet som endast innehåller resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e05a4-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="e05a4-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e05a4-134">PARAMETERS</span></span>

### <span data-ttu-id="e05a4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05a4-135">-DefaultProfile</span></span>
<span data-ttu-id="e05a4-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e05a4-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05a4-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e05a4-137">-ExcludeChangeType</span></span>
<span data-ttu-id="e05a4-138">Kommaavgränsade resurs ändrings typer som ska uteslutas från What-If resultat.</span><span class="sxs-lookup"><span data-stu-id="e05a4-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="e05a4-139">-Mode</span></span>
<span data-ttu-id="e05a4-140">Distributions läget.</span><span class="sxs-lookup"><span data-stu-id="e05a4-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="e05a4-141">-Name</span></span>
<span data-ttu-id="e05a4-142">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e05a4-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="e05a4-143">Om inget anges används standardvärdet för mallnamnet när en mallfil tillhandahålls; Standardvärdet för den aktuella tiden när ett mallfiler tillhandahålls, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="e05a4-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-144">-För</span><span class="sxs-lookup"><span data-stu-id="e05a4-144">-Pre</span></span>
<span data-ttu-id="e05a4-145">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e05a4-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e05a4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05a4-146">-ResourceGroupName</span></span>
<span data-ttu-id="e05a4-147">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e05a4-147">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="e05a4-148">-ResultFormat</span></span>
<span data-ttu-id="e05a4-149">What-If resultat format.</span><span class="sxs-lookup"><span data-stu-id="e05a4-149">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e05a4-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e05a4-151">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e05a4-152">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e05a4-153">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="e05a4-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e05a4-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e05a4-154">-TemplateFile</span></span>
<span data-ttu-id="e05a4-155">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-155">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e05a4-156">-TemplateObject</span></span>
<span data-ttu-id="e05a4-157">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-157">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e05a4-158">-TemplateParameterFile</span></span>
<span data-ttu-id="e05a4-159">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="e05a4-159">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e05a4-160">-TemplateParameterObject</span></span>
<span data-ttu-id="e05a4-161">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="e05a4-161">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e05a4-162">-TemplateParameterUri</span></span>
<span data-ttu-id="e05a4-163">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-163">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e05a4-164">-TemplateUri</span></span>
<span data-ttu-id="e05a4-165">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="e05a4-165">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05a4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05a4-166">CommonParameters</span></span>
<span data-ttu-id="e05a4-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05a4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05a4-168">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e05a4-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05a4-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e05a4-169">INPUTS</span></span>

### <span data-ttu-id="e05a4-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e05a4-170">System.String</span></span>

### <span data-ttu-id="e05a4-171">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="e05a4-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="e05a4-172">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e05a4-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e05a4-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e05a4-173">OUTPUTS</span></span>

### <span data-ttu-id="e05a4-174">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="e05a4-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="e05a4-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e05a4-175">NOTES</span></span>

## <span data-ttu-id="e05a4-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e05a4-176">RELATED LINKS</span></span>
