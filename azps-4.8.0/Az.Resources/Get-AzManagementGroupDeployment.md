---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261953"
---
# <span data-ttu-id="1b450-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b450-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1b450-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b450-102">SYNOPSIS</span></span>
<span data-ttu-id="1b450-103">Skaffa distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="1b450-103">Get deployment at a management group</span></span>

## <span data-ttu-id="1b450-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b450-104">SYNTAX</span></span>

### <span data-ttu-id="1b450-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="1b450-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b450-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1b450-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b450-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b450-107">DESCRIPTION</span></span>
<span data-ttu-id="1b450-108">Cmdleten **Get-AzManagementGroupDeployment** får distributionerna i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="1b450-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="1b450-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="1b450-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="1b450-110">Som standard får **Get-AzManagementGroupDeployment** alla distributioner i hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b450-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="1b450-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b450-111">EXAMPLES</span></span>

### <span data-ttu-id="1b450-112">Exempel 1: Hämta alla distributioner i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="1b450-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="1b450-113">Det här kommandot får alla distributioner i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="1b450-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="1b450-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="1b450-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="1b450-115">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="1b450-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="1b450-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="1b450-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="1b450-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="1b450-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="1b450-118">Exempel 3: skaffa en distribution utifrån ID</span><span class="sxs-lookup"><span data-stu-id="1b450-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="1b450-119">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="1b450-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="1b450-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b450-120">PARAMETERS</span></span>

### <span data-ttu-id="1b450-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b450-121">-ApiVersion</span></span>
<span data-ttu-id="1b450-122">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1b450-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b450-123">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="1b450-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1b450-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b450-124">-DefaultProfile</span></span>
<span data-ttu-id="1b450-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b450-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b450-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1b450-126">-Id</span></span>
<span data-ttu-id="1b450-127">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="1b450-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1b450-128">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1b450-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b450-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1b450-129">-ManagementGroupId</span></span>
<span data-ttu-id="1b450-130">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="1b450-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b450-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b450-131">-Name</span></span>
<span data-ttu-id="1b450-132">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="1b450-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b450-133">-För</span><span class="sxs-lookup"><span data-stu-id="1b450-133">-Pre</span></span>
<span data-ttu-id="1b450-134">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1b450-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1b450-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b450-135">CommonParameters</span></span>
<span data-ttu-id="1b450-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b450-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b450-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b450-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b450-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b450-138">INPUTS</span></span>

### <span data-ttu-id="1b450-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="1b450-139">None</span></span>

## <span data-ttu-id="1b450-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b450-140">OUTPUTS</span></span>

### <span data-ttu-id="1b450-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1b450-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1b450-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b450-142">NOTES</span></span>

## <span data-ttu-id="1b450-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b450-143">RELATED LINKS</span></span>
