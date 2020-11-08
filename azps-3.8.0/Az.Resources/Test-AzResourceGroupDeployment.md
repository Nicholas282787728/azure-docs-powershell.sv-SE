---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089429"
---
# <span data-ttu-id="c8c02-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c8c02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8c02-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c02-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c8c02-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="c8c02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8c02-104">SYNTAX</span></span>

### <span data-ttu-id="c8c02-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="c8c02-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8c02-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c8c02-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c8c02-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c8c02-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c8c02-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c8c02-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c8c02-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c8c02-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c8c02-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c8c02-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c02-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c8c02-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8c02-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c8c02-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c02-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8c02-117">DESCRIPTION</span></span>
<span data-ttu-id="c8c02-118">**Test-AzResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="c8c02-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="c8c02-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8c02-119">EXAMPLES</span></span>

### <span data-ttu-id="c8c02-120">Exempel 1: testa distributionen med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="c8c02-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c8c02-121">Det här kommandot testar en distribution i angiven resurs grupp med hjälp av en webb-hash med en i minnet skapad från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="c8c02-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="c8c02-122">Exempel 2: testa distribution via mallfil och parameter objekt</span><span class="sxs-lookup"><span data-stu-id="c8c02-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="c8c02-123">Det här kommandot testar en distribution i den angivna resurs gruppen och resursen med den medföljande mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="c8c02-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="c8c02-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8c02-124">PARAMETERS</span></span>

### <span data-ttu-id="c8c02-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8c02-125">-ApiVersion</span></span>
<span data-ttu-id="c8c02-126">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="c8c02-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c8c02-127">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="c8c02-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c8c02-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c02-128">-DefaultProfile</span></span>
<span data-ttu-id="c8c02-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8c02-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8c02-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="c8c02-130">-Mode</span></span>
<span data-ttu-id="c8c02-131">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="c8c02-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="c8c02-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c8c02-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8c02-133">Stegvis</span><span class="sxs-lookup"><span data-stu-id="c8c02-133">Incremental</span></span>
- <span data-ttu-id="c8c02-134">Kunna</span><span class="sxs-lookup"><span data-stu-id="c8c02-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c02-135">-För</span><span class="sxs-lookup"><span data-stu-id="c8c02-135">-Pre</span></span>
<span data-ttu-id="c8c02-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c8c02-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8c02-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c02-137">-ResourceGroupName</span></span>
<span data-ttu-id="c8c02-138">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="c8c02-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="c8c02-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="c8c02-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="c8c02-140">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="c8c02-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="c8c02-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="c8c02-142">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="c8c02-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="c8c02-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c8c02-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c8c02-144">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="c8c02-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="c8c02-145">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="c8c02-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="c8c02-146">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="c8c02-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c8c02-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c8c02-147">-TemplateFile</span></span>
<span data-ttu-id="c8c02-148">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="c8c02-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="c8c02-149">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c8c02-149">-TemplateObject</span></span>
<span data-ttu-id="c8c02-150">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="c8c02-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c8c02-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c8c02-151">-TemplateParameterFile</span></span>
<span data-ttu-id="c8c02-152">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="c8c02-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="c8c02-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c8c02-153">-TemplateParameterObject</span></span>
<span data-ttu-id="c8c02-154">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="c8c02-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="c8c02-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c8c02-155">-TemplateParameterUri</span></span>
<span data-ttu-id="c8c02-156">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="c8c02-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="c8c02-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c8c02-157">-TemplateUri</span></span>
<span data-ttu-id="c8c02-158">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="c8c02-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="c8c02-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c02-159">CommonParameters</span></span>
<span data-ttu-id="c8c02-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c02-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c02-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8c02-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c02-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8c02-162">INPUTS</span></span>

### <span data-ttu-id="c8c02-163">System. String</span><span class="sxs-lookup"><span data-stu-id="c8c02-163">System.String</span></span>

### <span data-ttu-id="c8c02-164">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c8c02-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="c8c02-165">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c8c02-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8c02-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8c02-166">OUTPUTS</span></span>

### <span data-ttu-id="c8c02-167">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c8c02-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c8c02-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8c02-168">NOTES</span></span>

## <span data-ttu-id="c8c02-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8c02-169">RELATED LINKS</span></span>

[<span data-ttu-id="c8c02-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="c8c02-171">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="c8c02-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c8c02-173">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c02-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


