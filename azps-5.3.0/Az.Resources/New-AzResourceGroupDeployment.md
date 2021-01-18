---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521387"
---
# <span data-ttu-id="a0226-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a0226-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0226-102">SYNOPSIS</span></span>
<span data-ttu-id="a0226-103">Lägger till en Azure-distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0226-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="a0226-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0226-104">SYNTAX</span></span>

### <span data-ttu-id="a0226-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="a0226-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0226-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0226-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0226-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0226-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0226-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0226-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a0226-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a0226-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a0226-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a0226-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0226-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a0226-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0226-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0226-117">DESCRIPTION</span></span>
<span data-ttu-id="a0226-118">**New-AzResourceGroupDeployment** cmdlet lägger till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0226-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="a0226-119">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="a0226-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="a0226-120">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas, en webbplats, en virtuell dator eller ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a0226-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="a0226-121">En Azure-adressresurs är en samling Azure-resurser som distribueras som en enhet, till exempel en webbplats, databas server och databaser som krävs för en finansiell webbplats.</span><span class="sxs-lookup"><span data-stu-id="a0226-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="a0226-122">Vid distribution av resurs grupper används en mall för att lägga till resurser i en resurs grupp och de publicerar dem så att de är tillgängliga i Azure.</span><span class="sxs-lookup"><span data-stu-id="a0226-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="a0226-123">Använd New-AzResource cmdlet för att lägga till resurser i en resurs grupp utan att använda en mall.</span><span class="sxs-lookup"><span data-stu-id="a0226-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="a0226-124">Om du vill lägga till en resurs grupps distribution anger du namnet på en befintlig resurs grupp och en mall för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0226-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="a0226-125">En mall för en resurs grupp är en JSON-sträng som representerar en resurs grupp för en komplex molnbaserad tjänst, till exempel en webb Portal.</span><span class="sxs-lookup"><span data-stu-id="a0226-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="a0226-126">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="a0226-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="a0226-127">Du kan hitta många mallar i Azure Template-galleriet, eller så kan du skapa egna mallar.</span><span class="sxs-lookup"><span data-stu-id="a0226-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="a0226-128">Om du vill använda en anpassad mall för att skapa en resurs grupp anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="a0226-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a0226-129">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a0226-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a0226-130">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a0226-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a0226-131">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="a0226-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a0226-132">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="a0226-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a0226-133">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="a0226-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="a0226-134">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0226-134">EXAMPLES</span></span>

### <span data-ttu-id="a0226-135">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="a0226-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="a0226-136">Det här kommandot skapar en ny distribution med hjälp av en anpassad mall och en mallfil på disk, med en definierad tagg-parameter.</span><span class="sxs-lookup"><span data-stu-id="a0226-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="a0226-137">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="a0226-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a0226-138">Exempel 2: använda ett anpassat mallfiler och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="a0226-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a0226-139">Det här kommandot skapar en ny distribution genom att använda en anpassad och en mallfil på en disk som har konverterats till en hash med inbyggd i minnet.</span><span class="sxs-lookup"><span data-stu-id="a0226-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="a0226-140">De två första kommandona läser texten för mallfilen på hård disken och konverterar den till en hash i minnet.</span><span class="sxs-lookup"><span data-stu-id="a0226-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="a0226-141">Det sista kommandot använder parametern *TemplateObject* för att ange en hash och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="a0226-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a0226-142">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a0226-142">Example 3</span></span>

<span data-ttu-id="a0226-143">Lägger till en Azure-distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0226-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="a0226-144">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="a0226-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="a0226-145">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0226-145">PARAMETERS</span></span>

### <span data-ttu-id="a0226-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0226-146">-AsJob</span></span>
<span data-ttu-id="a0226-147">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a0226-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0226-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0226-148">-DefaultProfile</span></span>
<span data-ttu-id="a0226-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0226-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0226-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a0226-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a0226-151">Anger en loggnings nivå för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="a0226-151">Specifies a debug log level.</span></span>
<span data-ttu-id="a0226-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a0226-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0226-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="a0226-153">RequestContent</span></span>
- <span data-ttu-id="a0226-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="a0226-154">ResponseContent</span></span>
- <span data-ttu-id="a0226-155">Alla</span><span class="sxs-lookup"><span data-stu-id="a0226-155">All</span></span>
- <span data-ttu-id="a0226-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="a0226-156">None</span></span>

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

### <span data-ttu-id="a0226-157">-Force</span><span class="sxs-lookup"><span data-stu-id="a0226-157">-Force</span></span>
<span data-ttu-id="a0226-158">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0226-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0226-159">-Mode</span><span class="sxs-lookup"><span data-stu-id="a0226-159">-Mode</span></span>
<span data-ttu-id="a0226-160">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="a0226-160">Specifies the deployment mode.</span></span> <span data-ttu-id="a0226-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a0226-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0226-162">Fullständig: i läget fullständig tas resurser som finns i resurs gruppen bort, men inte i mallen.</span><span class="sxs-lookup"><span data-stu-id="a0226-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="a0226-163">Stegvis: i stegvist läge blir resurs hanteraren inte oförändrade resurser som finns i resurs gruppen men som inte har angetts i mallen.</span><span class="sxs-lookup"><span data-stu-id="a0226-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="a0226-164">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0226-164">-Name</span></span>
<span data-ttu-id="a0226-165">Namnet på den distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a0226-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="a0226-166">Om inget anges används standardvärdet för mallnamnet när en mallfil tillhandahålls; Standardvärdet för den aktuella tiden när ett mallfiler tillhandahålls, till exempel "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="a0226-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="a0226-167">-För</span><span class="sxs-lookup"><span data-stu-id="a0226-167">-Pre</span></span>
<span data-ttu-id="a0226-168">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a0226-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a0226-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0226-169">-ResourceGroupName</span></span>
<span data-ttu-id="a0226-170">Anger namnet på resurs gruppen som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="a0226-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="a0226-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a0226-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="a0226-172">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="a0226-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="a0226-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a0226-174">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="a0226-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a0226-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a0226-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a0226-176">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="a0226-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a0226-177">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="a0226-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a0226-178">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="a0226-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a0226-179">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a0226-179">-Tag</span></span>
<span data-ttu-id="a0226-180">Taggarna som ska läggas till i distributionen.</span><span class="sxs-lookup"><span data-stu-id="a0226-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="a0226-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a0226-181">-TemplateFile</span></span>
<span data-ttu-id="a0226-182">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="a0226-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="a0226-183">Det kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel en som skapats med cmdleten **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="a0226-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="a0226-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a0226-184">-TemplateObject</span></span>
<span data-ttu-id="a0226-185">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="a0226-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a0226-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0226-186">-TemplateParameterFile</span></span>
<span data-ttu-id="a0226-187">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="a0226-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="a0226-188">Om en mall har parametrar måste du ange parameter värden med parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a0226-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a0226-189">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="a0226-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a0226-190">Om du vill använda dynamiska parametrar skriver du ett minus tecken (-) för att ange ett parameter namn och använder sedan TABB-tangenten för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a0226-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="a0226-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0226-191">-TemplateParameterObject</span></span>
<span data-ttu-id="a0226-192">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="a0226-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="a0226-193">Om du behöver hjälp med hash-tabeller i Windows PowerShell skriver du `Get-Help about_Hash_Tables` :</span><span class="sxs-lookup"><span data-stu-id="a0226-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a0226-194">Om en mall har parametrar måste du ange parameter värden.</span><span class="sxs-lookup"><span data-stu-id="a0226-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="a0226-195">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="a0226-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="a0226-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a0226-196">-TemplateParameterUri</span></span>
<span data-ttu-id="a0226-197">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="a0226-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a0226-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a0226-198">-TemplateUri</span></span>
<span data-ttu-id="a0226-199">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="a0226-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="a0226-200">Denna fil kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel genom att använda **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="a0226-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="a0226-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="a0226-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="a0226-202">Kommaavgränsade resurs ändrings typer som ska uteslutas från What-If resultat.</span><span class="sxs-lookup"><span data-stu-id="a0226-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="a0226-203">Tillämpbar när växeln-WhatIf eller-Confirm har ställts in.</span><span class="sxs-lookup"><span data-stu-id="a0226-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="a0226-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="a0226-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="a0226-205">What-If resultat format.</span><span class="sxs-lookup"><span data-stu-id="a0226-205">The What-If result format.</span></span>

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

### <span data-ttu-id="a0226-206">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0226-206">-Confirm</span></span>
<span data-ttu-id="a0226-207">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0226-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0226-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0226-208">-WhatIf</span></span>
<span data-ttu-id="a0226-209">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0226-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0226-210">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0226-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0226-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0226-211">CommonParameters</span></span>
<span data-ttu-id="a0226-212">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0226-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0226-213">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0226-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0226-214">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0226-214">INPUTS</span></span>

### <span data-ttu-id="a0226-215">System. String</span><span class="sxs-lookup"><span data-stu-id="a0226-215">System.String</span></span>

### <span data-ttu-id="a0226-216">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a0226-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a0226-217">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a0226-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0226-218">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0226-218">OUTPUTS</span></span>

### <span data-ttu-id="a0226-219">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a0226-220">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0226-220">NOTES</span></span>

## <span data-ttu-id="a0226-221">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0226-221">RELATED LINKS</span></span>

[<span data-ttu-id="a0226-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0226-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a0226-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="a0226-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0226-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a0226-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0226-226">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0226-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0226-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)