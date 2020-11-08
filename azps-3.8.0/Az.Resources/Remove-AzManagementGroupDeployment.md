---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089495"
---
# <span data-ttu-id="f98d3-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f98d3-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="f98d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f98d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f98d3-103">Tar bort en distribution i en hanterings grupp och tillhör ande åtgärder</span><span class="sxs-lookup"><span data-stu-id="f98d3-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="f98d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f98d3-104">SYNTAX</span></span>

### <span data-ttu-id="f98d3-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="f98d3-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f98d3-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f98d3-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98d3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f98d3-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98d3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f98d3-108">DESCRIPTION</span></span>
<span data-ttu-id="f98d3-109">Cmdleten **Remove-AzManagementGroupDeployment** tar bort en Azure-distribution i en hanterings grupp och tillhör ande åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f98d3-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="f98d3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f98d3-110">EXAMPLES</span></span>

### <span data-ttu-id="f98d3-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="f98d3-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="f98d3-112">Det här kommandot tar bort distributionen "RolesDeployment" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="f98d3-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="f98d3-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="f98d3-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="f98d3-114">Det här kommandot får distributionen "RolesDeployment" i hanterings gruppen "myMG" och tar bort den.</span><span class="sxs-lookup"><span data-stu-id="f98d3-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="f98d3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f98d3-115">PARAMETERS</span></span>

### <span data-ttu-id="f98d3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f98d3-116">-ApiVersion</span></span>
<span data-ttu-id="f98d3-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f98d3-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f98d3-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f98d3-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f98d3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f98d3-119">-AsJob</span></span>
<span data-ttu-id="f98d3-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f98d3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f98d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98d3-121">-DefaultProfile</span></span>
<span data-ttu-id="f98d3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f98d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98d3-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f98d3-123">-Id</span></span>
<span data-ttu-id="f98d3-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f98d3-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f98d3-125">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f98d3-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f98d3-126">-InputObject</span></span>
<span data-ttu-id="f98d3-127">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="f98d3-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f98d3-128">-ManagementGroupId</span></span>
<span data-ttu-id="f98d3-129">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="f98d3-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f98d3-130">-Name</span></span>
<span data-ttu-id="f98d3-131">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="f98d3-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f98d3-132">-PassThru</span></span>
<span data-ttu-id="f98d3-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f98d3-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f98d3-134">-För</span><span class="sxs-lookup"><span data-stu-id="f98d3-134">-Pre</span></span>
<span data-ttu-id="f98d3-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f98d3-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f98d3-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f98d3-136">-Confirm</span></span>
<span data-ttu-id="f98d3-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f98d3-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98d3-138">-WhatIf</span></span>
<span data-ttu-id="f98d3-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f98d3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98d3-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f98d3-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98d3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98d3-141">CommonParameters</span></span>
<span data-ttu-id="f98d3-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98d3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98d3-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f98d3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98d3-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f98d3-144">INPUTS</span></span>

### <span data-ttu-id="f98d3-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f98d3-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f98d3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f98d3-146">OUTPUTS</span></span>

### <span data-ttu-id="f98d3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f98d3-147">System.Boolean</span></span>

## <span data-ttu-id="f98d3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f98d3-148">NOTES</span></span>

## <span data-ttu-id="f98d3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f98d3-149">RELATED LINKS</span></span>
