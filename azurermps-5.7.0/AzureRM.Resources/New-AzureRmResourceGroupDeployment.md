---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575530"
---
# <span data-ttu-id="db2b2-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="db2b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="db2b2-103">Lägger till en Azure-distribution i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="db2b2-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db2b2-104">SYNTAX</span></span>

### <span data-ttu-id="db2b2-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="db2b2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2b2-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db2b2-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2b2-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db2b2-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2b2-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db2b2-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2b2-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db2b2-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2b2-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db2b2-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2b2-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db2b2-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db2b2-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="db2b2-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2b2-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db2b2-113">DESCRIPTION</span></span>
<span data-ttu-id="db2b2-114">**New-AzureRmResourceGroupDeployment** cmdlet lägger till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="db2b2-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="db2b2-115">Detta inkluderar de resurser som krävs för distributionen.</span><span class="sxs-lookup"><span data-stu-id="db2b2-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="db2b2-116">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas, en webbplats, en virtuell dator eller ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="db2b2-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="db2b2-117">En Azure-adressresurs är en samling Azure-resurser som distribueras som en enhet, till exempel en webbplats, databas server och databaser som krävs för en finansiell webbplats.</span><span class="sxs-lookup"><span data-stu-id="db2b2-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="db2b2-118">Vid distribution av resurs grupper används en mall för att lägga till resurser i en resurs grupp och de publicerar dem så att de är tillgängliga i Azure.</span><span class="sxs-lookup"><span data-stu-id="db2b2-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="db2b2-119">Använd New-AzureRmResource cmdlet för att lägga till resurser i en resurs grupp utan att använda en mall.</span><span class="sxs-lookup"><span data-stu-id="db2b2-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="db2b2-120">Om du vill lägga till en resurs grupps distribution anger du namnet på en befintlig resurs grupp och en mall för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="db2b2-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="db2b2-121">En mall för en resurs grupp är en JSON-sträng som representerar en resurs grupp för en komplex molnbaserad tjänst, till exempel en webb Portal.</span><span class="sxs-lookup"><span data-stu-id="db2b2-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="db2b2-122">Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.</span><span class="sxs-lookup"><span data-stu-id="db2b2-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="db2b2-123">Du kan hitta många mallar i Azure Template-galleriet, eller så kan du skapa egna mallar.</span><span class="sxs-lookup"><span data-stu-id="db2b2-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="db2b2-124">Du kan använda cmdleten **Get-AzureRmResourceGroupGalleryTemplate** för att hitta en mall i galleriet.</span><span class="sxs-lookup"><span data-stu-id="db2b2-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="db2b2-125">Om du vill använda en anpassad mall för att skapa en resurs grupp anger du parametern *TemplateFile* eller parametern *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="db2b2-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="db2b2-126">Varje mall har parametrar för konfigurerbara egenskaper.</span><span class="sxs-lookup"><span data-stu-id="db2b2-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="db2b2-127">Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="db2b2-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="db2b2-128">Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="db2b2-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="db2b2-129">Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.</span><span class="sxs-lookup"><span data-stu-id="db2b2-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="db2b2-130">De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.</span><span class="sxs-lookup"><span data-stu-id="db2b2-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="db2b2-131">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db2b2-131">EXAMPLES</span></span>

### <span data-ttu-id="db2b2-132">Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="db2b2-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="db2b2-133">Det här kommandot skapar en ny distribution med hjälp av en anpassad mall och en mallfil på disk.</span><span class="sxs-lookup"><span data-stu-id="db2b2-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="db2b2-134">Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.</span><span class="sxs-lookup"><span data-stu-id="db2b2-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="db2b2-135">Parametern *TemplateVersion* används för att ange versionen för mallen.</span><span class="sxs-lookup"><span data-stu-id="db2b2-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="db2b2-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db2b2-136">PARAMETERS</span></span>

### <span data-ttu-id="db2b2-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="db2b2-137">-ApiVersion</span></span>
<span data-ttu-id="db2b2-138">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="db2b2-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="db2b2-139">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="db2b2-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="db2b2-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db2b2-140">-AsJob</span></span>
<span data-ttu-id="db2b2-141">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="db2b2-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db2b2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2b2-142">-DefaultProfile</span></span>
<span data-ttu-id="db2b2-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="db2b2-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db2b2-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="db2b2-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="db2b2-145">Anger en loggnings nivå för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="db2b2-145">Specifies a debug log level.</span></span>
<span data-ttu-id="db2b2-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="db2b2-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2b2-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="db2b2-147">RequestContent</span></span>
- <span data-ttu-id="db2b2-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="db2b2-148">ResponseContent</span></span>
- <span data-ttu-id="db2b2-149">Alla</span><span class="sxs-lookup"><span data-stu-id="db2b2-149">All</span></span>
- <span data-ttu-id="db2b2-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="db2b2-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-151">-Force</span><span class="sxs-lookup"><span data-stu-id="db2b2-151">-Force</span></span>
<span data-ttu-id="db2b2-152">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db2b2-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db2b2-153">-Mode</span><span class="sxs-lookup"><span data-stu-id="db2b2-153">-Mode</span></span>
<span data-ttu-id="db2b2-154">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="db2b2-154">Specifies the deployment mode.</span></span> <span data-ttu-id="db2b2-155">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="db2b2-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2b2-156">Kunna</span><span class="sxs-lookup"><span data-stu-id="db2b2-156">Complete</span></span>
- <span data-ttu-id="db2b2-157">Stegvis</span><span class="sxs-lookup"><span data-stu-id="db2b2-157">Incremental</span></span>

<span data-ttu-id="db2b2-158">I fullständigt läge tar Resource Manager bort resurser som finns i resurs gruppen men som inte har angetts i mallen.</span><span class="sxs-lookup"><span data-stu-id="db2b2-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="db2b2-159">I stegvist läge blir resurs hanteraren oförändrade resurser som finns i resurs gruppen men som inte har angetts i mallen.</span><span class="sxs-lookup"><span data-stu-id="db2b2-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="db2b2-160">-Name</span></span>
<span data-ttu-id="db2b2-161">Anger namnet på den resurs grupps distribution som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="db2b2-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-162">-För</span><span class="sxs-lookup"><span data-stu-id="db2b2-162">-Pre</span></span>
<span data-ttu-id="db2b2-163">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="db2b2-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db2b2-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2b2-164">-ResourceGroupName</span></span>
<span data-ttu-id="db2b2-165">Anger namnet på resurs gruppen som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="db2b2-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="db2b2-166">-TemplateFile</span></span>
<span data-ttu-id="db2b2-167">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="db2b2-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="db2b2-168">Det kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel en som skapats med cmdleten **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="db2b2-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="db2b2-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="db2b2-169">-TemplateParameterFile</span></span>
<span data-ttu-id="db2b2-170">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="db2b2-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="db2b2-171">Om en mall har parametrar måste du ange parameter värden med parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="db2b2-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="db2b2-172">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="db2b2-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="db2b2-173">Om du vill använda dynamiska parametrar skriver du ett minus tecken (-) för att ange ett parameter namn och använder sedan TABB-tangenten för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="db2b2-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="db2b2-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="db2b2-174">-TemplateParameterObject</span></span>
<span data-ttu-id="db2b2-175">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="db2b2-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="db2b2-176">Om du behöver hjälp med hash-tabeller i Windows PowerShell skriver du `Get-Help about_Hash_Tables` :</span><span class="sxs-lookup"><span data-stu-id="db2b2-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="db2b2-177">Om en mall har parametrar måste du ange parameter värden.</span><span class="sxs-lookup"><span data-stu-id="db2b2-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="db2b2-178">Mallparametrar läggs till dynamiskt till kommandot när du anger en mall.</span><span class="sxs-lookup"><span data-stu-id="db2b2-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="db2b2-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="db2b2-179">-TemplateParameterUri</span></span>
<span data-ttu-id="db2b2-180">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="db2b2-180">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="db2b2-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="db2b2-181">-TemplateUri</span></span>
<span data-ttu-id="db2b2-182">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="db2b2-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="db2b2-183">Denna fil kan vara en anpassad mall eller en mall som har sparats som en JSON-fil, till exempel genom att använda **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="db2b2-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="db2b2-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db2b2-184">-Confirm</span></span>
<span data-ttu-id="db2b2-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db2b2-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2b2-186">-WhatIf</span></span>
<span data-ttu-id="db2b2-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db2b2-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2b2-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db2b2-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2b2-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2b2-189">CommonParameters</span></span>
<span data-ttu-id="db2b2-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2b2-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2b2-191">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2b2-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2b2-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db2b2-192">INPUTS</span></span>

### <span data-ttu-id="db2b2-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="db2b2-193">None</span></span>

## <span data-ttu-id="db2b2-194">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db2b2-194">OUTPUTS</span></span>

### <span data-ttu-id="db2b2-195">Microsoft. Azure. commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="db2b2-196">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db2b2-196">NOTES</span></span>

## <span data-ttu-id="db2b2-197">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db2b2-197">RELATED LINKS</span></span>

[<span data-ttu-id="db2b2-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="db2b2-199">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="db2b2-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="db2b2-200">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db2b2-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="db2b2-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="db2b2-202">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="db2b2-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db2b2-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


