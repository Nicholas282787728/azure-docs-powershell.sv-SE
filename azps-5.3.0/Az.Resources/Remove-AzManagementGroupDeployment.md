---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521307"
---
# <span data-ttu-id="d5077-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d5077-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d5077-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5077-102">SYNOPSIS</span></span>
<span data-ttu-id="d5077-103">Tar bort en distribution i en hanterings grupp och tillhör ande åtgärder</span><span class="sxs-lookup"><span data-stu-id="d5077-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="d5077-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5077-104">SYNTAX</span></span>

### <span data-ttu-id="d5077-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d5077-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5077-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d5077-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5077-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5077-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5077-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5077-108">DESCRIPTION</span></span>
<span data-ttu-id="d5077-109">Cmdleten **Remove-AzManagementGroupDeployment** tar bort en Azure-distribution i en hanterings grupp och tillhör ande åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d5077-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="d5077-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5077-110">EXAMPLES</span></span>

### <span data-ttu-id="d5077-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="d5077-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="d5077-112">Det här kommandot tar bort distributionen "RolesDeployment" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="d5077-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="d5077-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="d5077-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="d5077-114">Det här kommandot får distributionen "RolesDeployment" i hanterings gruppen "myMG" och tar bort den.</span><span class="sxs-lookup"><span data-stu-id="d5077-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="d5077-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5077-115">PARAMETERS</span></span>

### <span data-ttu-id="d5077-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5077-116">-AsJob</span></span>
<span data-ttu-id="d5077-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d5077-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5077-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5077-118">-DefaultProfile</span></span>
<span data-ttu-id="d5077-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5077-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5077-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d5077-120">-Id</span></span>
<span data-ttu-id="d5077-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="d5077-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d5077-122">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d5077-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5077-123">-InputObject</span></span>
<span data-ttu-id="d5077-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="d5077-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d5077-125">-ManagementGroupId</span></span>
<span data-ttu-id="d5077-126">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="d5077-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5077-127">-Name</span></span>
<span data-ttu-id="d5077-128">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="d5077-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5077-129">-PassThru</span></span>
<span data-ttu-id="d5077-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d5077-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d5077-131">-För</span><span class="sxs-lookup"><span data-stu-id="d5077-131">-Pre</span></span>
<span data-ttu-id="d5077-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d5077-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d5077-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5077-133">-Confirm</span></span>
<span data-ttu-id="d5077-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5077-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5077-135">-WhatIf</span></span>
<span data-ttu-id="d5077-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5077-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5077-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5077-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5077-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5077-138">CommonParameters</span></span>
<span data-ttu-id="d5077-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5077-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5077-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5077-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5077-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5077-141">INPUTS</span></span>

### <span data-ttu-id="d5077-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d5077-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d5077-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5077-143">OUTPUTS</span></span>

### <span data-ttu-id="d5077-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5077-144">System.Boolean</span></span>

## <span data-ttu-id="d5077-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5077-145">NOTES</span></span>

## <span data-ttu-id="d5077-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5077-146">RELATED LINKS</span></span>
