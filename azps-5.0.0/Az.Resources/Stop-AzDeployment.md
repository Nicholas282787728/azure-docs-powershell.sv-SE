---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270264"
---
# <span data-ttu-id="228fc-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="228fc-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="228fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="228fc-102">SYNOPSIS</span></span>
<span data-ttu-id="228fc-103">Avbryta en pågående installation</span><span class="sxs-lookup"><span data-stu-id="228fc-103">Cancel a running deployment</span></span>

## <span data-ttu-id="228fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="228fc-104">SYNTAX</span></span>

### <span data-ttu-id="228fc-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="228fc-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="228fc-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="228fc-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="228fc-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="228fc-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228fc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="228fc-108">DESCRIPTION</span></span>
<span data-ttu-id="228fc-109">Cmdleten **Stop-AzDeployment** avbryter en distribution vid en prenumeration som har startat men inte slutförts.</span><span class="sxs-lookup"><span data-stu-id="228fc-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="228fc-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="228fc-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="228fc-111">Om du vill skapa en distributions prenumerations omfattning använder du New-AzDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="228fc-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="228fc-112">Denna cmdlet stoppar bara en drift sättning.</span><span class="sxs-lookup"><span data-stu-id="228fc-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="228fc-113">Använd parametern *namn* för att stoppa en specifik distribution.</span><span class="sxs-lookup"><span data-stu-id="228fc-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="228fc-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="228fc-114">EXAMPLES</span></span>

### <span data-ttu-id="228fc-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="228fc-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="228fc-116">Det här kommandot avbryter en drift sättning "deployment01" för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="228fc-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="228fc-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="228fc-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="228fc-118">Det här kommandot får distributionen "deployment01" vid den aktuella prenumerations omfattningen och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="228fc-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="228fc-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="228fc-119">PARAMETERS</span></span>

### <span data-ttu-id="228fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228fc-120">-DefaultProfile</span></span>
<span data-ttu-id="228fc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="228fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="228fc-122">-ID</span><span class="sxs-lookup"><span data-stu-id="228fc-122">-Id</span></span>
<span data-ttu-id="228fc-123">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="228fc-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="228fc-124">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="228fc-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="228fc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="228fc-125">-InputObject</span></span>
<span data-ttu-id="228fc-126">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="228fc-126">The deployment object.</span></span>

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

### <span data-ttu-id="228fc-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="228fc-127">-Name</span></span>
<span data-ttu-id="228fc-128">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="228fc-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="228fc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="228fc-129">-PassThru</span></span>
<span data-ttu-id="228fc-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="228fc-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="228fc-131">-För</span><span class="sxs-lookup"><span data-stu-id="228fc-131">-Pre</span></span>
<span data-ttu-id="228fc-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="228fc-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="228fc-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="228fc-133">-Confirm</span></span>
<span data-ttu-id="228fc-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="228fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228fc-135">-WhatIf</span></span>
<span data-ttu-id="228fc-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="228fc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228fc-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="228fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228fc-138">CommonParameters</span></span>
<span data-ttu-id="228fc-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228fc-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="228fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228fc-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="228fc-141">INPUTS</span></span>

### <span data-ttu-id="228fc-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="228fc-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="228fc-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="228fc-143">OUTPUTS</span></span>

### <span data-ttu-id="228fc-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="228fc-144">System.Boolean</span></span>

## <span data-ttu-id="228fc-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="228fc-145">NOTES</span></span>

## <span data-ttu-id="228fc-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="228fc-146">RELATED LINKS</span></span>
