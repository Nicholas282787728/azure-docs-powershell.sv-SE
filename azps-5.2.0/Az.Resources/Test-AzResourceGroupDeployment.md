---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401184"
---
# <span data-ttu-id="f16cc-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f16cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f16cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f16cc-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f16cc-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="f16cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f16cc-104">SYNTAX</span></span>

### <span data-ttu-id="f16cc-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="f16cc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f16cc-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f16cc-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f16cc-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f16cc-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f16cc-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f16cc-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f16cc-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f16cc-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f16cc-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f16cc-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f16cc-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f16cc-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f16cc-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f16cc-117">DESCRIPTION</span></span>
<span data-ttu-id="f16cc-118">**Test-AzResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="f16cc-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f16cc-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f16cc-119">EXAMPLES</span></span>

### <span data-ttu-id="f16cc-120">Exempel 1: testa distributionen med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="f16cc-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="f16cc-121">Det här kommandot testar en distribution i angiven resurs grupp med hjälp av en webb-hash med en i minnet skapad från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="f16cc-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="f16cc-122">Exempel 2: testa distribution via mallfil och parameter fil</span><span class="sxs-lookup"><span data-stu-id="f16cc-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="f16cc-123">Det här kommandot testar en distribution i den angivna resurs gruppen och resursen med den medföljande mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="f16cc-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="f16cc-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f16cc-124">PARAMETERS</span></span>

### <span data-ttu-id="f16cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f16cc-125">-DefaultProfile</span></span>
<span data-ttu-id="f16cc-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f16cc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f16cc-127">-Mode</span><span class="sxs-lookup"><span data-stu-id="f16cc-127">-Mode</span></span>
<span data-ttu-id="f16cc-128">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="f16cc-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="f16cc-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f16cc-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f16cc-130">Stegvis</span><span class="sxs-lookup"><span data-stu-id="f16cc-130">Incremental</span></span>
- <span data-ttu-id="f16cc-131">Kunna</span><span class="sxs-lookup"><span data-stu-id="f16cc-131">Complete</span></span>

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

### <span data-ttu-id="f16cc-132">-För</span><span class="sxs-lookup"><span data-stu-id="f16cc-132">-Pre</span></span>
<span data-ttu-id="f16cc-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f16cc-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f16cc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f16cc-134">-ResourceGroupName</span></span>
<span data-ttu-id="f16cc-135">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="f16cc-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="f16cc-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f16cc-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="f16cc-137">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="f16cc-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="f16cc-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="f16cc-139">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="f16cc-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="f16cc-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f16cc-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f16cc-141">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="f16cc-142">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="f16cc-143">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="f16cc-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f16cc-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f16cc-144">-TemplateFile</span></span>
<span data-ttu-id="f16cc-145">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="f16cc-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f16cc-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f16cc-146">-TemplateObject</span></span>
<span data-ttu-id="f16cc-147">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f16cc-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f16cc-148">-TemplateParameterFile</span></span>
<span data-ttu-id="f16cc-149">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="f16cc-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="f16cc-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f16cc-150">-TemplateParameterObject</span></span>
<span data-ttu-id="f16cc-151">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="f16cc-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="f16cc-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f16cc-152">-TemplateParameterUri</span></span>
<span data-ttu-id="f16cc-153">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="f16cc-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="f16cc-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f16cc-154">-TemplateUri</span></span>
<span data-ttu-id="f16cc-155">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="f16cc-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f16cc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16cc-156">CommonParameters</span></span>
<span data-ttu-id="f16cc-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f16cc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16cc-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f16cc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16cc-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f16cc-159">INPUTS</span></span>

### <span data-ttu-id="f16cc-160">System. String</span><span class="sxs-lookup"><span data-stu-id="f16cc-160">System.String</span></span>

### <span data-ttu-id="f16cc-161">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="f16cc-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="f16cc-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f16cc-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f16cc-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f16cc-163">OUTPUTS</span></span>

### <span data-ttu-id="f16cc-164">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f16cc-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f16cc-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f16cc-165">NOTES</span></span>

## <span data-ttu-id="f16cc-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f16cc-166">RELATED LINKS</span></span>

[<span data-ttu-id="f16cc-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="f16cc-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f16cc-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="f16cc-170">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f16cc-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


