---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258031"
---
# <span data-ttu-id="208db-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="208db-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="208db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="208db-102">SYNOPSIS</span></span>
<span data-ttu-id="208db-103">Avbryta en pågående distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="208db-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="208db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="208db-104">SYNTAX</span></span>

### <span data-ttu-id="208db-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="208db-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="208db-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="208db-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208db-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="208db-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208db-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="208db-108">DESCRIPTION</span></span>
<span data-ttu-id="208db-109">Cmdleten **Stop-AzManagementGroupDeployment** avbryter en distribution som har startat men inte slutförts i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="208db-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="208db-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="208db-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="208db-111">Använd New-AzManagementGroupDeployment cmdlet för att skapa en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="208db-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="208db-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="208db-112">EXAMPLES</span></span>

### <span data-ttu-id="208db-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="208db-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="208db-114">Det här kommandot avbryter en drift sättning "deployment01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="208db-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="208db-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="208db-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="208db-116">Det här kommandot får distributionen "deployment01" i hanterings gruppen "myMG" och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="208db-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="208db-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="208db-117">PARAMETERS</span></span>

### <span data-ttu-id="208db-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="208db-118">-ApiVersion</span></span>
<span data-ttu-id="208db-119">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="208db-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="208db-120">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="208db-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="208db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208db-121">-DefaultProfile</span></span>
<span data-ttu-id="208db-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="208db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="208db-123">-ID</span><span class="sxs-lookup"><span data-stu-id="208db-123">-Id</span></span>
<span data-ttu-id="208db-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="208db-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="208db-125">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="208db-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208db-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="208db-126">-InputObject</span></span>
<span data-ttu-id="208db-127">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="208db-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208db-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="208db-128">-ManagementGroupId</span></span>
<span data-ttu-id="208db-129">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="208db-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208db-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="208db-130">-Name</span></span>
<span data-ttu-id="208db-131">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="208db-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208db-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="208db-132">-PassThru</span></span>
<span data-ttu-id="208db-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="208db-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="208db-134">-För</span><span class="sxs-lookup"><span data-stu-id="208db-134">-Pre</span></span>
<span data-ttu-id="208db-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="208db-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="208db-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="208db-136">-Confirm</span></span>
<span data-ttu-id="208db-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="208db-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208db-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208db-138">-WhatIf</span></span>
<span data-ttu-id="208db-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="208db-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208db-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="208db-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208db-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208db-141">CommonParameters</span></span>
<span data-ttu-id="208db-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208db-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208db-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="208db-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208db-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="208db-144">INPUTS</span></span>

### <span data-ttu-id="208db-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="208db-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="208db-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="208db-146">OUTPUTS</span></span>

### <span data-ttu-id="208db-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="208db-147">System.Boolean</span></span>

## <span data-ttu-id="208db-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="208db-148">NOTES</span></span>

## <span data-ttu-id="208db-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="208db-149">RELATED LINKS</span></span>
