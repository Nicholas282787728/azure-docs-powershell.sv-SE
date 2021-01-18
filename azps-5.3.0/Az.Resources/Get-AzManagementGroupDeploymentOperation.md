---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521547"
---
# <span data-ttu-id="d5134-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5134-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="d5134-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5134-102">SYNOPSIS</span></span>
<span data-ttu-id="d5134-103">Skaffa distributions åtgärd för hanterings grupp distribution</span><span class="sxs-lookup"><span data-stu-id="d5134-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="d5134-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5134-104">SYNTAX</span></span>

### <span data-ttu-id="d5134-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d5134-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5134-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5134-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5134-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5134-107">DESCRIPTION</span></span>
<span data-ttu-id="d5134-108">Cmdleten **Get-AzManagementGroupDeploymentOperation** innehåller alla åtgärder som ingick i en hanterings grupp distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="d5134-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d5134-109">Det här är samma information som anges i distributions informationen på portalen.</span><span class="sxs-lookup"><span data-stu-id="d5134-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="d5134-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5134-110">EXAMPLES</span></span>

### <span data-ttu-id="d5134-111">Exempel 1: skaffa distributions åtgärder som fått ett distributions namn</span><span class="sxs-lookup"><span data-stu-id="d5134-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="d5134-112">Hämtar distributions åtgärder med namnet "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="d5134-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="d5134-113">Exempel 2: skaffa en distribution och få drift sättnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="d5134-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="d5134-114">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG" och får sin distribution.</span><span class="sxs-lookup"><span data-stu-id="d5134-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="d5134-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5134-115">PARAMETERS</span></span>

### <span data-ttu-id="d5134-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5134-116">-DefaultProfile</span></span>
<span data-ttu-id="d5134-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5134-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5134-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d5134-118">-DeploymentName</span></span>
<span data-ttu-id="d5134-119">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="d5134-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5134-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5134-120">-DeploymentObject</span></span>
<span data-ttu-id="d5134-121">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="d5134-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5134-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d5134-122">-ManagementGroupId</span></span>
<span data-ttu-id="d5134-123">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="d5134-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5134-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d5134-124">-OperationId</span></span>
<span data-ttu-id="d5134-125">Distributions åtgärdens ID.</span><span class="sxs-lookup"><span data-stu-id="d5134-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5134-126">-För</span><span class="sxs-lookup"><span data-stu-id="d5134-126">-Pre</span></span>
<span data-ttu-id="d5134-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d5134-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d5134-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5134-128">CommonParameters</span></span>
<span data-ttu-id="d5134-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5134-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5134-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5134-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5134-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5134-131">INPUTS</span></span>

### <span data-ttu-id="d5134-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d5134-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d5134-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5134-133">OUTPUTS</span></span>

### <span data-ttu-id="d5134-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5134-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d5134-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5134-135">NOTES</span></span>

## <span data-ttu-id="d5134-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5134-136">RELATED LINKS</span></span>
