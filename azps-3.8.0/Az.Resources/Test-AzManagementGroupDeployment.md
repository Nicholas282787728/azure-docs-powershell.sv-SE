---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089430"
---
# <span data-ttu-id="20324-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="20324-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="20324-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20324-102">SYNOPSIS</span></span>
<span data-ttu-id="20324-103">Validerar en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="20324-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="20324-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20324-104">SYNTAX</span></span>

### <span data-ttu-id="20324-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="20324-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20324-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="20324-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="20324-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="20324-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="20324-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="20324-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="20324-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="20324-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="20324-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="20324-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="20324-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20324-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="20324-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20324-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20324-117">DESCRIPTION</span></span>
<span data-ttu-id="20324-118">**Test-AzManagementGroupDeployment** cmdlet avgör om en distributionsmall och dess parameter värden är giltiga i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="20324-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="20324-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20324-119">EXAMPLES</span></span>

### <span data-ttu-id="20324-120">Exempel 1: testa distributionen med en anpassad mall och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="20324-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="20324-121">Det här kommandot testar en distribution i hanterings gruppen "myMG" med den givna mallfilen och parameter filen.</span><span class="sxs-lookup"><span data-stu-id="20324-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="20324-122">Exempel 2: testa distribution med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="20324-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="20324-123">Det här kommandot testar en distribution i hanterings gruppen "myMG" med hjälp av en webb-WM-fil som skapats från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="20324-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="20324-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20324-124">PARAMETERS</span></span>

### <span data-ttu-id="20324-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20324-125">-ApiVersion</span></span>
<span data-ttu-id="20324-126">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="20324-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="20324-127">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="20324-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="20324-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20324-128">-DefaultProfile</span></span>
<span data-ttu-id="20324-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20324-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20324-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="20324-130">-Location</span></span>
<span data-ttu-id="20324-131">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="20324-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="20324-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="20324-132">-ManagementGroupId</span></span>
<span data-ttu-id="20324-133">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="20324-133">The management group id.</span></span>

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

### <span data-ttu-id="20324-134">-För</span><span class="sxs-lookup"><span data-stu-id="20324-134">-Pre</span></span>
<span data-ttu-id="20324-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="20324-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="20324-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="20324-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="20324-137">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="20324-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="20324-138">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="20324-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="20324-139">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="20324-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="20324-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="20324-140">-TemplateFile</span></span>
<span data-ttu-id="20324-141">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="20324-141">Local path to the template file.</span></span>

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

### <span data-ttu-id="20324-142">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="20324-142">-TemplateObject</span></span>
<span data-ttu-id="20324-143">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="20324-143">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20324-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="20324-144">-TemplateParameterFile</span></span>
<span data-ttu-id="20324-145">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="20324-145">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20324-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="20324-146">-TemplateParameterObject</span></span>
<span data-ttu-id="20324-147">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="20324-147">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20324-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="20324-148">-TemplateParameterUri</span></span>
<span data-ttu-id="20324-149">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="20324-149">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20324-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="20324-150">-TemplateUri</span></span>
<span data-ttu-id="20324-151">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="20324-151">Uri to the template file.</span></span>

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

### <span data-ttu-id="20324-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20324-152">CommonParameters</span></span>
<span data-ttu-id="20324-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20324-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20324-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20324-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20324-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20324-155">INPUTS</span></span>

### <span data-ttu-id="20324-156">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="20324-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="20324-157">System. String</span><span class="sxs-lookup"><span data-stu-id="20324-157">System.String</span></span>

## <span data-ttu-id="20324-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20324-158">OUTPUTS</span></span>

### <span data-ttu-id="20324-159">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="20324-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="20324-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20324-160">NOTES</span></span>

## <span data-ttu-id="20324-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20324-161">RELATED LINKS</span></span>
