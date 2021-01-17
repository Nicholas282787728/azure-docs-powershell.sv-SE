---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389991"
---
# <span data-ttu-id="f110b-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f110b-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="f110b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f110b-102">SYNOPSIS</span></span>
<span data-ttu-id="f110b-103">Uppdatera mutable-fälten i en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="f110b-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="f110b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f110b-104">SYNTAX</span></span>

### <span data-ttu-id="f110b-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f110b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f110b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f110b-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f110b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f110b-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f110b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f110b-108">DESCRIPTION</span></span>
<span data-ttu-id="f110b-109">Uppdatera angivna egenskaper för en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="f110b-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="f110b-110">Obs! konfigurations innehåll ändras inte.</span><span class="sxs-lookup"><span data-stu-id="f110b-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="f110b-111">Konfigurations egenskaper som kan uppdateras är ' etiketter ', ' mått ', ' Priority ' och ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="f110b-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="f110b-112">Mer https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  information finns i.</span><span class="sxs-lookup"><span data-stu-id="f110b-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="f110b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f110b-113">EXAMPLES</span></span>

### <span data-ttu-id="f110b-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f110b-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="f110b-115">Ändra prioriteten för IoT Edge Deployment och uppdatera dess mål villkor.</span><span class="sxs-lookup"><span data-stu-id="f110b-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="f110b-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f110b-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="f110b-117">Uppdatera måtten och etiketterna för en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="f110b-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="f110b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f110b-118">PARAMETERS</span></span>

### <span data-ttu-id="f110b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f110b-119">-DefaultProfile</span></span>
<span data-ttu-id="f110b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f110b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f110b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f110b-121">-Force</span></span>
<span data-ttu-id="f110b-122">Gör det möjligt att ersätta distributions objekt även om det har uppdaterats sedan det hämtades förra gången.</span><span class="sxs-lookup"><span data-stu-id="f110b-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="f110b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f110b-123">-InputObject</span></span>
<span data-ttu-id="f110b-124">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="f110b-124">IotHub object</span></span>

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

### <span data-ttu-id="f110b-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f110b-125">-IotHubName</span></span>
<span data-ttu-id="f110b-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="f110b-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f110b-127">-Etikett</span><span class="sxs-lookup"><span data-stu-id="f110b-127">-Label</span></span>
<span data-ttu-id="f110b-128">Kart karta som ska användas för mål distribution.</span><span class="sxs-lookup"><span data-stu-id="f110b-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="f110b-129">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="f110b-129">-Metric</span></span>
<span data-ttu-id="f110b-130">Samling med frågor om IoT Edge Deployment Metrics.</span><span class="sxs-lookup"><span data-stu-id="f110b-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="f110b-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="f110b-131">-Name</span></span>
<span data-ttu-id="f110b-132">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f110b-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="f110b-133">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="f110b-133">-Priority</span></span>
<span data-ttu-id="f110b-134">Vikt för drift sättning i händelse av konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="f110b-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="f110b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f110b-135">-ResourceGroupName</span></span>
<span data-ttu-id="f110b-136">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f110b-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f110b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f110b-137">-ResourceId</span></span>
<span data-ttu-id="f110b-138">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="f110b-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f110b-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="f110b-139">-TargetCondition</span></span>
<span data-ttu-id="f110b-140">Mål villkor som en Edge-distribution gäller för.</span><span class="sxs-lookup"><span data-stu-id="f110b-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="f110b-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f110b-141">-Confirm</span></span>
<span data-ttu-id="f110b-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f110b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f110b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f110b-143">-WhatIf</span></span>
<span data-ttu-id="f110b-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f110b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f110b-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f110b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f110b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f110b-146">CommonParameters</span></span>
<span data-ttu-id="f110b-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f110b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f110b-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f110b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f110b-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f110b-149">INPUTS</span></span>

### <span data-ttu-id="f110b-150">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f110b-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f110b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f110b-151">System.String</span></span>

## <span data-ttu-id="f110b-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f110b-152">OUTPUTS</span></span>

### <span data-ttu-id="f110b-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f110b-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="f110b-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f110b-154">NOTES</span></span>

## <span data-ttu-id="f110b-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f110b-155">RELATED LINKS</span></span>
