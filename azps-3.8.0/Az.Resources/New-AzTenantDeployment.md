---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926453"
---
# <span data-ttu-id="cb094-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cb094-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="cb094-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb094-102">SYNOPSIS</span></span>
<span data-ttu-id="cb094-103">Skapa en distribution med klient-scope</span><span class="sxs-lookup"><span data-stu-id="cb094-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="cb094-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb094-104">SYNTAX</span></span>

### <span data-ttu-id="cb094-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="cb094-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb094-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb094-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb094-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb094-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb094-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb094-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb094-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb094-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb094-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb094-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb094-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb094-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb094-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb094-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb094-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb094-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb094-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb094-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb094-117">DESCRIPTION</span></span>
<span data-ttu-id="cb094-118">Cmdleten **New-AzTenantDeployment** lägger till en distribution med den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="cb094-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="cb094-119">Om du vill lägga till en distribution vid klient omfattningen anger du platsen och en mall.</span><span class="sxs-lookup"><span data-stu-id="cb094-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="cb094-120">Platsen säger att Azure Resource Manager lagrar distributions data.</span><span class="sxs-lookup"><span data-stu-id="cb094-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="cb094-121">Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="cb094-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="cb094-122">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="cb094-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="cb094-123">Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="cb094-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="cb094-124">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="cb094-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="cb094-125">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="cb094-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="cb094-126">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="cb094-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="cb094-127">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="cb094-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="cb094-128">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="cb094-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="cb094-129">Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzResourceGroupDeployment** som skapar en distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cb094-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="cb094-130">Om du vill lägga till resurser i en prenumeration använder du den **nya-AzSubscriptionDeployment** som skapar en distribution i prenumerations omfattning, som distribuerar abonnemangs nivå resurser.</span><span class="sxs-lookup"><span data-stu-id="cb094-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="cb094-131">Om du vill lägga till resurser i en hanterings grupp använder du den **nya-AzManagementGroupDeployment** som skapar en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="cb094-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="cb094-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb094-132">EXAMPLES</span></span>

### <span data-ttu-id="cb094-133">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="cb094-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="cb094-134">Det här kommandot skapar en ny distribution med den aktuella klient organisations omfattningen genom att använda en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="cb094-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="cb094-135">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="cb094-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="cb094-136">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="cb094-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="cb094-137">Det här kommandot skapar en ny distribution hos den aktuella klient organisationen med hjälp av en anpassad mall och en mallfil på en disk som har konverterats till en i minnet.</span><span class="sxs-lookup"><span data-stu-id="cb094-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="cb094-138">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="cb094-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="cb094-139">Det sista kommandot använder parametern *TemplateObject* för att ange den här hash-tabellen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="cb094-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="cb094-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb094-140">PARAMETERS</span></span>

### <span data-ttu-id="cb094-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cb094-141">-ApiVersion</span></span>
<span data-ttu-id="cb094-142">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cb094-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="cb094-143">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="cb094-143">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb094-144">-AsJob</span></span>
<span data-ttu-id="cb094-145">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cb094-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb094-146">-DefaultProfile</span></span>
<span data-ttu-id="cb094-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb094-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="cb094-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="cb094-149">Loggnings nivå för distributions fel.</span><span class="sxs-lookup"><span data-stu-id="cb094-149">The deployment debug log level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="cb094-150">-Location</span></span>
<span data-ttu-id="cb094-151">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="cb094-151">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb094-152">-Name</span></span>
<span data-ttu-id="cb094-153">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cb094-153">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="cb094-154">Endast giltigt när en mall används.</span><span class="sxs-lookup"><span data-stu-id="cb094-154">Only valid when a template is used.</span></span>
<span data-ttu-id="cb094-155">När en mall används, om användaren inte anger ett distributions namn använder du den aktuella tiden, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="cb094-155">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-156">-För</span><span class="sxs-lookup"><span data-stu-id="cb094-156">-Pre</span></span>
<span data-ttu-id="cb094-157">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cb094-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-158">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="cb094-158">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="cb094-159">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="cb094-159">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="cb094-160">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="cb094-160">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="cb094-161">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="cb094-161">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="cb094-162">-TemplateFile</span></span>
<span data-ttu-id="cb094-163">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="cb094-163">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="cb094-164">-TemplateObject</span></span>
<span data-ttu-id="cb094-165">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="cb094-165">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb094-166">-TemplateParameterFile</span></span>
<span data-ttu-id="cb094-167">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="cb094-167">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb094-168">-TemplateParameterObject</span></span>
<span data-ttu-id="cb094-169">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cb094-169">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb094-170">-TemplateParameterUri</span></span>
<span data-ttu-id="cb094-171">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="cb094-171">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="cb094-172">-TemplateUri</span></span>
<span data-ttu-id="cb094-173">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="cb094-173">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-174">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb094-174">-Confirm</span></span>
<span data-ttu-id="cb094-175">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb094-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb094-176">-WhatIf</span></span>
<span data-ttu-id="cb094-177">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb094-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb094-178">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb094-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb094-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb094-179">CommonParameters</span></span>
<span data-ttu-id="cb094-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb094-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb094-181">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb094-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb094-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb094-182">INPUTS</span></span>

### <span data-ttu-id="cb094-183">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cb094-183">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cb094-184">System. String</span><span class="sxs-lookup"><span data-stu-id="cb094-184">System.String</span></span>

## <span data-ttu-id="cb094-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb094-185">OUTPUTS</span></span>

### <span data-ttu-id="cb094-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="cb094-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="cb094-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb094-187">NOTES</span></span>

## <span data-ttu-id="cb094-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb094-188">RELATED LINKS</span></span>
