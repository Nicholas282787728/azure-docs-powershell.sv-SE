---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 15dcc77a616037d6190fa11be34b8bc8f762aa59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258033"
---
# <span data-ttu-id="4e5f4-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4e5f4-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="4e5f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5f4-103">Hämtar en ARM-mall What-If resultatet för en distribution i prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="4e5f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e5f4-104">SYNTAX</span></span>

### <span data-ttu-id="4e5f4-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="4e5f4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4e5f4-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4e5f4-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4e5f4-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4e5f4-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4e5f4-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4e5f4-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4e5f4-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e5f4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4e5f4-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e5f4-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e5f4-117">DESCRIPTION</span></span>
<span data-ttu-id="4e5f4-118">Cmdleten **Get-AzDeploymentWhatIfResult** får arm-mallen What-If resultat för en mall distribution i den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="4e5f4-119">Den returnerar en lista över ändringar som visar vilka resurser som kommer att uppdateras om distributionen tillämpas utan att du behöver göra några ändringar i verkliga resurser.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="4e5f4-120">Om du vill ange formatet för det resulterande resultatet kan du använda parametern *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="4e5f4-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="4e5f4-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e5f4-121">EXAMPLES</span></span>

### <span data-ttu-id="4e5f4-122">Exempel 1: Hämta en What-If resultat av ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4e5f4-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="4e5f4-123">Det här kommandot får en What-If resultat i det aktuella abonnemanget med hjälp av en anpassad mallfil och en parameter fil på disken.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4e5f4-124">Kommandot använder parametern *location* för att ange var distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4e5f4-125">Kommandot använder parametern *TemplateFile* för att ange en mallfil.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4e5f4-126">Kommandot använder parametern *TemplateParameterFile* för att ange en mallparameter.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4e5f4-127">Kommandot använder parametern *ResultFormat* för att ange What-If resultatet ska inkludera fullständiga resurs nytto laster.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="4e5f4-128">Exempel 2: Hämta ett What-If resultat i ett abonnemang med ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="4e5f4-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="4e5f4-129">Det här kommandot får en What-If resultat i det aktuella abonnemanget med hjälp av en anpassad mallfil och en parameter fil på disken.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4e5f4-130">Kommandot använder parametern *location* för att ange var distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4e5f4-131">Kommandot använder parametern *TemplateFile* för att ange en mallfil.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4e5f4-132">Kommandot använder parametern *TemplateParameterFile* för att ange en mallparameter.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4e5f4-133">Kommandot använder parametern *ResultFormat* för att ange What-If-resultatet som endast innehåller resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="4e5f4-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e5f4-134">PARAMETERS</span></span>

### <span data-ttu-id="4e5f4-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e5f4-135">-ApiVersion</span></span>
<span data-ttu-id="4e5f4-136">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4e5f4-137">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5f4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-138">-DefaultProfile</span></span>
<span data-ttu-id="4e5f4-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e5f4-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4e5f4-140">-ExcludeChangeType</span></span>
<span data-ttu-id="4e5f4-141">Kommaavgränsad lista över resurs ändrings typer som ska uteslutas från What-If resultat.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-141">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="4e5f4-142">-Plats</span><span class="sxs-lookup"><span data-stu-id="4e5f4-142">-Location</span></span>
<span data-ttu-id="4e5f4-143">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-143">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4e5f4-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e5f4-144">-Name</span></span>
<span data-ttu-id="4e5f4-145">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4e5f4-146">Om inget anges används standardvärdet för mallnamnet när en mallfil tillhandahålls; Standardvärdet för den aktuella tiden när ett mallfiler tillhandahålls, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4e5f4-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5f4-147">-För</span><span class="sxs-lookup"><span data-stu-id="4e5f4-147">-Pre</span></span>
<span data-ttu-id="4e5f4-148">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4e5f4-149">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="4e5f4-149">-ResultFormat</span></span>
<span data-ttu-id="4e5f4-150">What-If resultat format.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-150">The What-If result format.</span></span>

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

### <span data-ttu-id="4e5f4-151">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4e5f4-151">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4e5f4-152">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-152">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="4e5f4-153">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-153">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="4e5f4-154">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-154">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4e5f4-155">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-155">-TemplateFile</span></span>
<span data-ttu-id="4e5f4-156">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-156">Local path to the template file.</span></span>

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

### <span data-ttu-id="4e5f4-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4e5f4-157">-TemplateObject</span></span>
<span data-ttu-id="4e5f4-158">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4e5f4-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4e5f4-159">-TemplateParameterFile</span></span>
<span data-ttu-id="4e5f4-160">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4e5f4-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4e5f4-161">-TemplateParameterObject</span></span>
<span data-ttu-id="4e5f4-162">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4e5f4-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4e5f4-163">-TemplateParameterUri</span></span>
<span data-ttu-id="4e5f4-164">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4e5f4-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4e5f4-165">-TemplateUri</span></span>
<span data-ttu-id="4e5f4-166">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="4e5f4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5f4-167">CommonParameters</span></span>
<span data-ttu-id="4e5f4-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5f4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5f4-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e5f4-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5f4-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e5f4-170">INPUTS</span></span>

### <span data-ttu-id="4e5f4-171">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4e5f4-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4e5f4-172">System. String</span><span class="sxs-lookup"><span data-stu-id="4e5f4-172">System.String</span></span>

## <span data-ttu-id="4e5f4-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e5f4-173">OUTPUTS</span></span>

### <span data-ttu-id="4e5f4-174">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="4e5f4-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="4e5f4-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e5f4-175">NOTES</span></span>

## <span data-ttu-id="4e5f4-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e5f4-176">RELATED LINKS</span></span>
