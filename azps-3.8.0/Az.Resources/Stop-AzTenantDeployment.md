---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089435"
---
# <span data-ttu-id="bdaca-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bdaca-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="bdaca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdaca-102">SYNOPSIS</span></span>
<span data-ttu-id="bdaca-103">Avbryta en drift sättnings distribution med klient omfånget</span><span class="sxs-lookup"><span data-stu-id="bdaca-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="bdaca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdaca-104">SYNTAX</span></span>

### <span data-ttu-id="bdaca-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="bdaca-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdaca-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bdaca-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdaca-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="bdaca-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdaca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdaca-108">DESCRIPTION</span></span>
<span data-ttu-id="bdaca-109">Cmdleten **Stop-AzTenantDeployment** avbryter en distribution som har startat men inte slutförts i den aktuella klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="bdaca-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="bdaca-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="bdaca-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="bdaca-111">Använd New-AzTenantDeployment cmdlet för att skapa en distribution med klient-scope.</span><span class="sxs-lookup"><span data-stu-id="bdaca-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="bdaca-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdaca-112">EXAMPLES</span></span>

### <span data-ttu-id="bdaca-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bdaca-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="bdaca-114">Det här kommandot avbryter en drift sättning "deployment01" med den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="bdaca-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="bdaca-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bdaca-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="bdaca-116">Det här kommandot får distributionen "deployment01" i den aktuella klient omfattningen och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="bdaca-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="bdaca-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdaca-117">PARAMETERS</span></span>

### <span data-ttu-id="bdaca-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdaca-118">-ApiVersion</span></span>
<span data-ttu-id="bdaca-119">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bdaca-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdaca-120">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="bdaca-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bdaca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdaca-121">-DefaultProfile</span></span>
<span data-ttu-id="bdaca-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdaca-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdaca-123">-ID</span><span class="sxs-lookup"><span data-stu-id="bdaca-123">-Id</span></span>
<span data-ttu-id="bdaca-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="bdaca-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="bdaca-125">exempel:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="bdaca-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="bdaca-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdaca-126">-InputObject</span></span>
<span data-ttu-id="bdaca-127">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="bdaca-127">The deployment object.</span></span>

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

### <span data-ttu-id="bdaca-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="bdaca-128">-Name</span></span>
<span data-ttu-id="bdaca-129">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="bdaca-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdaca-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdaca-130">-PassThru</span></span>
<span data-ttu-id="bdaca-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bdaca-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bdaca-132">-För</span><span class="sxs-lookup"><span data-stu-id="bdaca-132">-Pre</span></span>
<span data-ttu-id="bdaca-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bdaca-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bdaca-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdaca-134">-Confirm</span></span>
<span data-ttu-id="bdaca-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdaca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdaca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdaca-136">-WhatIf</span></span>
<span data-ttu-id="bdaca-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdaca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdaca-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdaca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdaca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdaca-139">CommonParameters</span></span>
<span data-ttu-id="bdaca-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdaca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdaca-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdaca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdaca-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdaca-142">INPUTS</span></span>

### <span data-ttu-id="bdaca-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="bdaca-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="bdaca-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdaca-144">OUTPUTS</span></span>

### <span data-ttu-id="bdaca-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdaca-145">System.Boolean</span></span>

## <span data-ttu-id="bdaca-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdaca-146">NOTES</span></span>

## <span data-ttu-id="bdaca-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdaca-147">RELATED LINKS</span></span>
