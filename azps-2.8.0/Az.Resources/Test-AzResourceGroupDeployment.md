---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920024"
---
# <span data-ttu-id="a33ca-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a33ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a33ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a33ca-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a33ca-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="a33ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a33ca-104">SYNTAX</span></span>

### <span data-ttu-id="a33ca-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="a33ca-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33ca-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a33ca-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a33ca-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a33ca-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a33ca-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a33ca-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a33ca-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a33ca-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a33ca-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a33ca-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33ca-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a33ca-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33ca-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a33ca-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33ca-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a33ca-117">DESCRIPTION</span></span>
<span data-ttu-id="a33ca-118">**Test-AzResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="a33ca-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="a33ca-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a33ca-119">EXAMPLES</span></span>

### <span data-ttu-id="a33ca-120">Exempel 1: testa distributionen med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="a33ca-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a33ca-121">Det här kommandot testar en distribution i angiven resurs grupp med hjälp av en webb-hash med en i minnet skapad från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="a33ca-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="a33ca-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a33ca-122">PARAMETERS</span></span>

### <span data-ttu-id="a33ca-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a33ca-123">-ApiVersion</span></span>
<span data-ttu-id="a33ca-124">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="a33ca-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a33ca-125">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="a33ca-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a33ca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33ca-126">-DefaultProfile</span></span>
<span data-ttu-id="a33ca-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a33ca-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a33ca-128">-Mode</span><span class="sxs-lookup"><span data-stu-id="a33ca-128">-Mode</span></span>
<span data-ttu-id="a33ca-129">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="a33ca-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="a33ca-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a33ca-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a33ca-131">Stegvis</span><span class="sxs-lookup"><span data-stu-id="a33ca-131">Incremental</span></span>
- <span data-ttu-id="a33ca-132">Kunna</span><span class="sxs-lookup"><span data-stu-id="a33ca-132">Complete</span></span>

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

### <span data-ttu-id="a33ca-133">-För</span><span class="sxs-lookup"><span data-stu-id="a33ca-133">-Pre</span></span>
<span data-ttu-id="a33ca-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a33ca-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a33ca-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33ca-135">-ResourceGroupName</span></span>
<span data-ttu-id="a33ca-136">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="a33ca-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="a33ca-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a33ca-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="a33ca-138">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="a33ca-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="a33ca-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a33ca-140">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="a33ca-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a33ca-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a33ca-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a33ca-142">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="a33ca-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a33ca-143">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="a33ca-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a33ca-144">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="a33ca-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a33ca-145">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a33ca-145">-TemplateFile</span></span>
<span data-ttu-id="a33ca-146">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="a33ca-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="a33ca-147">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a33ca-147">-TemplateObject</span></span>
<span data-ttu-id="a33ca-148">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="a33ca-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a33ca-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a33ca-149">-TemplateParameterFile</span></span>
<span data-ttu-id="a33ca-150">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="a33ca-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="a33ca-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a33ca-151">-TemplateParameterObject</span></span>
<span data-ttu-id="a33ca-152">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="a33ca-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="a33ca-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a33ca-153">-TemplateParameterUri</span></span>
<span data-ttu-id="a33ca-154">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="a33ca-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a33ca-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a33ca-155">-TemplateUri</span></span>
<span data-ttu-id="a33ca-156">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="a33ca-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="a33ca-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33ca-157">CommonParameters</span></span>
<span data-ttu-id="a33ca-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a33ca-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33ca-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a33ca-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33ca-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a33ca-160">INPUTS</span></span>

### <span data-ttu-id="a33ca-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a33ca-161">System.String</span></span>

### <span data-ttu-id="a33ca-162">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a33ca-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a33ca-163">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a33ca-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a33ca-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a33ca-164">OUTPUTS</span></span>

### <span data-ttu-id="a33ca-165">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="a33ca-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="a33ca-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a33ca-166">NOTES</span></span>

## <span data-ttu-id="a33ca-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a33ca-167">RELATED LINKS</span></span>

[<span data-ttu-id="a33ca-168">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a33ca-169">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a33ca-170">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a33ca-171">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a33ca-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


