---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: d6222c0e1ecd6eee39b65ac65e74707d1d64ef17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258647"
---
# <span data-ttu-id="c4549-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c4549-101">Test-AzDeployment</span></span>

## <span data-ttu-id="c4549-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4549-102">SYNOPSIS</span></span>
<span data-ttu-id="c4549-103">Verifierar en distribution.</span><span class="sxs-lookup"><span data-stu-id="c4549-103">Validates a deployment.</span></span>

## <span data-ttu-id="c4549-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4549-104">SYNTAX</span></span>

### <span data-ttu-id="c4549-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="c4549-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4549-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c4549-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c4549-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c4549-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c4549-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c4549-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c4549-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c4549-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c4549-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c4549-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4549-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c4549-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4549-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c4549-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4549-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4549-117">DESCRIPTION</span></span>
<span data-ttu-id="c4549-118">**Test-AzDeployment** cmdlet bestämmer om en distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="c4549-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="c4549-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4549-119">EXAMPLES</span></span>

### <span data-ttu-id="c4549-120">Exempel 1: testa distributionen med en anpassad mall och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="c4549-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="c4549-121">Det här kommandot testar en distribution vid det aktuella abonnemanget med hjälp av en given mallfil och parameter fil.</span><span class="sxs-lookup"><span data-stu-id="c4549-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="c4549-122">Exempel 2: testa distribution med ett anpassat malldokument och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="c4549-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c4549-123">Det här kommandot testar en distribution vid det aktuella abonnemanget med hjälp av en webb-hash med en i minnet skapad från den angivna mallfilen och en parameter fil.</span><span class="sxs-lookup"><span data-stu-id="c4549-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="c4549-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4549-124">PARAMETERS</span></span>

### <span data-ttu-id="c4549-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4549-125">-ApiVersion</span></span>
<span data-ttu-id="c4549-126">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c4549-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c4549-127">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="c4549-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c4549-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4549-128">-DefaultProfile</span></span>
<span data-ttu-id="c4549-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4549-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4549-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4549-130">-Location</span></span>
<span data-ttu-id="c4549-131">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="c4549-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c4549-132">-För</span><span class="sxs-lookup"><span data-stu-id="c4549-132">-Pre</span></span>
<span data-ttu-id="c4549-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c4549-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c4549-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c4549-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c4549-135">Hoppar över den dynamiska PowerShell-parametern för parametrar som kontrollerar om den tillgängliga mallen innehåller alla nödvändiga parametrar som används i mallen.</span><span class="sxs-lookup"><span data-stu-id="c4549-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="c4549-136">Den här kontrollen uppmanar användaren att ange ett värde för de saknade parametrarna, men om du anger SkipTemplateParameterPrompt ignorerar den här uppmaningen och felvärderar omedelbart om en parameter inte är bunden i mallen.</span><span class="sxs-lookup"><span data-stu-id="c4549-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="c4549-137">För icke-interaktiva skript kan-SkipTemplateParameterPrompt tillhandahållas för att ge ett bättre fel meddelande om inte alla nödvändiga parametrar uppfylls.</span><span class="sxs-lookup"><span data-stu-id="c4549-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c4549-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c4549-138">-TemplateFile</span></span>
<span data-ttu-id="c4549-139">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="c4549-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="c4549-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c4549-140">-TemplateObject</span></span>
<span data-ttu-id="c4549-141">En hash-tabell som representerar mallen.</span><span class="sxs-lookup"><span data-stu-id="c4549-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c4549-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c4549-142">-TemplateParameterFile</span></span>
<span data-ttu-id="c4549-143">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="c4549-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c4549-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c4549-144">-TemplateParameterObject</span></span>
<span data-ttu-id="c4549-145">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="c4549-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c4549-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c4549-146">-TemplateParameterUri</span></span>
<span data-ttu-id="c4549-147">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="c4549-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c4549-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c4549-148">-TemplateUri</span></span>
<span data-ttu-id="c4549-149">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="c4549-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="c4549-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4549-150">CommonParameters</span></span>
<span data-ttu-id="c4549-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4549-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4549-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4549-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4549-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4549-153">INPUTS</span></span>

### <span data-ttu-id="c4549-154">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c4549-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c4549-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c4549-155">System.String</span></span>

## <span data-ttu-id="c4549-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4549-156">OUTPUTS</span></span>

### <span data-ttu-id="c4549-157">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c4549-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c4549-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4549-158">NOTES</span></span>

## <span data-ttu-id="c4549-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4549-159">RELATED LINKS</span></span>
