---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091973"
---
# <span data-ttu-id="e5287-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5287-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="e5287-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5287-102">SYNOPSIS</span></span>
<span data-ttu-id="e5287-103">Lägga till en IoT-konfiguration för automatisk enhets hantering i en måls IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e5287-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="e5287-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5287-104">SYNTAX</span></span>

### <span data-ttu-id="e5287-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e5287-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5287-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5287-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5287-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5287-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5287-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5287-108">DESCRIPTION</span></span>
<span data-ttu-id="e5287-109">Konfigurations innehåll är JSON och kan variera beroende på enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="e5287-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="e5287-110">Enhets konfigurationerna är i form av {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="e5287-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="e5287-111">Webbplatskonfigurationer är i form av {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="e5287-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="e5287-112">Konfigurationer kan definieras med användarnas mått för utvärdering av en begäran.</span><span class="sxs-lookup"><span data-stu-id="e5287-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="e5287-113">Användar värden är JSON och i form av {"frågor": {...}}</span><span class="sxs-lookup"><span data-stu-id="e5287-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="e5287-114">eller {"Mät värden": {"frågor": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="e5287-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="e5287-115">Obs! mål villkor för moduler måste börja med "från enheter. modules där".</span><span class="sxs-lookup"><span data-stu-id="e5287-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="e5287-116">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management information finns i.</span><span class="sxs-lookup"><span data-stu-id="e5287-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="e5287-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5287-117">EXAMPLES</span></span>

### <span data-ttu-id="e5287-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e5287-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="e5287-119">Skapa en enhets konfiguration med standardmetadata.</span><span class="sxs-lookup"><span data-stu-id="e5287-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="e5287-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e5287-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="e5287-121">Skapa en enhets konfiguration med prioritet 3 som gäller för villkor när en enhet är märkt i byggnad 9 och miljön är "test".</span><span class="sxs-lookup"><span data-stu-id="e5287-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="e5287-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e5287-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="e5287-123">Skapa en enhets konfiguration med användar mått.</span><span class="sxs-lookup"><span data-stu-id="e5287-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="e5287-124">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e5287-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="e5287-125">Skapa en enhets konfiguration med etiketter.</span><span class="sxs-lookup"><span data-stu-id="e5287-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="e5287-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="e5287-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="e5287-127">Skapa en enhets konfiguration med innehåll.</span><span class="sxs-lookup"><span data-stu-id="e5287-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="e5287-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5287-128">PARAMETERS</span></span>

### <span data-ttu-id="e5287-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5287-129">-DefaultProfile</span></span>
<span data-ttu-id="e5287-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5287-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5287-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="e5287-131">-DeviceContent</span></span>
<span data-ttu-id="e5287-132">Konfiguration för IotHub-enheter.</span><span class="sxs-lookup"><span data-stu-id="e5287-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="e5287-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5287-133">-InputObject</span></span>
<span data-ttu-id="e5287-134">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="e5287-134">IotHub object</span></span>

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

### <span data-ttu-id="e5287-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e5287-135">-IotHubName</span></span>
<span data-ttu-id="e5287-136">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e5287-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5287-137">-Etikett</span><span class="sxs-lookup"><span data-stu-id="e5287-137">-Label</span></span>
<span data-ttu-id="e5287-138">Kart karta som ska användas för mål konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5287-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="e5287-139">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="e5287-139">-Metric</span></span>
<span data-ttu-id="e5287-140">Samling med frågor för konfigurations mått.</span><span class="sxs-lookup"><span data-stu-id="e5287-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="e5287-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5287-141">-Name</span></span>
<span data-ttu-id="e5287-142">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e5287-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="e5287-143">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="e5287-143">-Priority</span></span>
<span data-ttu-id="e5287-144">Vikt för enhetens konfiguration om det rör sig om konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="e5287-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="e5287-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5287-145">-ResourceGroupName</span></span>
<span data-ttu-id="e5287-146">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e5287-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5287-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5287-147">-ResourceId</span></span>
<span data-ttu-id="e5287-148">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="e5287-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5287-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="e5287-149">-TargetCondition</span></span>
<span data-ttu-id="e5287-150">Mål villkor där en enhets konfiguration gäller.</span><span class="sxs-lookup"><span data-stu-id="e5287-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="e5287-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5287-151">-Confirm</span></span>
<span data-ttu-id="e5287-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5287-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5287-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5287-153">-WhatIf</span></span>
<span data-ttu-id="e5287-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5287-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5287-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5287-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5287-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5287-156">CommonParameters</span></span>
<span data-ttu-id="e5287-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5287-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5287-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5287-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5287-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5287-159">INPUTS</span></span>

### <span data-ttu-id="e5287-160">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5287-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5287-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e5287-161">System.String</span></span>

## <span data-ttu-id="e5287-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5287-162">OUTPUTS</span></span>

### <span data-ttu-id="e5287-163">Microsoft. Azure. commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5287-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="e5287-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5287-164">NOTES</span></span>

## <span data-ttu-id="e5287-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5287-165">RELATED LINKS</span></span>