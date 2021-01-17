---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415736"
---
# <span data-ttu-id="ed9db-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ed9db-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ed9db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed9db-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9db-103">Skaffa distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="ed9db-103">Get deployment at a management group</span></span>

## <span data-ttu-id="ed9db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed9db-104">SYNTAX</span></span>

### <span data-ttu-id="ed9db-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="ed9db-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed9db-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ed9db-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed9db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed9db-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9db-108">Cmdleten **Get-AzManagementGroupDeployment** får distributionerna i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="ed9db-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="ed9db-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="ed9db-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ed9db-110">Som standard får **Get-AzManagementGroupDeployment** alla distributioner i hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="ed9db-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="ed9db-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed9db-111">EXAMPLES</span></span>

### <span data-ttu-id="ed9db-112">Exempel 1: Hämta alla distributioner i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="ed9db-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="ed9db-113">Det här kommandot får alla distributioner i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="ed9db-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="ed9db-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="ed9db-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="ed9db-115">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="ed9db-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="ed9db-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="ed9db-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ed9db-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="ed9db-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ed9db-118">Exempel 3: skaffa en distribution utifrån ID</span><span class="sxs-lookup"><span data-stu-id="ed9db-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ed9db-119">Det här kommandot får distributionen "Deploy01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="ed9db-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="ed9db-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed9db-120">PARAMETERS</span></span>

### <span data-ttu-id="ed9db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9db-121">-DefaultProfile</span></span>
<span data-ttu-id="ed9db-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9db-123">-ID</span><span class="sxs-lookup"><span data-stu-id="ed9db-123">-Id</span></span>
<span data-ttu-id="ed9db-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="ed9db-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ed9db-125">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ed9db-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9db-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ed9db-126">-ManagementGroupId</span></span>
<span data-ttu-id="ed9db-127">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="ed9db-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9db-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed9db-128">-Name</span></span>
<span data-ttu-id="ed9db-129">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="ed9db-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9db-130">-För</span><span class="sxs-lookup"><span data-stu-id="ed9db-130">-Pre</span></span>
<span data-ttu-id="ed9db-131">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ed9db-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ed9db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9db-132">CommonParameters</span></span>
<span data-ttu-id="ed9db-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9db-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed9db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9db-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed9db-135">INPUTS</span></span>

### <span data-ttu-id="ed9db-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="ed9db-136">None</span></span>

## <span data-ttu-id="ed9db-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed9db-137">OUTPUTS</span></span>

### <span data-ttu-id="ed9db-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ed9db-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ed9db-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed9db-139">NOTES</span></span>

## <span data-ttu-id="ed9db-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed9db-140">RELATED LINKS</span></span>
