---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 6c64c9defb3905e9851e79da5303b68e98514f44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930829"
---
# <span data-ttu-id="34a44-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="34a44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34a44-102">SYNOPSIS</span></span>
<span data-ttu-id="34a44-103">Lägger till en Azure-distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="34a44-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34a44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34a44-104">SYNTAX</span></span>

### <span data-ttu-id="34a44-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="34a44-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="34a44-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="34a44-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="34a44-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="34a44-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="34a44-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="34a44-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a44-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="34a44-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a44-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34a44-113">DESCRIPTION</span></span>
<span data-ttu-id="34a44-114">**New-AzureRmResourceGroupDeployment** cmdlet lägger till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="34a44-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="34a44-115">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="34a44-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="34a44-116">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas, en webbplats, en virtuell dator eller ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="34a44-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="34a44-117">En Azure-adressresurs är en samling Azure-resurser som distribueras som en enhet, till exempel en webbplats, databas server och databaser som krävs för en finansiell webbplats.</span><span class="sxs-lookup"><span data-stu-id="34a44-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="34a44-118">Vid distribution av resurs grupper används en mall för att lägga till resurser i en resurs grupp och de publicerar dem så att de är tillgängliga i Azure.</span><span class="sxs-lookup"><span data-stu-id="34a44-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="34a44-119">Använd New-AzureRmResource cmdlet för att lägga till resurser i en resurs grupp utan att använda en mall.</span><span class="sxs-lookup"><span data-stu-id="34a44-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="34a44-120">Om du vill lägga till en resurs grupps distribution anger du namnet på en befintlig resurs grupp och en mall för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="34a44-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="34a44-121">En mall för en resurs grupp är en JSON-sträng som representerar en resurs grupp för en komplex molnbaserad tjänst, till exempel en webb Portal.</span><span class="sxs-lookup"><span data-stu-id="34a44-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="34a44-122">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="34a44-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="34a44-123">Du kan hitta många mallar i Azure Template-galleriet, eller så kan du skapa egna mallar.</span><span class="sxs-lookup"><span data-stu-id="34a44-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="34a44-124">Du kan använda cmdleten **Get-AzureRmResourceGroupGalleryTemplate** för att hitta en mall i galleriet.</span><span class="sxs-lookup"><span data-stu-id="34a44-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="34a44-125">Om du vill använda en anpassad mall för att skapa en resurs grupp anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="34a44-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="34a44-126">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="34a44-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="34a44-127">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="34a44-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="34a44-128">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="34a44-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="34a44-129">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="34a44-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="34a44-130">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="34a44-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="34a44-131">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34a44-131">EXAMPLES</span></span>

### <span data-ttu-id="34a44-132">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="34a44-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="34a44-133">Det här kommandot skapar en ny distribution med hjälp av en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="34a44-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="34a44-134">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="34a44-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="34a44-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34a44-135">PARAMETERS</span></span>

### <span data-ttu-id="34a44-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34a44-136">-ApiVersion</span></span>
<span data-ttu-id="34a44-137">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="34a44-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="34a44-138">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="34a44-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="34a44-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34a44-139">-AsJob</span></span>
<span data-ttu-id="34a44-140">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="34a44-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34a44-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a44-141">-DefaultProfile</span></span>
<span data-ttu-id="34a44-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34a44-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34a44-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="34a44-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="34a44-144">Anger en loggnings nivå för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="34a44-144">Specifies a debug log level.</span></span>
<span data-ttu-id="34a44-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34a44-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34a44-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="34a44-146">RequestContent</span></span>
- <span data-ttu-id="34a44-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="34a44-147">ResponseContent</span></span>
- <span data-ttu-id="34a44-148">Alla</span><span class="sxs-lookup"><span data-stu-id="34a44-148">All</span></span>
- <span data-ttu-id="34a44-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="34a44-149">None</span></span>

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

### <span data-ttu-id="34a44-150">-Force</span><span class="sxs-lookup"><span data-stu-id="34a44-150">-Force</span></span>
<span data-ttu-id="34a44-151">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="34a44-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34a44-152">-Mode</span><span class="sxs-lookup"><span data-stu-id="34a44-152">-Mode</span></span>
<span data-ttu-id="34a44-153">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="34a44-153">Specifies the deployment mode.</span></span> <span data-ttu-id="34a44-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34a44-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34a44-155">Kunna</span><span class="sxs-lookup"><span data-stu-id="34a44-155">Complete</span></span>
- <span data-ttu-id="34a44-156">I läget fullständig tas resurser som finns i resurs gruppen bort, men inte i mallen.</span><span class="sxs-lookup"><span data-stu-id="34a44-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="34a44-157">I stegvist läge blir resurs hanteraren oförändrade resurser som finns i resurs gruppen men som inte har angetts i mallen.</span><span class="sxs-lookup"><span data-stu-id="34a44-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a44-158">-Namn</span><span class="sxs-lookup"><span data-stu-id="34a44-158">-Name</span></span>
<span data-ttu-id="34a44-159">Anger namnet på den resurs grupps distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="34a44-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="34a44-160">-För</span><span class="sxs-lookup"><span data-stu-id="34a44-160">-Pre</span></span>
<span data-ttu-id="34a44-161">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="34a44-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="34a44-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a44-162">-ResourceGroupName</span></span>
<span data-ttu-id="34a44-163">Anger namnet på resurs gruppen som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="34a44-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="34a44-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="34a44-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="34a44-165">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="34a44-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="34a44-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="34a44-167">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="34a44-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="34a44-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="34a44-168">-TemplateFile</span></span>
<span data-ttu-id="34a44-169">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="34a44-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="34a44-170">Det kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel en som skapats med cmdleten **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="34a44-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="34a44-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="34a44-171">-TemplateParameterFile</span></span>
<span data-ttu-id="34a44-172">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="34a44-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="34a44-173">Om en mall har parametrar måste du ange parameter värden med parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="34a44-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="34a44-174">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="34a44-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="34a44-175">Om du vill använda dynamiska parametrar skriver du ett minus tecken (-) för att ange ett parameter namn och använder sedan TABB-tangenten för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="34a44-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a44-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="34a44-176">-TemplateParameterObject</span></span>
<span data-ttu-id="34a44-177">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="34a44-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="34a44-178">Om du behöver hjälp med hash-tabeller i Windows PowerShell skriver du `Get-Help about_Hash_Tables` :</span><span class="sxs-lookup"><span data-stu-id="34a44-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="34a44-179">Om en mall har parametrar måste du ange parameter värden.</span><span class="sxs-lookup"><span data-stu-id="34a44-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="34a44-180">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="34a44-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a44-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="34a44-181">-TemplateParameterUri</span></span>
<span data-ttu-id="34a44-182">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="34a44-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a44-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="34a44-183">-TemplateUri</span></span>
<span data-ttu-id="34a44-184">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="34a44-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="34a44-185">Denna fil kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel genom att använda **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="34a44-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="34a44-186">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34a44-186">-Confirm</span></span>
<span data-ttu-id="34a44-187">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34a44-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a44-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a44-188">-WhatIf</span></span>
<span data-ttu-id="34a44-189">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34a44-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a44-190">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34a44-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a44-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a44-191">CommonParameters</span></span>
<span data-ttu-id="34a44-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a44-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a44-193">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a44-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a44-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34a44-194">INPUTS</span></span>

### <span data-ttu-id="34a44-195">Ingen</span><span class="sxs-lookup"><span data-stu-id="34a44-195">None</span></span>

## <span data-ttu-id="34a44-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34a44-196">OUTPUTS</span></span>

### <span data-ttu-id="34a44-197">Microsoft. Azure. commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="34a44-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34a44-198">NOTES</span></span>

## <span data-ttu-id="34a44-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34a44-199">RELATED LINKS</span></span>

[<span data-ttu-id="34a44-200">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="34a44-201">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="34a44-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="34a44-202">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34a44-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="34a44-203">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="34a44-204">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="34a44-205">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="34a44-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


