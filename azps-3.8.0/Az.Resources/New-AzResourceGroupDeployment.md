---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: cf0b8f4897832d84630c98a8518b3c10eefcf5e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091221"
---
# <span data-ttu-id="c78d5-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c78d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c78d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c78d5-103">Lägger till en Azure-distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c78d5-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="c78d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c78d5-104">SYNTAX</span></span>

### <span data-ttu-id="c78d5-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="c78d5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c78d5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c78d5-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c78d5-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c78d5-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c78d5-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c78d5-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c78d5-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c78d5-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c78d5-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c78d5-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78d5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c78d5-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c78d5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c78d5-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c78d5-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c78d5-117">DESCRIPTION</span></span>
<span data-ttu-id="c78d5-118">**New-AzResourceGroupDeployment** cmdlet lägger till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c78d5-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="c78d5-119">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="c78d5-120">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas, en webbplats, en virtuell dator eller ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c78d5-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="c78d5-121">En Azure-adressresurs är en samling Azure-resurser som distribueras som en enhet, till exempel en webbplats, databas server och databaser som krävs för en finansiell webbplats.</span><span class="sxs-lookup"><span data-stu-id="c78d5-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="c78d5-122">Vid distribution av resurs grupper används en mall för att lägga till resurser i en resurs grupp och de publicerar dem så att de är tillgängliga i Azure.</span><span class="sxs-lookup"><span data-stu-id="c78d5-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="c78d5-123">Använd New-AzResource cmdlet för att lägga till resurser i en resurs grupp utan att använda en mall.</span><span class="sxs-lookup"><span data-stu-id="c78d5-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="c78d5-124">Om du vill lägga till en resurs grupps distribution anger du namnet på en befintlig resurs grupp och en mall för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c78d5-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="c78d5-125">En mall för en resurs grupp är en JSON-sträng som representerar en resurs grupp för en komplex molnbaserad tjänst, till exempel en webb Portal.</span><span class="sxs-lookup"><span data-stu-id="c78d5-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="c78d5-126">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="c78d5-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="c78d5-127">Du kan hitta många mallar i Azure Template-galleriet, eller så kan du skapa egna mallar.</span><span class="sxs-lookup"><span data-stu-id="c78d5-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="c78d5-128">Om du vill använda en anpassad mall för att skapa en resurs grupp anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="c78d5-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="c78d5-129">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c78d5-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="c78d5-130">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="c78d5-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="c78d5-131">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="c78d5-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="c78d5-132">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="c78d5-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="c78d5-133">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="c78d5-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="c78d5-134">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c78d5-134">EXAMPLES</span></span>

### <span data-ttu-id="c78d5-135">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="c78d5-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="c78d5-136">Det här kommandot skapar en ny distribution med hjälp av en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="c78d5-136">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="c78d5-137">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="c78d5-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="c78d5-138">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="c78d5-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c78d5-139">Det här kommandot skapar en ny distribution genom att använda en anpassad och en mallfil på en disk som har konverterats till en hash med inbyggd i minnet.</span><span class="sxs-lookup"><span data-stu-id="c78d5-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="c78d5-140">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="c78d5-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="c78d5-141">Det sista kommandot använder parametern *TemplateObject* för att ange en hash och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="c78d5-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="c78d5-142">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c78d5-142">PARAMETERS</span></span>

### <span data-ttu-id="c78d5-143">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c78d5-143">-ApiVersion</span></span>
<span data-ttu-id="c78d5-144">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="c78d5-144">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c78d5-145">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-145">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c78d5-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c78d5-146">-AsJob</span></span>
<span data-ttu-id="c78d5-147">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c78d5-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c78d5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78d5-148">-DefaultProfile</span></span>
<span data-ttu-id="c78d5-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c78d5-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c78d5-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="c78d5-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="c78d5-151">Anger en loggnings nivå för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="c78d5-151">Specifies a debug log level.</span></span>
<span data-ttu-id="c78d5-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c78d5-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c78d5-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="c78d5-153">RequestContent</span></span>
- <span data-ttu-id="c78d5-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="c78d5-154">ResponseContent</span></span>
- <span data-ttu-id="c78d5-155">Alla</span><span class="sxs-lookup"><span data-stu-id="c78d5-155">All</span></span>
- <span data-ttu-id="c78d5-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="c78d5-156">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c78d5-157">-Force</span><span class="sxs-lookup"><span data-stu-id="c78d5-157">-Force</span></span>
<span data-ttu-id="c78d5-158">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c78d5-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c78d5-159">-Mode</span><span class="sxs-lookup"><span data-stu-id="c78d5-159">-Mode</span></span>
<span data-ttu-id="c78d5-160">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="c78d5-160">Specifies the deployment mode.</span></span> <span data-ttu-id="c78d5-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c78d5-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c78d5-162">Fullständig: i läget fullständig tas resurser som finns i resurs gruppen bort, men inte i mallen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="c78d5-163">Stegvis: i stegvist läge blir resurs hanteraren inte oförändrade resurser som finns i resurs gruppen men som inte har angetts i mallen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c78d5-164">-Namn</span><span class="sxs-lookup"><span data-stu-id="c78d5-164">-Name</span></span>
<span data-ttu-id="c78d5-165">Anger namnet på den resurs grupps distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c78d5-165">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="c78d5-166">-För</span><span class="sxs-lookup"><span data-stu-id="c78d5-166">-Pre</span></span>
<span data-ttu-id="c78d5-167">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c78d5-167">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c78d5-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c78d5-168">-ResourceGroupName</span></span>
<span data-ttu-id="c78d5-169">Anger namnet på resurs gruppen som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="c78d5-169">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="c78d5-170">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="c78d5-170">-RollBackDeploymentName</span></span>
<span data-ttu-id="c78d5-171">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="c78d5-171">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c78d5-172">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-172">-RollbackToLastDeployment</span></span>
<span data-ttu-id="c78d5-173">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="c78d5-173">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="c78d5-174">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c78d5-174">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c78d5-175">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-175">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="c78d5-176">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-176">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="c78d5-177">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="c78d5-177">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c78d5-178">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c78d5-178">-TemplateFile</span></span>
<span data-ttu-id="c78d5-179">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="c78d5-179">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="c78d5-180">Det kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel en som skapats med cmdleten **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="c78d5-180">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="c78d5-181">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c78d5-181">-TemplateObject</span></span>
<span data-ttu-id="c78d5-182">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="c78d5-182">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c78d5-183">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c78d5-183">-TemplateParameterFile</span></span>
<span data-ttu-id="c78d5-184">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="c78d5-184">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="c78d5-185">Om en mall har parametrar måste du ange parameter värden med parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="c78d5-185">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="c78d5-186">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="c78d5-186">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="c78d5-187">Om du vill använda dynamiska parametrar skriver du ett minus tecken (-) för att ange ett parameter namn och använder sedan TABB-tangenten för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="c78d5-187">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="c78d5-188">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c78d5-188">-TemplateParameterObject</span></span>
<span data-ttu-id="c78d5-189">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="c78d5-189">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="c78d5-190">Om du behöver hjälp med hash-tabeller i Windows PowerShell skriver du `Get-Help about_Hash_Tables` :</span><span class="sxs-lookup"><span data-stu-id="c78d5-190">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="c78d5-191">Om en mall har parametrar måste du ange parameter värden.</span><span class="sxs-lookup"><span data-stu-id="c78d5-191">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="c78d5-192">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="c78d5-192">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="c78d5-193">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c78d5-193">-TemplateParameterUri</span></span>
<span data-ttu-id="c78d5-194">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="c78d5-194">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="c78d5-195">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c78d5-195">-TemplateUri</span></span>
<span data-ttu-id="c78d5-196">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="c78d5-196">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="c78d5-197">Denna fil kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel genom att använda **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="c78d5-197">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="c78d5-198">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c78d5-198">-Confirm</span></span>
<span data-ttu-id="c78d5-199">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c78d5-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c78d5-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c78d5-200">-WhatIf</span></span>
<span data-ttu-id="c78d5-201">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c78d5-201">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c78d5-202">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c78d5-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c78d5-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78d5-203">CommonParameters</span></span>
<span data-ttu-id="c78d5-204">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78d5-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78d5-205">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c78d5-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78d5-206">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c78d5-206">INPUTS</span></span>

### <span data-ttu-id="c78d5-207">System. String</span><span class="sxs-lookup"><span data-stu-id="c78d5-207">System.String</span></span>

### <span data-ttu-id="c78d5-208">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c78d5-208">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="c78d5-209">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c78d5-209">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c78d5-210">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c78d5-210">OUTPUTS</span></span>

### <span data-ttu-id="c78d5-211">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-211">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="c78d5-212">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c78d5-212">NOTES</span></span>

## <span data-ttu-id="c78d5-213">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c78d5-213">RELATED LINKS</span></span>

[<span data-ttu-id="c78d5-214">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-214">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="c78d5-215">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="c78d5-215">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c78d5-216">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c78d5-216">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="c78d5-217">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-217">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c78d5-218">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-218">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="c78d5-219">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c78d5-219">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


