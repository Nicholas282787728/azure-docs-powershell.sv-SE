---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523759"
---
# <span data-ttu-id="eb9ad-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="eb9ad-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="eb9ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9ad-103">Tar bort en distribution med klient omfattningen och eventuella associerade åtgärder</span><span class="sxs-lookup"><span data-stu-id="eb9ad-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="eb9ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb9ad-104">SYNTAX</span></span>

### <span data-ttu-id="eb9ad-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="eb9ad-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb9ad-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="eb9ad-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb9ad-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb9ad-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb9ad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb9ad-108">DESCRIPTION</span></span>
<span data-ttu-id="eb9ad-109">Cmdleten **Remove-AzTenantDeployment** tar bort en Azure-distribution för det aktuella klient-scopet och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="eb9ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb9ad-110">EXAMPLES</span></span>

### <span data-ttu-id="eb9ad-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="eb9ad-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="eb9ad-112">Det här kommandot tar bort distributionen "RolesDeployment" med den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="eb9ad-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="eb9ad-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="eb9ad-114">Det här kommandot får distributionen "RolesDeployment" vid den aktuella klient omfattningen och tar bort det.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="eb9ad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb9ad-115">PARAMETERS</span></span>

### <span data-ttu-id="eb9ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb9ad-116">-AsJob</span></span>
<span data-ttu-id="eb9ad-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eb9ad-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb9ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9ad-118">-DefaultProfile</span></span>
<span data-ttu-id="eb9ad-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb9ad-120">-ID</span><span class="sxs-lookup"><span data-stu-id="eb9ad-120">-Id</span></span>
<span data-ttu-id="eb9ad-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="eb9ad-122">exempel:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="eb9ad-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="eb9ad-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb9ad-123">-InputObject</span></span>
<span data-ttu-id="eb9ad-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-124">The deployment object.</span></span>

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

### <span data-ttu-id="eb9ad-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb9ad-125">-Name</span></span>
<span data-ttu-id="eb9ad-126">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9ad-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb9ad-127">-PassThru</span></span>
<span data-ttu-id="eb9ad-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eb9ad-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="eb9ad-129">-För</span><span class="sxs-lookup"><span data-stu-id="eb9ad-129">-Pre</span></span>
<span data-ttu-id="eb9ad-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eb9ad-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb9ad-131">-Confirm</span></span>
<span data-ttu-id="eb9ad-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9ad-133">-WhatIf</span></span>
<span data-ttu-id="eb9ad-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb9ad-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9ad-136">CommonParameters</span></span>
<span data-ttu-id="eb9ad-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9ad-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb9ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9ad-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb9ad-139">INPUTS</span></span>

### <span data-ttu-id="eb9ad-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="eb9ad-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="eb9ad-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb9ad-141">OUTPUTS</span></span>

### <span data-ttu-id="eb9ad-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb9ad-142">System.Boolean</span></span>

## <span data-ttu-id="eb9ad-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb9ad-143">NOTES</span></span>

## <span data-ttu-id="eb9ad-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb9ad-144">RELATED LINKS</span></span>
