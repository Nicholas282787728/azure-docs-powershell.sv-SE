---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 2cd572266656cf194e1d0ff73770f2d2e617009d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092183"
---
# <span data-ttu-id="3891f-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3891f-101">New-AzDeployment</span></span>

## <span data-ttu-id="3891f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3891f-102">SYNOPSIS</span></span>
<span data-ttu-id="3891f-103">Skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3891f-103">Create a deployment</span></span>

## <span data-ttu-id="3891f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3891f-104">SYNTAX</span></span>

### <span data-ttu-id="3891f-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="3891f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3891f-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3891f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3891f-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3891f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3891f-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3891f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3891f-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3891f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3891f-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3891f-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3891f-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3891f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3891f-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3891f-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3891f-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3891f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3891f-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3891f-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3891f-117">DESCRIPTION</span></span>
<span data-ttu-id="3891f-118">Cmdleten **New-AzDeployment** lägger till en distribution i den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="3891f-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="3891f-119">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="3891f-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="3891f-120">En Azure-resurs är en användardefinierad Azure-enhet.</span><span class="sxs-lookup"><span data-stu-id="3891f-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="3891f-121">En resurs kan finnas i en resurs grupp, till exempel databas server, databas, webbplats, virtuell dator eller lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3891f-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="3891f-122">Eller så kan det vara en prenumerations nivå resurs, till exempel roll definition, princip definition etc.</span><span class="sxs-lookup"><span data-stu-id="3891f-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="3891f-123">Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzResourceGroupDeployment** som skapar en distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3891f-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="3891f-124">Cmdleten **New-AzDeployment** skapar en distribution vid den aktuella prenumerationens omfattning, som distribuerar abonnemangs nivå resurser.</span><span class="sxs-lookup"><span data-stu-id="3891f-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="3891f-125">Om du vill lägga till en distribution vid abonnemang anger du platsen och en mall.</span><span class="sxs-lookup"><span data-stu-id="3891f-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="3891f-126">Platsen säger att Azure Resource Manager lagrar distributions data.</span><span class="sxs-lookup"><span data-stu-id="3891f-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="3891f-127">Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="3891f-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="3891f-128">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="3891f-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="3891f-129">Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="3891f-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="3891f-130">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3891f-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="3891f-131">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="3891f-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="3891f-132">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="3891f-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="3891f-133">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="3891f-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="3891f-134">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="3891f-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="3891f-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3891f-135">EXAMPLES</span></span>

### <span data-ttu-id="3891f-136">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3891f-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="3891f-137">Det här kommandot skapar en ny distribution vid det aktuella abonnemanget genom att använda en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="3891f-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="3891f-138">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="3891f-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="3891f-139">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="3891f-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="3891f-140">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="3891f-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="3891f-141">Det här kommandot skapar en ny distribution vid det aktuella abonnemanget genom att använda en anpassad mall och en mallfil på en disk som har konverterats till en i minnet.</span><span class="sxs-lookup"><span data-stu-id="3891f-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="3891f-142">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="3891f-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="3891f-143">Det sista kommandot använder parametern *TemplateObject* för att ange den här hash-tabellen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="3891f-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="3891f-144">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="3891f-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="3891f-145">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3891f-145">PARAMETERS</span></span>

### <span data-ttu-id="3891f-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3891f-146">-ApiVersion</span></span>
<span data-ttu-id="3891f-147">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3891f-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3891f-148">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="3891f-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3891f-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3891f-149">-AsJob</span></span>
<span data-ttu-id="3891f-150">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3891f-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3891f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3891f-151">-DefaultProfile</span></span>
<span data-ttu-id="3891f-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3891f-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3891f-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="3891f-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="3891f-154">Loggnings nivå för distributions fel.</span><span class="sxs-lookup"><span data-stu-id="3891f-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="3891f-155">-Plats</span><span class="sxs-lookup"><span data-stu-id="3891f-155">-Location</span></span>
<span data-ttu-id="3891f-156">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="3891f-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3891f-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="3891f-157">-Name</span></span>
<span data-ttu-id="3891f-158">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3891f-158">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="3891f-159">Endast giltigt när en mall används.</span><span class="sxs-lookup"><span data-stu-id="3891f-159">Only valid when a template is used.</span></span>
<span data-ttu-id="3891f-160">När en mall används, om användaren inte anger ett distributions namn använder du den aktuella tiden, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="3891f-160">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="3891f-161">-För</span><span class="sxs-lookup"><span data-stu-id="3891f-161">-Pre</span></span>
<span data-ttu-id="3891f-162">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3891f-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3891f-163">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3891f-163">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3891f-164">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="3891f-164">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="3891f-165">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="3891f-165">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="3891f-166">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="3891f-166">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3891f-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3891f-167">-TemplateFile</span></span>
<span data-ttu-id="3891f-168">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="3891f-168">Local path to the template file.</span></span>

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

### <span data-ttu-id="3891f-169">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3891f-169">-TemplateObject</span></span>
<span data-ttu-id="3891f-170">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="3891f-170">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3891f-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3891f-171">-TemplateParameterFile</span></span>
<span data-ttu-id="3891f-172">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="3891f-172">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3891f-173">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3891f-173">-TemplateParameterObject</span></span>
<span data-ttu-id="3891f-174">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="3891f-174">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3891f-175">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3891f-175">-TemplateParameterUri</span></span>
<span data-ttu-id="3891f-176">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="3891f-176">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3891f-177">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3891f-177">-TemplateUri</span></span>
<span data-ttu-id="3891f-178">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="3891f-178">Uri to the template file.</span></span>

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

### <span data-ttu-id="3891f-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3891f-179">-Confirm</span></span>
<span data-ttu-id="3891f-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3891f-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3891f-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3891f-181">-WhatIf</span></span>
<span data-ttu-id="3891f-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3891f-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3891f-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3891f-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3891f-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3891f-184">CommonParameters</span></span>
<span data-ttu-id="3891f-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3891f-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3891f-186">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3891f-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3891f-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3891f-187">INPUTS</span></span>

### <span data-ttu-id="3891f-188">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3891f-188">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3891f-189">System. String</span><span class="sxs-lookup"><span data-stu-id="3891f-189">System.String</span></span>

## <span data-ttu-id="3891f-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3891f-190">OUTPUTS</span></span>

### <span data-ttu-id="3891f-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3891f-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3891f-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3891f-192">NOTES</span></span>

## <span data-ttu-id="3891f-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3891f-193">RELATED LINKS</span></span>
