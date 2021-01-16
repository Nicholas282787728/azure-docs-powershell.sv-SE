---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414971"
---
# <span data-ttu-id="2db2f-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2db2f-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2db2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2db2f-102">SYNOPSIS</span></span>
<span data-ttu-id="2db2f-103">Validerar en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="2db2f-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="2db2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2db2f-104">SYNTAX</span></span>

### <span data-ttu-id="2db2f-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="2db2f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db2f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2db2f-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db2f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2db2f-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db2f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2db2f-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db2f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2db2f-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2db2f-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2db2f-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2db2f-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2db2f-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2db2f-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db2f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2db2f-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db2f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2db2f-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db2f-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2db2f-117">DESCRIPTION</span></span>
<span data-ttu-id="2db2f-118">**Test-AzManagementGroupDeployment** cmdlet avgör om en distributionsmall och dess parameter värden är giltiga i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="2db2f-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="2db2f-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2db2f-119">EXAMPLES</span></span>

### <span data-ttu-id="2db2f-120">Exempel 1: testa distributionen med en anpassad mall och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="2db2f-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="2db2f-121">Det här kommandot testar en distribution i hanterings gruppen "myMG" med den givna mallfilen och parameter filen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="2db2f-122">Exempel 2: testa distribution med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="2db2f-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2db2f-123">Det här kommandot testar en distribution i hanterings gruppen "myMG" med hjälp av en webb-WM-fil som skapats från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="2db2f-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="2db2f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2db2f-124">PARAMETERS</span></span>

### <span data-ttu-id="2db2f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db2f-125">-DefaultProfile</span></span>
<span data-ttu-id="2db2f-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2db2f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db2f-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="2db2f-127">-Location</span></span>
<span data-ttu-id="2db2f-128">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="2db2f-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2db2f-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2db2f-129">-ManagementGroupId</span></span>
<span data-ttu-id="2db2f-130">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="2db2f-130">The management group id.</span></span>

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

### <span data-ttu-id="2db2f-131">-För</span><span class="sxs-lookup"><span data-stu-id="2db2f-131">-Pre</span></span>
<span data-ttu-id="2db2f-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2db2f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2db2f-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2db2f-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2db2f-134">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2db2f-135">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2db2f-136">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="2db2f-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2db2f-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2db2f-137">-TemplateFile</span></span>
<span data-ttu-id="2db2f-138">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="2db2f-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2db2f-139">-TemplateObject</span></span>
<span data-ttu-id="2db2f-140">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2db2f-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2db2f-141">-TemplateParameterFile</span></span>
<span data-ttu-id="2db2f-142">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="2db2f-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2db2f-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2db2f-143">-TemplateParameterObject</span></span>
<span data-ttu-id="2db2f-144">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="2db2f-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2db2f-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2db2f-145">-TemplateParameterUri</span></span>
<span data-ttu-id="2db2f-146">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2db2f-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2db2f-147">-TemplateUri</span></span>
<span data-ttu-id="2db2f-148">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="2db2f-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="2db2f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db2f-149">CommonParameters</span></span>
<span data-ttu-id="2db2f-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db2f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db2f-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2db2f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db2f-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2db2f-152">INPUTS</span></span>

### <span data-ttu-id="2db2f-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="2db2f-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2db2f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2db2f-154">System.String</span></span>

## <span data-ttu-id="2db2f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2db2f-155">OUTPUTS</span></span>

### <span data-ttu-id="2db2f-156">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="2db2f-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="2db2f-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2db2f-157">NOTES</span></span>

## <span data-ttu-id="2db2f-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2db2f-158">RELATED LINKS</span></span>
