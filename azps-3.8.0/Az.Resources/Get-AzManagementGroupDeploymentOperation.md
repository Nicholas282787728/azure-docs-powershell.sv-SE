---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927361"
---
# <span data-ttu-id="f6e06-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f6e06-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="f6e06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6e06-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e06-103">Skaffa distributions åtgärd för hanterings grupp distribution</span><span class="sxs-lookup"><span data-stu-id="f6e06-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="f6e06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6e06-104">SYNTAX</span></span>

### <span data-ttu-id="f6e06-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="f6e06-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6e06-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f6e06-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e06-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6e06-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e06-108">Cmdleten **Get-AzManagementGroupDeploymentOperation** innehåller alla åtgärder som ingick i en hanterings grupp distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="f6e06-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="f6e06-109">Det här är samma information som anges i distributions informationen på portalen.</span><span class="sxs-lookup"><span data-stu-id="f6e06-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="f6e06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6e06-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e06-111">Exempel 1: skaffa distributions åtgärder som fått ett distributions namn</span><span class="sxs-lookup"><span data-stu-id="f6e06-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="f6e06-112">Hämtar distributions åtgärder med namnet "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="f6e06-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="f6e06-113">Exempel 2: skaffa en distribution och få drift sättnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="f6e06-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="f6e06-114">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG" och får sin distribution.</span><span class="sxs-lookup"><span data-stu-id="f6e06-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="f6e06-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6e06-115">PARAMETERS</span></span>

### <span data-ttu-id="f6e06-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6e06-116">-ApiVersion</span></span>
<span data-ttu-id="f6e06-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f6e06-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6e06-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f6e06-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f6e06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e06-119">-DefaultProfile</span></span>
<span data-ttu-id="f6e06-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e06-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f6e06-121">-DeploymentName</span></span>
<span data-ttu-id="f6e06-122">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="f6e06-122">The deployment name.</span></span>

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

### <span data-ttu-id="f6e06-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f6e06-123">-DeploymentObject</span></span>
<span data-ttu-id="f6e06-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="f6e06-124">The deployment object.</span></span>

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

### <span data-ttu-id="f6e06-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f6e06-125">-ManagementGroupId</span></span>
<span data-ttu-id="f6e06-126">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="f6e06-126">The management group id.</span></span>

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

### <span data-ttu-id="f6e06-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f6e06-127">-OperationId</span></span>
<span data-ttu-id="f6e06-128">Distributions åtgärdens ID.</span><span class="sxs-lookup"><span data-stu-id="f6e06-128">The deployment operation Id.</span></span>

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

### <span data-ttu-id="f6e06-129">-För</span><span class="sxs-lookup"><span data-stu-id="f6e06-129">-Pre</span></span>
<span data-ttu-id="f6e06-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f6e06-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f6e06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e06-131">CommonParameters</span></span>
<span data-ttu-id="f6e06-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e06-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6e06-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e06-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6e06-134">INPUTS</span></span>

### <span data-ttu-id="f6e06-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f6e06-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f6e06-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6e06-136">OUTPUTS</span></span>

### <span data-ttu-id="f6e06-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f6e06-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="f6e06-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6e06-138">NOTES</span></span>

## <span data-ttu-id="f6e06-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6e06-139">RELATED LINKS</span></span>
