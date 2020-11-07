---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 77c2a712a3d44d963fd08642d1a1c88b5d8c81e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923753"
---
# <span data-ttu-id="f0e79-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0e79-101">Test-AzDeployment</span></span>

## <span data-ttu-id="f0e79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0e79-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e79-103">Verifierar en distribution.</span><span class="sxs-lookup"><span data-stu-id="f0e79-103">Validates a deployment.</span></span>

## <span data-ttu-id="f0e79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0e79-104">SYNTAX</span></span>

### <span data-ttu-id="f0e79-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="f0e79-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f0e79-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f0e79-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f0e79-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f0e79-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f0e79-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f0e79-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e79-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f0e79-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0e79-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0e79-113">DESCRIPTION</span></span>
<span data-ttu-id="f0e79-114">**Test-AzDeployment** cmdlet bestämmer om en distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="f0e79-114">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f0e79-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0e79-115">EXAMPLES</span></span>

### <span data-ttu-id="f0e79-116">Exempel 1: testa distributionen med en anpassad mall och en parameter fil</span><span class="sxs-lookup"><span data-stu-id="f0e79-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="f0e79-117">Det här kommandot testar en distribution vid det aktuella abonnemanget med hjälp av en given mallfil och parameter fil.</span><span class="sxs-lookup"><span data-stu-id="f0e79-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="f0e79-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0e79-118">PARAMETERS</span></span>

### <span data-ttu-id="f0e79-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0e79-119">-ApiVersion</span></span>
<span data-ttu-id="f0e79-120">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f0e79-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0e79-121">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f0e79-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f0e79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e79-122">-DefaultProfile</span></span>
<span data-ttu-id="f0e79-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e79-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="f0e79-124">-Location</span></span>
<span data-ttu-id="f0e79-125">Platsen där distributions data ska lagras.</span><span class="sxs-lookup"><span data-stu-id="f0e79-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f0e79-126">-För</span><span class="sxs-lookup"><span data-stu-id="f0e79-126">-Pre</span></span>
<span data-ttu-id="f0e79-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f0e79-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f0e79-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f0e79-128">-TemplateFile</span></span>
<span data-ttu-id="f0e79-129">Lokal sökväg till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="f0e79-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="f0e79-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f0e79-130">-TemplateParameterFile</span></span>
<span data-ttu-id="f0e79-131">En fil som innehåller mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="f0e79-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f0e79-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f0e79-132">-TemplateParameterObject</span></span>
<span data-ttu-id="f0e79-133">En hash-tabell som representerar parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f0e79-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f0e79-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f0e79-134">-TemplateParameterUri</span></span>
<span data-ttu-id="f0e79-135">URI till mallstrukturlistan-filen.</span><span class="sxs-lookup"><span data-stu-id="f0e79-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f0e79-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f0e79-136">-TemplateUri</span></span>
<span data-ttu-id="f0e79-137">URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="f0e79-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="f0e79-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e79-138">CommonParameters</span></span>
<span data-ttu-id="f0e79-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e79-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e79-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e79-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e79-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0e79-141">INPUTS</span></span>

### <span data-ttu-id="f0e79-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e79-142">System.String</span></span>
<span data-ttu-id="f0e79-143">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f0e79-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0e79-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0e79-144">OUTPUTS</span></span>

### <span data-ttu-id="f0e79-145">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f0e79-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f0e79-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0e79-146">NOTES</span></span>

## <span data-ttu-id="f0e79-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0e79-147">RELATED LINKS</span></span>
