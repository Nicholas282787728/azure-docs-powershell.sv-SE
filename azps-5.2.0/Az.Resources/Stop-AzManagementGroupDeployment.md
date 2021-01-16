---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407656"
---
# <span data-ttu-id="3597f-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3597f-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="3597f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3597f-102">SYNOPSIS</span></span>
<span data-ttu-id="3597f-103">Avbryta en pågående distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="3597f-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="3597f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3597f-104">SYNTAX</span></span>

### <span data-ttu-id="3597f-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="3597f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3597f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3597f-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3597f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="3597f-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3597f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3597f-108">DESCRIPTION</span></span>
<span data-ttu-id="3597f-109">Cmdleten **Stop-AzManagementGroupDeployment** avbryter en distribution som har startat men inte slutförts i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="3597f-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="3597f-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="3597f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="3597f-111">Använd New-AzManagementGroupDeployment cmdlet för att skapa en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="3597f-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="3597f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3597f-112">EXAMPLES</span></span>

### <span data-ttu-id="3597f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3597f-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="3597f-114">Det här kommandot avbryter en drift sättning "deployment01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="3597f-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="3597f-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3597f-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="3597f-116">Det här kommandot får distributionen "deployment01" i hanterings gruppen "myMG" och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="3597f-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="3597f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3597f-117">PARAMETERS</span></span>

### <span data-ttu-id="3597f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3597f-118">-DefaultProfile</span></span>
<span data-ttu-id="3597f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3597f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3597f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="3597f-120">-Id</span></span>
<span data-ttu-id="3597f-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="3597f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3597f-122">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3597f-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3597f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3597f-123">-InputObject</span></span>
<span data-ttu-id="3597f-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="3597f-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3597f-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3597f-125">-ManagementGroupId</span></span>
<span data-ttu-id="3597f-126">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="3597f-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3597f-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="3597f-127">-Name</span></span>
<span data-ttu-id="3597f-128">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="3597f-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3597f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3597f-129">-PassThru</span></span>
<span data-ttu-id="3597f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3597f-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3597f-131">-För</span><span class="sxs-lookup"><span data-stu-id="3597f-131">-Pre</span></span>
<span data-ttu-id="3597f-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3597f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3597f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3597f-133">-Confirm</span></span>
<span data-ttu-id="3597f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3597f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3597f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3597f-135">-WhatIf</span></span>
<span data-ttu-id="3597f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3597f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3597f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3597f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3597f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3597f-138">CommonParameters</span></span>
<span data-ttu-id="3597f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3597f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3597f-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3597f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3597f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3597f-141">INPUTS</span></span>

### <span data-ttu-id="3597f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3597f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3597f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3597f-143">OUTPUTS</span></span>

### <span data-ttu-id="3597f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3597f-144">System.Boolean</span></span>

## <span data-ttu-id="3597f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3597f-145">NOTES</span></span>

## <span data-ttu-id="3597f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3597f-146">RELATED LINKS</span></span>
