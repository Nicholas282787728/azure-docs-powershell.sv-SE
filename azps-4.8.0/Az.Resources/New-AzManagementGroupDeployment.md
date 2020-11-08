---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: c15a7fca43568e63b8e7407b5c2048d03b9b6bc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261731"
---
# <span data-ttu-id="ca40c-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ca40c-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ca40c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca40c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca40c-103">Skapa en distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="ca40c-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="ca40c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca40c-104">SYNTAX</span></span>

### <span data-ttu-id="ca40c-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="ca40c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca40c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca40c-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca40c-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca40c-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca40c-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca40c-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca40c-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca40c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ca40c-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca40c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ca40c-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca40c-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca40c-117">DESCRIPTION</span></span>
<span data-ttu-id="ca40c-118">Cmdleten **New-AzManagementGroupDeployment** lägger till en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="ca40c-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="ca40c-119">Om du vill lägga till en distribution i en hanterings grupp anger du hanterings grupp, plats och en mall.</span><span class="sxs-lookup"><span data-stu-id="ca40c-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="ca40c-120">Platsen säger att Azure Resource Manager lagrar distributions data.</span><span class="sxs-lookup"><span data-stu-id="ca40c-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="ca40c-121">Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="ca40c-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="ca40c-122">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="ca40c-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="ca40c-123">Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="ca40c-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="ca40c-124">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ca40c-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="ca40c-125">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="ca40c-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="ca40c-126">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="ca40c-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="ca40c-127">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="ca40c-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="ca40c-128">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="ca40c-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="ca40c-129">Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzResourceGroupDeployment** som skapar en distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ca40c-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="ca40c-130">Om du vill lägga till resurser i en prenumeration använder du den **nya-AzSubscriptionDeployment** som skapar en distribution i prenumerations omfattning, som distribuerar abonnemangs nivå resurser.</span><span class="sxs-lookup"><span data-stu-id="ca40c-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="ca40c-131">Om du vill lägga till resurser i klient omfattningen använder du den **nya-AzTenantDeployment** som skapar en distribution med klientens omfång.</span><span class="sxs-lookup"><span data-stu-id="ca40c-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="ca40c-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca40c-132">EXAMPLES</span></span>

### <span data-ttu-id="ca40c-133">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="ca40c-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="ca40c-134">Det här kommandot skapar en ny distribution i gruppen "myMG" genom att använda en anpassad mall och en mallfil på disk, med en definierad parameter.</span><span class="sxs-lookup"><span data-stu-id="ca40c-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="ca40c-135">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="ca40c-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="ca40c-136">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="ca40c-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="ca40c-137">Det här kommandot skapar en ny distribution i gruppen "myMG" genom att använda en anpassad mall och en mallfil på en disk som har konverterats till en hash-gruppgrupp.</span><span class="sxs-lookup"><span data-stu-id="ca40c-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="ca40c-138">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="ca40c-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="ca40c-139">Det sista kommandot använder parametern *TemplateObject* för att ange den här hash-tabellen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="ca40c-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="ca40c-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca40c-140">PARAMETERS</span></span>

### <span data-ttu-id="ca40c-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ca40c-141">-ApiVersion</span></span>
<span data-ttu-id="ca40c-142">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ca40c-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ca40c-143">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="ca40c-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ca40c-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca40c-144">-AsJob</span></span>
<span data-ttu-id="ca40c-145">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ca40c-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca40c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca40c-146">-DefaultProfile</span></span>
<span data-ttu-id="ca40c-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca40c-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca40c-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="ca40c-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="ca40c-149">Loggnings nivå för distributions fel.</span><span class="sxs-lookup"><span data-stu-id="ca40c-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="ca40c-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="ca40c-150">-Location</span></span>
<span data-ttu-id="ca40c-151">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="ca40c-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ca40c-152">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ca40c-152">-ManagementGroupId</span></span>
<span data-ttu-id="ca40c-153">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="ca40c-153">The management group ID.</span></span>

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

### <span data-ttu-id="ca40c-154">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca40c-154">-Name</span></span>
<span data-ttu-id="ca40c-155">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ca40c-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="ca40c-156">Om inget anges används standardvärdet för mallnamnet när en mallfil tillhandahålls; Standardvärdet för den aktuella tiden när ett mallfiler tillhandahålls, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="ca40c-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="ca40c-157">-För</span><span class="sxs-lookup"><span data-stu-id="ca40c-157">-Pre</span></span>
<span data-ttu-id="ca40c-158">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ca40c-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca40c-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ca40c-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ca40c-160">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ca40c-161">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ca40c-162">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="ca40c-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ca40c-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ca40c-163">-Tag</span></span>
<span data-ttu-id="ca40c-164">Taggarna som ska läggas till i distributionen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="ca40c-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ca40c-165">-TemplateFile</span></span>
<span data-ttu-id="ca40c-166">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="ca40c-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-167">-TemplateObject</span></span>
<span data-ttu-id="ca40c-168">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ca40c-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca40c-169">-TemplateParameterFile</span></span>
<span data-ttu-id="ca40c-170">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="ca40c-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ca40c-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-171">-TemplateParameterObject</span></span>
<span data-ttu-id="ca40c-172">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ca40c-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ca40c-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca40c-173">-TemplateParameterUri</span></span>
<span data-ttu-id="ca40c-174">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ca40c-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ca40c-175">-TemplateUri</span></span>
<span data-ttu-id="ca40c-176">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="ca40c-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="ca40c-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="ca40c-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="ca40c-178">Kommaavgränsade resurs ändrings typer som ska uteslutas från What-If resultat.</span><span class="sxs-lookup"><span data-stu-id="ca40c-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="ca40c-179">Tillämpbar när växeln-WhatIf eller-Confirm har ställts in.</span><span class="sxs-lookup"><span data-stu-id="ca40c-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="ca40c-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="ca40c-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="ca40c-181">What-If resultat format.</span><span class="sxs-lookup"><span data-stu-id="ca40c-181">The What-If result format.</span></span> <span data-ttu-id="ca40c-182">Tillämpbar när växeln-WhatIf eller-Confirm har ställts in.</span><span class="sxs-lookup"><span data-stu-id="ca40c-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="ca40c-183">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca40c-183">-Confirm</span></span>
<span data-ttu-id="ca40c-184">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca40c-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca40c-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca40c-185">-WhatIf</span></span>
<span data-ttu-id="ca40c-186">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca40c-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca40c-187">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca40c-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca40c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca40c-188">CommonParameters</span></span>
<span data-ttu-id="ca40c-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca40c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca40c-190">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca40c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca40c-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca40c-191">INPUTS</span></span>

### <span data-ttu-id="ca40c-192">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ca40c-192">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ca40c-193">System. String</span><span class="sxs-lookup"><span data-stu-id="ca40c-193">System.String</span></span>

## <span data-ttu-id="ca40c-194">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca40c-194">OUTPUTS</span></span>

### <span data-ttu-id="ca40c-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ca40c-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ca40c-196">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca40c-196">NOTES</span></span>

## <span data-ttu-id="ca40c-197">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca40c-197">RELATED LINKS</span></span>
