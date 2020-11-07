---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3db7d3b0b27cd49207871ba7b9d47d5b79e661fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923842"
---
# <span data-ttu-id="e5100-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e5100-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="e5100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5100-102">SYNOPSIS</span></span>
<span data-ttu-id="e5100-103">Tar bort en distribution och eventuella associerade åtgärder</span><span class="sxs-lookup"><span data-stu-id="e5100-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="e5100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5100-104">SYNTAX</span></span>

### <span data-ttu-id="e5100-105">RemoveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="e5100-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5100-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e5100-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5100-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5100-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5100-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5100-108">DESCRIPTION</span></span>
<span data-ttu-id="e5100-109">Cmdleten **Remove-AzDeployment** tar bort en Azure-distribution i prenumerations omfattning och tillhör ande åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e5100-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="e5100-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5100-110">EXAMPLES</span></span>

### <span data-ttu-id="e5100-111">Exempel 1: ta bort en distribution med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="e5100-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="e5100-112">Det här kommandot tar bort distributionen "RolesDeployment" i aktuell prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="e5100-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="e5100-113">Exempel 2: skaffa en distribution och ta bort den</span><span class="sxs-lookup"><span data-stu-id="e5100-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="e5100-114">Det här kommandot får distributionen "RolesDeployment" vid den aktuella prenumerations omfattningen och tar bort den.</span><span class="sxs-lookup"><span data-stu-id="e5100-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="e5100-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5100-115">PARAMETERS</span></span>

### <span data-ttu-id="e5100-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5100-116">-ApiVersion</span></span>
<span data-ttu-id="e5100-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e5100-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5100-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="e5100-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e5100-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5100-119">-AsJob</span></span>
<span data-ttu-id="e5100-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e5100-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5100-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5100-121">-DefaultProfile</span></span>
<span data-ttu-id="e5100-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5100-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5100-123">-ID</span><span class="sxs-lookup"><span data-stu-id="e5100-123">-Id</span></span>
<span data-ttu-id="e5100-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="e5100-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e5100-125">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="e5100-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="e5100-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5100-126">-InputObject</span></span>
<span data-ttu-id="e5100-127">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="e5100-127">The deployment object.</span></span>

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

### <span data-ttu-id="e5100-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5100-128">-Name</span></span>
<span data-ttu-id="e5100-129">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="e5100-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="e5100-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5100-130">-PassThru</span></span>
<span data-ttu-id="e5100-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e5100-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e5100-132">-För</span><span class="sxs-lookup"><span data-stu-id="e5100-132">-Pre</span></span>
<span data-ttu-id="e5100-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e5100-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e5100-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5100-134">-Confirm</span></span>
<span data-ttu-id="e5100-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5100-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5100-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5100-136">-WhatIf</span></span>
<span data-ttu-id="e5100-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5100-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5100-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5100-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5100-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5100-139">CommonParameters</span></span>
<span data-ttu-id="e5100-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5100-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5100-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5100-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5100-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5100-142">INPUTS</span></span>

### <span data-ttu-id="e5100-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e5100-143">System.String</span></span>

## <span data-ttu-id="e5100-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5100-144">OUTPUTS</span></span>

### <span data-ttu-id="e5100-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5100-145">System.Boolean</span></span>

## <span data-ttu-id="e5100-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5100-146">NOTES</span></span>

## <span data-ttu-id="e5100-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5100-147">RELATED LINKS</span></span>
