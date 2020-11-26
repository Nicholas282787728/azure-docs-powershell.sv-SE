---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269110"
---
# <span data-ttu-id="b8167-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b8167-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="b8167-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8167-102">SYNOPSIS</span></span>
<span data-ttu-id="b8167-103">Tar bort en distribution och eventuella associerade åtgärder</span><span class="sxs-lookup"><span data-stu-id="b8167-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="b8167-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8167-104">SYNTAX</span></span>

### <span data-ttu-id="b8167-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8167-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8167-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b8167-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8167-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b8167-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8167-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8167-108">DESCRIPTION</span></span>
<span data-ttu-id="b8167-109">Cmdleten **Remove-AzDeployment** tar bort en Azure-distribution i prenumerations omfattning och tillhör ande åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b8167-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="b8167-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8167-110">EXAMPLES</span></span>

### <span data-ttu-id="b8167-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="b8167-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="b8167-112">Det här kommandot tar bort distributionen "RolesDeployment" i aktuell prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="b8167-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="b8167-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="b8167-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="b8167-114">Det här kommandot får distributionen "RolesDeployment" vid den aktuella prenumerations omfattningen och tar bort den.</span><span class="sxs-lookup"><span data-stu-id="b8167-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="b8167-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8167-115">PARAMETERS</span></span>

### <span data-ttu-id="b8167-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8167-116">-AsJob</span></span>
<span data-ttu-id="b8167-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b8167-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8167-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8167-118">-DefaultProfile</span></span>
<span data-ttu-id="b8167-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8167-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8167-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b8167-120">-Id</span></span>
<span data-ttu-id="b8167-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="b8167-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b8167-122">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b8167-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b8167-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8167-123">-InputObject</span></span>
<span data-ttu-id="b8167-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="b8167-124">The deployment object.</span></span>

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

### <span data-ttu-id="b8167-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8167-125">-Name</span></span>
<span data-ttu-id="b8167-126">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="b8167-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="b8167-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8167-127">-PassThru</span></span>
<span data-ttu-id="b8167-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b8167-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b8167-129">-För</span><span class="sxs-lookup"><span data-stu-id="b8167-129">-Pre</span></span>
<span data-ttu-id="b8167-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b8167-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b8167-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8167-131">-Confirm</span></span>
<span data-ttu-id="b8167-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8167-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8167-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8167-133">-WhatIf</span></span>
<span data-ttu-id="b8167-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8167-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8167-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8167-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8167-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8167-136">CommonParameters</span></span>
<span data-ttu-id="b8167-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8167-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8167-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8167-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8167-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8167-139">INPUTS</span></span>

### <span data-ttu-id="b8167-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b8167-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b8167-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8167-141">OUTPUTS</span></span>

### <span data-ttu-id="b8167-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8167-142">System.Boolean</span></span>

## <span data-ttu-id="b8167-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8167-143">NOTES</span></span>

## <span data-ttu-id="b8167-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8167-144">RELATED LINKS</span></span>