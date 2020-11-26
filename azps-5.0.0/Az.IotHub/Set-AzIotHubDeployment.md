---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273481"
---
# <span data-ttu-id="89f37-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="89f37-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="89f37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89f37-102">SYNOPSIS</span></span>
<span data-ttu-id="89f37-103">Uppdatera mutable-fälten i en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="89f37-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="89f37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89f37-104">SYNTAX</span></span>

### <span data-ttu-id="89f37-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="89f37-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f37-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89f37-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f37-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89f37-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f37-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89f37-108">DESCRIPTION</span></span>
<span data-ttu-id="89f37-109">Uppdatera angivna egenskaper för en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="89f37-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="89f37-110">Obs! konfigurations innehåll ändras inte.</span><span class="sxs-lookup"><span data-stu-id="89f37-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="89f37-111">Konfigurations egenskaper som kan uppdateras är ' etiketter ', ' mått ', ' Priority ' och ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="89f37-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="89f37-112">Mer https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  information finns i.</span><span class="sxs-lookup"><span data-stu-id="89f37-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="89f37-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89f37-113">EXAMPLES</span></span>

### <span data-ttu-id="89f37-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89f37-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="89f37-115">Ändra prioriteten för IoT Edge Deployment och uppdatera dess mål villkor.</span><span class="sxs-lookup"><span data-stu-id="89f37-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="89f37-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89f37-116">PARAMETERS</span></span>

### <span data-ttu-id="89f37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f37-117">-DefaultProfile</span></span>
<span data-ttu-id="89f37-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89f37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f37-119">-Force</span><span class="sxs-lookup"><span data-stu-id="89f37-119">-Force</span></span>
<span data-ttu-id="89f37-120">Gör det möjligt att ersätta distributions objekt även om det har uppdaterats sedan det hämtades förra gången.</span><span class="sxs-lookup"><span data-stu-id="89f37-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="89f37-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89f37-121">-InputObject</span></span>
<span data-ttu-id="89f37-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="89f37-122">IotHub object</span></span>

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

### <span data-ttu-id="89f37-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="89f37-123">-IotHubName</span></span>
<span data-ttu-id="89f37-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="89f37-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="89f37-125">-Etikett</span><span class="sxs-lookup"><span data-stu-id="89f37-125">-Label</span></span>
<span data-ttu-id="89f37-126">Kart karta som ska användas för mål distribution.</span><span class="sxs-lookup"><span data-stu-id="89f37-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="89f37-127">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="89f37-127">-Metric</span></span>
<span data-ttu-id="89f37-128">Samling med frågor om IoT Edge Deployment Metrics.</span><span class="sxs-lookup"><span data-stu-id="89f37-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="89f37-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="89f37-129">-Name</span></span>
<span data-ttu-id="89f37-130">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="89f37-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="89f37-131">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="89f37-131">-Priority</span></span>
<span data-ttu-id="89f37-132">Vikt för drift sättning i händelse av konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="89f37-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="89f37-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f37-133">-ResourceGroupName</span></span>
<span data-ttu-id="89f37-134">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="89f37-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89f37-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89f37-135">-ResourceId</span></span>
<span data-ttu-id="89f37-136">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="89f37-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="89f37-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="89f37-137">-TargetCondition</span></span>
<span data-ttu-id="89f37-138">Mål villkor som en Edge-distribution gäller för.</span><span class="sxs-lookup"><span data-stu-id="89f37-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="89f37-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89f37-139">-Confirm</span></span>
<span data-ttu-id="89f37-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89f37-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f37-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f37-141">-WhatIf</span></span>
<span data-ttu-id="89f37-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89f37-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f37-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89f37-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f37-144">CommonParameters</span></span>
<span data-ttu-id="89f37-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f37-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f37-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f37-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89f37-147">INPUTS</span></span>

### <span data-ttu-id="89f37-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="89f37-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="89f37-149">System. String</span><span class="sxs-lookup"><span data-stu-id="89f37-149">System.String</span></span>

## <span data-ttu-id="89f37-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89f37-150">OUTPUTS</span></span>

### <span data-ttu-id="89f37-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="89f37-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="89f37-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89f37-152">NOTES</span></span>

## <span data-ttu-id="89f37-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89f37-153">RELATED LINKS</span></span>