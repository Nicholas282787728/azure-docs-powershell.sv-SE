---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091503"
---
# <span data-ttu-id="087c3-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="087c3-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="087c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="087c3-102">SYNOPSIS</span></span>
<span data-ttu-id="087c3-103">Skaffa distributions åtgärd för distribution med klient-scope</span><span class="sxs-lookup"><span data-stu-id="087c3-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="087c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="087c3-104">SYNTAX</span></span>

### <span data-ttu-id="087c3-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="087c3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="087c3-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="087c3-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="087c3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="087c3-107">DESCRIPTION</span></span>
<span data-ttu-id="087c3-108">Cmdleten **Get-AzTenantDeploymentOperation** innehåller alla åtgärder som ingick i distributionen i den aktuella klient omfattningen för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="087c3-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="087c3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="087c3-109">EXAMPLES</span></span>

### <span data-ttu-id="087c3-110">Exempel 1: skaffa distributions åtgärder som fått ett distributions namn</span><span class="sxs-lookup"><span data-stu-id="087c3-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="087c3-111">Hämtar distributions åtgärder med namnet "Deploy01" i det aktuella klient scopet.</span><span class="sxs-lookup"><span data-stu-id="087c3-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="087c3-112">Exempel 2: skaffa en distribution och få drift sättnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="087c3-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="087c3-113">Det här kommandot får distributionen "Deploy01" vid den aktuella klient omfattningen och får drift sättnings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="087c3-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="087c3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="087c3-114">PARAMETERS</span></span>

### <span data-ttu-id="087c3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="087c3-115">-ApiVersion</span></span>
<span data-ttu-id="087c3-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="087c3-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="087c3-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="087c3-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="087c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087c3-118">-DefaultProfile</span></span>
<span data-ttu-id="087c3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="087c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="087c3-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="087c3-120">-DeploymentName</span></span>
<span data-ttu-id="087c3-121">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="087c3-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087c3-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="087c3-122">-DeploymentObject</span></span>
<span data-ttu-id="087c3-123">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="087c3-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="087c3-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="087c3-124">-OperationId</span></span>
<span data-ttu-id="087c3-125">Distributions åtgärdens ID.</span><span class="sxs-lookup"><span data-stu-id="087c3-125">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087c3-126">-För</span><span class="sxs-lookup"><span data-stu-id="087c3-126">-Pre</span></span>
<span data-ttu-id="087c3-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="087c3-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="087c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087c3-128">CommonParameters</span></span>
<span data-ttu-id="087c3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087c3-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="087c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087c3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="087c3-131">INPUTS</span></span>

### <span data-ttu-id="087c3-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="087c3-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="087c3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="087c3-133">OUTPUTS</span></span>

### <span data-ttu-id="087c3-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="087c3-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="087c3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="087c3-135">NOTES</span></span>

## <span data-ttu-id="087c3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="087c3-136">RELATED LINKS</span></span>
