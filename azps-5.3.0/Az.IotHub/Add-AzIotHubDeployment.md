---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526046"
---
# <span data-ttu-id="c0013-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c0013-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="c0013-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0013-102">SYNOPSIS</span></span>
<span data-ttu-id="c0013-103">Lägga till en IoT Edge-distribution i en måls IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c0013-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="c0013-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0013-104">SYNTAX</span></span>

### <span data-ttu-id="c0013-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c0013-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0013-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0013-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0013-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0013-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0013-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0013-108">DESCRIPTION</span></span>
<span data-ttu-id="c0013-109">Edge-driftsättningar kan skapas med användardefinierade mått för utvärdering av en begäran.</span><span class="sxs-lookup"><span data-stu-id="c0013-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="c0013-110">Mer https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring information finns i.</span><span class="sxs-lookup"><span data-stu-id="c0013-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="c0013-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0013-111">EXAMPLES</span></span>

### <span data-ttu-id="c0013-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0013-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="c0013-113">Skapa en Edge-distribution med standardmetadata.</span><span class="sxs-lookup"><span data-stu-id="c0013-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="c0013-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0013-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="c0013-115">Skapa en Edge-distribution med prioriteten 3 som gäller för villkor när en enhet är märkt i byggnad 9 och miljön är "test".</span><span class="sxs-lookup"><span data-stu-id="c0013-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="c0013-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0013-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="c0013-117">Skapa en Edge-distribution med användar mått.</span><span class="sxs-lookup"><span data-stu-id="c0013-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="c0013-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c0013-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="c0013-119">Skapa en Edge-distribution med etiketter.</span><span class="sxs-lookup"><span data-stu-id="c0013-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="c0013-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c0013-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="c0013-121">Skapa en Edge-distribution med innehåll.</span><span class="sxs-lookup"><span data-stu-id="c0013-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="c0013-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0013-122">PARAMETERS</span></span>

### <span data-ttu-id="c0013-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0013-123">-DefaultProfile</span></span>
<span data-ttu-id="c0013-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0013-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0013-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0013-125">-InputObject</span></span>
<span data-ttu-id="c0013-126">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="c0013-126">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c0013-127">-IotHubName</span></span>
<span data-ttu-id="c0013-128">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c0013-128">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-129">-Etikett</span><span class="sxs-lookup"><span data-stu-id="c0013-129">-Label</span></span>
<span data-ttu-id="c0013-130">Kart karta som ska användas för mål distribution.</span><span class="sxs-lookup"><span data-stu-id="c0013-130">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-131">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="c0013-131">-Metric</span></span>
<span data-ttu-id="c0013-132">Samling med frågor om IoT Edge Deployment Metrics.</span><span class="sxs-lookup"><span data-stu-id="c0013-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="c0013-133">-ModulesContent</span></span>
<span data-ttu-id="c0013-134">Distributions innehåll i moduler för IoT Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="c0013-134">Deployment content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0013-135">-Name</span></span>
<span data-ttu-id="c0013-136">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="c0013-136">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-137">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="c0013-137">-Priority</span></span>
<span data-ttu-id="c0013-138">Vikt för drift sättning i händelse av konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="c0013-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0013-139">-ResourceGroupName</span></span>
<span data-ttu-id="c0013-140">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c0013-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0013-141">-ResourceId</span></span>
<span data-ttu-id="c0013-142">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="c0013-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0013-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="c0013-143">-TargetCondition</span></span>
<span data-ttu-id="c0013-144">Mål villkor som en Edge-distribution gäller för.</span><span class="sxs-lookup"><span data-stu-id="c0013-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="c0013-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0013-145">-Confirm</span></span>
<span data-ttu-id="c0013-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0013-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0013-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0013-147">-WhatIf</span></span>
<span data-ttu-id="c0013-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0013-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0013-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0013-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0013-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0013-150">CommonParameters</span></span>
<span data-ttu-id="c0013-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0013-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0013-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0013-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0013-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0013-153">INPUTS</span></span>

### <span data-ttu-id="c0013-154">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c0013-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c0013-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c0013-155">System.String</span></span>

## <span data-ttu-id="c0013-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0013-156">OUTPUTS</span></span>

### <span data-ttu-id="c0013-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c0013-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="c0013-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0013-158">NOTES</span></span>

## <span data-ttu-id="c0013-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0013-159">RELATED LINKS</span></span>
