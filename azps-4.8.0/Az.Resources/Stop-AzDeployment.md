---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 366bbdf03b5fc7a23e6b71e03e1c3f1652925e7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259130"
---
# <span data-ttu-id="d3730-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d3730-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="d3730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3730-102">SYNOPSIS</span></span>
<span data-ttu-id="d3730-103">Avbryta en pågående installation</span><span class="sxs-lookup"><span data-stu-id="d3730-103">Cancel a running deployment</span></span>

## <span data-ttu-id="d3730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3730-104">SYNTAX</span></span>

### <span data-ttu-id="d3730-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d3730-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3730-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d3730-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3730-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3730-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3730-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3730-108">DESCRIPTION</span></span>
<span data-ttu-id="d3730-109">Cmdleten **Stop-AzDeployment** avbryter en distribution vid en prenumeration som har startat men inte slutförts.</span><span class="sxs-lookup"><span data-stu-id="d3730-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="d3730-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="d3730-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="d3730-111">Om du vill skapa en distributions prenumerations omfattning använder du New-AzDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3730-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="d3730-112">Denna cmdlet stoppar bara en drift sättning.</span><span class="sxs-lookup"><span data-stu-id="d3730-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="d3730-113">Använd parametern *namn* för att stoppa en specifik distribution.</span><span class="sxs-lookup"><span data-stu-id="d3730-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="d3730-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3730-114">EXAMPLES</span></span>

### <span data-ttu-id="d3730-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3730-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="d3730-116">Det här kommandot avbryter en drift sättning "deployment01" för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d3730-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="d3730-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d3730-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="d3730-118">Det här kommandot får distributionen "deployment01" vid den aktuella prenumerations omfattningen och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="d3730-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="d3730-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3730-119">PARAMETERS</span></span>

### <span data-ttu-id="d3730-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d3730-120">-ApiVersion</span></span>
<span data-ttu-id="d3730-121">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d3730-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d3730-122">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="d3730-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3730-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3730-123">-DefaultProfile</span></span>
<span data-ttu-id="d3730-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3730-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3730-125">-ID</span><span class="sxs-lookup"><span data-stu-id="d3730-125">-Id</span></span>
<span data-ttu-id="d3730-126">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="d3730-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d3730-127">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d3730-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="d3730-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3730-128">-InputObject</span></span>
<span data-ttu-id="d3730-129">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="d3730-129">The deployment object.</span></span>

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

### <span data-ttu-id="d3730-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3730-130">-Name</span></span>
<span data-ttu-id="d3730-131">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="d3730-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="d3730-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3730-132">-PassThru</span></span>
<span data-ttu-id="d3730-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d3730-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d3730-134">-För</span><span class="sxs-lookup"><span data-stu-id="d3730-134">-Pre</span></span>
<span data-ttu-id="d3730-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d3730-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d3730-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3730-136">-Confirm</span></span>
<span data-ttu-id="d3730-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3730-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3730-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3730-138">-WhatIf</span></span>
<span data-ttu-id="d3730-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3730-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3730-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3730-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3730-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3730-141">CommonParameters</span></span>
<span data-ttu-id="d3730-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3730-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3730-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3730-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3730-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3730-144">INPUTS</span></span>

### <span data-ttu-id="d3730-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d3730-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d3730-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3730-146">OUTPUTS</span></span>

### <span data-ttu-id="d3730-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3730-147">System.Boolean</span></span>

## <span data-ttu-id="d3730-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3730-148">NOTES</span></span>

## <span data-ttu-id="d3730-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3730-149">RELATED LINKS</span></span>
