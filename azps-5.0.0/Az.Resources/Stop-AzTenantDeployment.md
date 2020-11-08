---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270256"
---
# <span data-ttu-id="69fef-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="69fef-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="69fef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69fef-102">SYNOPSIS</span></span>
<span data-ttu-id="69fef-103">Avbryta en drift sättnings distribution med klient omfånget</span><span class="sxs-lookup"><span data-stu-id="69fef-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="69fef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69fef-104">SYNTAX</span></span>

### <span data-ttu-id="69fef-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="69fef-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69fef-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="69fef-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69fef-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="69fef-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69fef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69fef-108">DESCRIPTION</span></span>
<span data-ttu-id="69fef-109">Cmdleten **Stop-AzTenantDeployment** avbryter en distribution som har startat men inte slutförts i den aktuella klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="69fef-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="69fef-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="69fef-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="69fef-111">Använd New-AzTenantDeployment cmdlet för att skapa en distribution med klient-scope.</span><span class="sxs-lookup"><span data-stu-id="69fef-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="69fef-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69fef-112">EXAMPLES</span></span>

### <span data-ttu-id="69fef-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69fef-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="69fef-114">Det här kommandot avbryter en drift sättning "deployment01" med den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="69fef-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="69fef-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="69fef-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="69fef-116">Det här kommandot får distributionen "deployment01" i den aktuella klient omfattningen och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="69fef-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="69fef-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69fef-117">PARAMETERS</span></span>

### <span data-ttu-id="69fef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fef-118">-DefaultProfile</span></span>
<span data-ttu-id="69fef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69fef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69fef-120">-ID</span><span class="sxs-lookup"><span data-stu-id="69fef-120">-Id</span></span>
<span data-ttu-id="69fef-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="69fef-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="69fef-122">exempel:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="69fef-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="69fef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69fef-123">-InputObject</span></span>
<span data-ttu-id="69fef-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="69fef-124">The deployment object.</span></span>

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

### <span data-ttu-id="69fef-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="69fef-125">-Name</span></span>
<span data-ttu-id="69fef-126">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="69fef-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69fef-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69fef-127">-PassThru</span></span>
<span data-ttu-id="69fef-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="69fef-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="69fef-129">-För</span><span class="sxs-lookup"><span data-stu-id="69fef-129">-Pre</span></span>
<span data-ttu-id="69fef-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="69fef-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="69fef-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69fef-131">-Confirm</span></span>
<span data-ttu-id="69fef-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69fef-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69fef-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69fef-133">-WhatIf</span></span>
<span data-ttu-id="69fef-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69fef-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69fef-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69fef-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69fef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fef-136">CommonParameters</span></span>
<span data-ttu-id="69fef-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69fef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fef-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69fef-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fef-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69fef-139">INPUTS</span></span>

### <span data-ttu-id="69fef-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="69fef-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="69fef-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69fef-141">OUTPUTS</span></span>

### <span data-ttu-id="69fef-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69fef-142">System.Boolean</span></span>

## <span data-ttu-id="69fef-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69fef-143">NOTES</span></span>

## <span data-ttu-id="69fef-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69fef-144">RELATED LINKS</span></span>
