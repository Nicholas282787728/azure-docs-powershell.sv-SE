---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 87b911f480e5bd3186b956f5d9529afbef1e4582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930469"
---
# <span data-ttu-id="f5a31-101">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a31-101">New-AzureRmDeployment</span></span>

## <span data-ttu-id="f5a31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5a31-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a31-103">Skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="f5a31-103">Creat a deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5a31-104">SYNTAX</span></span>

### <span data-ttu-id="f5a31-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="f5a31-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f5a31-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f5a31-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f5a31-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f5a31-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f5a31-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f5a31-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a31-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f5a31-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a31-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5a31-113">DESCRIPTION</span></span>
<span data-ttu-id="f5a31-114">Cmdleten **New-AzureRmDeployment** lägger till en distribution i den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-114">The **New-AzureRmDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="f5a31-115">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="f5a31-116">En Azure-resurs är en användardefinierad Azure-enhet.</span><span class="sxs-lookup"><span data-stu-id="f5a31-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="f5a31-117">En resurs kan finnas i en resurs grupp, till exempel databas server, databas, webbplats, virtuell dator eller lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f5a31-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="f5a31-118">Eller så kan det vara en prenumerations nivå resurs, till exempel roll definition, princip definition etc.</span><span class="sxs-lookup"><span data-stu-id="f5a31-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="f5a31-119">Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzureRmDeployment** som skapar en distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f5a31-119">To add resources to a resource group, use the **New-AzureRmDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="f5a31-120">Cmdleten **New-AzureRmDeployment** skapar en distribution vid den aktuella prenumerationens omfattning, som distribuerar abonnemangs nivå resurser.</span><span class="sxs-lookup"><span data-stu-id="f5a31-120">The **New-AzureRmDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="f5a31-121">Om du vill lägga till en distribution vid abonnemang anger du platsen och en mall.</span><span class="sxs-lookup"><span data-stu-id="f5a31-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="f5a31-122">Platsen säger att Azure Resource Manager lagrar distributions data.</span><span class="sxs-lookup"><span data-stu-id="f5a31-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="f5a31-123">Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="f5a31-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="f5a31-124">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="f5a31-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="f5a31-125">Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="f5a31-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="f5a31-126">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f5a31-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="f5a31-127">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="f5a31-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f5a31-128">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="f5a31-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="f5a31-129">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="f5a31-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="f5a31-130">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="f5a31-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="f5a31-131">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5a31-131">EXAMPLES</span></span>

### <span data-ttu-id="f5a31-132">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="f5a31-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="f5a31-133">Det här kommandot skapar en ny distribution vid det aktuella abonnemanget genom att använda en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="f5a31-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="f5a31-134">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="f5a31-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="f5a31-135">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="f5a31-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5a31-136">PARAMETERS</span></span>

### <span data-ttu-id="f5a31-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5a31-137">-ApiVersion</span></span>
<span data-ttu-id="f5a31-138">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f5a31-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5a31-139">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f5a31-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f5a31-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5a31-140">-AsJob</span></span>
<span data-ttu-id="f5a31-141">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f5a31-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5a31-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a31-142">-DefaultProfile</span></span>
<span data-ttu-id="f5a31-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a31-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a31-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="f5a31-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="f5a31-145">Loggnings nivå för distributions fel.</span><span class="sxs-lookup"><span data-stu-id="f5a31-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="f5a31-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="f5a31-146">-Location</span></span>
<span data-ttu-id="f5a31-147">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="f5a31-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f5a31-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5a31-148">-Name</span></span>
<span data-ttu-id="f5a31-149">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f5a31-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="f5a31-150">Endast giltigt när en mall används.</span><span class="sxs-lookup"><span data-stu-id="f5a31-150">Only valid when a template is used.</span></span>
<span data-ttu-id="f5a31-151">När en mall används, om användaren inte anger ett distributions namn använder du den aktuella tiden, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="f5a31-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="f5a31-152">-För</span><span class="sxs-lookup"><span data-stu-id="f5a31-152">-Pre</span></span>
<span data-ttu-id="f5a31-153">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f5a31-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f5a31-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f5a31-154">-TemplateFile</span></span>
<span data-ttu-id="f5a31-155">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="f5a31-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f5a31-156">-TemplateParameterFile</span></span>
<span data-ttu-id="f5a31-157">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="f5a31-157">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a31-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f5a31-158">-TemplateParameterObject</span></span>
<span data-ttu-id="f5a31-159">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f5a31-159">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a31-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f5a31-160">-TemplateParameterUri</span></span>
<span data-ttu-id="f5a31-161">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-161">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a31-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f5a31-162">-TemplateUri</span></span>
<span data-ttu-id="f5a31-163">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="f5a31-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="f5a31-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5a31-164">-Confirm</span></span>
<span data-ttu-id="f5a31-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5a31-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a31-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a31-166">-WhatIf</span></span>
<span data-ttu-id="f5a31-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5a31-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a31-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5a31-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a31-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a31-169">CommonParameters</span></span>
<span data-ttu-id="f5a31-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a31-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a31-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a31-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a31-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5a31-172">INPUTS</span></span>

### <span data-ttu-id="f5a31-173">System. String</span><span class="sxs-lookup"><span data-stu-id="f5a31-173">System.String</span></span>
<span data-ttu-id="f5a31-174">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f5a31-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5a31-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5a31-175">OUTPUTS</span></span>

### <span data-ttu-id="f5a31-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a31-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f5a31-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5a31-177">NOTES</span></span>

## <span data-ttu-id="f5a31-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5a31-178">RELATED LINKS</span></span>
