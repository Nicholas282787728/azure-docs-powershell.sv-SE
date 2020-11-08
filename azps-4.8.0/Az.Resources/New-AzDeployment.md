---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 56be1071c2a6307bee28f0ce4cf13dde626df72e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100894"
---
# <span data-ttu-id="3413f-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3413f-101">New-AzDeployment</span></span>

## <span data-ttu-id="3413f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3413f-102">SYNOPSIS</span></span>
<span data-ttu-id="3413f-103">Skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3413f-103">Create a deployment</span></span>

## <span data-ttu-id="3413f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3413f-104">SYNTAX</span></span>

### <span data-ttu-id="3413f-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="3413f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3413f-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3413f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3413f-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3413f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3413f-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3413f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3413f-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3413f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3413f-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3413f-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3413f-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3413f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3413f-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3413f-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3413f-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3413f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3413f-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3413f-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3413f-117">DESCRIPTION</span></span>
<span data-ttu-id="3413f-118">Cmdleten **New-AzDeployment** lägger till en distribution i den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="3413f-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="3413f-119">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="3413f-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="3413f-120">En Azure-resurs är en användardefinierad Azure-enhet.</span><span class="sxs-lookup"><span data-stu-id="3413f-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="3413f-121">En resurs kan finnas i en resurs grupp, till exempel databas server, databas, webbplats, virtuell dator eller lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3413f-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="3413f-122">Eller så kan det vara en prenumerations nivå resurs, till exempel roll definition, princip definition etc.</span><span class="sxs-lookup"><span data-stu-id="3413f-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="3413f-123">Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzResourceGroupDeployment** som skapar en distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3413f-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="3413f-124">Cmdleten **New-AzDeployment** skapar en distribution vid den aktuella prenumerationens omfattning, som distribuerar abonnemangs nivå resurser.</span><span class="sxs-lookup"><span data-stu-id="3413f-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="3413f-125">Om du vill lägga till en distribution vid abonnemang anger du platsen och en mall.</span><span class="sxs-lookup"><span data-stu-id="3413f-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="3413f-126">Platsen säger att Azure Resource Manager lagrar distributions data.</span><span class="sxs-lookup"><span data-stu-id="3413f-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="3413f-127">Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="3413f-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="3413f-128">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="3413f-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="3413f-129">Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="3413f-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="3413f-130">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3413f-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="3413f-131">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="3413f-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="3413f-132">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="3413f-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="3413f-133">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="3413f-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="3413f-134">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="3413f-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="3413f-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3413f-135">EXAMPLES</span></span>

### <span data-ttu-id="3413f-136">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3413f-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="3413f-137">Det här kommandot skapar en ny distribution vid det aktuella abonnemanget med hjälp av en anpassad mall och en mallfil på disk, med en definierad tagg-parameter.</span><span class="sxs-lookup"><span data-stu-id="3413f-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="3413f-138">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="3413f-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="3413f-139">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="3413f-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="3413f-140">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3413f-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="3413f-141">Det här kommandot skapar en ny distribution vid det aktuella abonnemanget genom att använda en anpassad mall och en mallfil på en disk som har konverterats till en i minnet.</span><span class="sxs-lookup"><span data-stu-id="3413f-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="3413f-142">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="3413f-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="3413f-143">Det sista kommandot använder parametern *TemplateObject* för att ange den här hash-tabellen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="3413f-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="3413f-144">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="3413f-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="3413f-145">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3413f-145">PARAMETERS</span></span>

### <span data-ttu-id="3413f-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3413f-146">-ApiVersion</span></span>
<span data-ttu-id="3413f-147">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3413f-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3413f-148">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="3413f-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3413f-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3413f-149">-AsJob</span></span>
<span data-ttu-id="3413f-150">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3413f-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3413f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3413f-151">-DefaultProfile</span></span>
<span data-ttu-id="3413f-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3413f-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3413f-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="3413f-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="3413f-154">Loggnings nivå för distributions fel.</span><span class="sxs-lookup"><span data-stu-id="3413f-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="3413f-155">-Plats</span><span class="sxs-lookup"><span data-stu-id="3413f-155">-Location</span></span>
<span data-ttu-id="3413f-156">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="3413f-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3413f-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="3413f-157">-Name</span></span>
<span data-ttu-id="3413f-158">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3413f-158">The name of the deployment it's going to create.</span></span> <span data-ttu-id="3413f-159">Om inget anges används standardvärdet för mallnamnet när en mallfil tillhandahålls; Standardvärdet för den aktuella tiden när ett mallfiler tillhandahålls, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="3413f-159">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="3413f-160">-För</span><span class="sxs-lookup"><span data-stu-id="3413f-160">-Pre</span></span>
<span data-ttu-id="3413f-161">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3413f-161">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3413f-162">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3413f-162">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3413f-163">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="3413f-163">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="3413f-164">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="3413f-164">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="3413f-165">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="3413f-165">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3413f-166">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3413f-166">-Tag</span></span>
<span data-ttu-id="3413f-167">Taggarna som ska läggas till i distributionen.</span><span class="sxs-lookup"><span data-stu-id="3413f-167">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3413f-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3413f-168">-TemplateFile</span></span>
<span data-ttu-id="3413f-169">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="3413f-169">Local path to the template file.</span></span>

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

### <span data-ttu-id="3413f-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3413f-170">-TemplateObject</span></span>
<span data-ttu-id="3413f-171">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="3413f-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3413f-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3413f-172">-TemplateParameterFile</span></span>
<span data-ttu-id="3413f-173">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="3413f-173">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3413f-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3413f-174">-TemplateParameterObject</span></span>
<span data-ttu-id="3413f-175">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="3413f-175">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3413f-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3413f-176">-TemplateParameterUri</span></span>
<span data-ttu-id="3413f-177">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="3413f-177">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3413f-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3413f-178">-TemplateUri</span></span>
<span data-ttu-id="3413f-179">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="3413f-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="3413f-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="3413f-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="3413f-181">Kommaavgränsade resurs ändrings typer som ska uteslutas från What-If resultat.</span><span class="sxs-lookup"><span data-stu-id="3413f-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="3413f-182">Tillämpbar när växeln-WhatIf eller-Confirm har ställts in.</span><span class="sxs-lookup"><span data-stu-id="3413f-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="3413f-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="3413f-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="3413f-184">What-If resultat format.</span><span class="sxs-lookup"><span data-stu-id="3413f-184">The What-If result format.</span></span>

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

### <span data-ttu-id="3413f-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3413f-185">-Confirm</span></span>
<span data-ttu-id="3413f-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3413f-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3413f-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3413f-187">-WhatIf</span></span>
<span data-ttu-id="3413f-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3413f-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3413f-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3413f-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3413f-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3413f-190">CommonParameters</span></span>
<span data-ttu-id="3413f-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3413f-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3413f-192">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3413f-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3413f-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3413f-193">INPUTS</span></span>

### <span data-ttu-id="3413f-194">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3413f-194">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3413f-195">System. String</span><span class="sxs-lookup"><span data-stu-id="3413f-195">System.String</span></span>

## <span data-ttu-id="3413f-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3413f-196">OUTPUTS</span></span>

### <span data-ttu-id="3413f-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3413f-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3413f-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3413f-198">NOTES</span></span>

## <span data-ttu-id="3413f-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3413f-199">RELATED LINKS</span></span>
