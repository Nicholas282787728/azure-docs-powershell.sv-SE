---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 7bd45da18565ae408ec71753f7f4527e53c2e4c1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931149"
---
# <span data-ttu-id="cf6ca-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cf6ca-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="cf6ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6ca-103">Tar bort en distribution och eventuella associerade åtgärder</span><span class="sxs-lookup"><span data-stu-id="cf6ca-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf6ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf6ca-104">SYNTAX</span></span>

### <span data-ttu-id="cf6ca-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="cf6ca-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ca-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="cf6ca-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ca-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf6ca-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf6ca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf6ca-108">DESCRIPTION</span></span>
<span data-ttu-id="cf6ca-109">Cmdleten **Remove-AzureRmDeployment** tar bort en Azure-distribution i prenumerations omfattning och tillhör ande åtgärder.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="cf6ca-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf6ca-110">EXAMPLES</span></span>

### <span data-ttu-id="cf6ca-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="cf6ca-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="cf6ca-112">Det här kommandot tar bort distributionen "RolesDeployment" i aktuell prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="cf6ca-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="cf6ca-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="cf6ca-114">Det här kommandot får distributionen "RolesDeployment" vid den aktuella prenumerations omfattningen och tar bort den.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="cf6ca-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf6ca-115">PARAMETERS</span></span>

### <span data-ttu-id="cf6ca-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cf6ca-116">-ApiVersion</span></span>
<span data-ttu-id="cf6ca-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="cf6ca-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="cf6ca-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf6ca-119">-AsJob</span></span>
<span data-ttu-id="cf6ca-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cf6ca-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf6ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6ca-121">-DefaultProfile</span></span>
<span data-ttu-id="cf6ca-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ca-123">-ID</span><span class="sxs-lookup"><span data-stu-id="cf6ca-123">-Id</span></span>
<span data-ttu-id="cf6ca-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="cf6ca-125">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="cf6ca-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="cf6ca-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf6ca-126">-InputObject</span></span>
<span data-ttu-id="cf6ca-127">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-127">The deployment object.</span></span>

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

### <span data-ttu-id="cf6ca-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf6ca-128">-Name</span></span>
<span data-ttu-id="cf6ca-129">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ca-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf6ca-130">-PassThru</span></span>
<span data-ttu-id="cf6ca-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cf6ca-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cf6ca-132">-För</span><span class="sxs-lookup"><span data-stu-id="cf6ca-132">-Pre</span></span>
<span data-ttu-id="cf6ca-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cf6ca-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf6ca-134">-Confirm</span></span>
<span data-ttu-id="cf6ca-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf6ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf6ca-136">-WhatIf</span></span>
<span data-ttu-id="cf6ca-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf6ca-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf6ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6ca-139">CommonParameters</span></span>
<span data-ttu-id="cf6ca-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6ca-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf6ca-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6ca-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf6ca-142">INPUTS</span></span>

### <span data-ttu-id="cf6ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cf6ca-143">System.String</span></span>

## <span data-ttu-id="cf6ca-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf6ca-144">OUTPUTS</span></span>

### <span data-ttu-id="cf6ca-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf6ca-145">System.Boolean</span></span>

## <span data-ttu-id="cf6ca-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf6ca-146">NOTES</span></span>

## <span data-ttu-id="cf6ca-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf6ca-147">RELATED LINKS</span></span>
