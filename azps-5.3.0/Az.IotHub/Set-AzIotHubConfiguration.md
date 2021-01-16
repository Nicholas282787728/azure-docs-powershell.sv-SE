---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425963"
---
# <span data-ttu-id="54cee-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="54cee-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="54cee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54cee-102">SYNOPSIS</span></span>
<span data-ttu-id="54cee-103">Uppdatera mutable-fälten för konfigurations registreringen.</span><span class="sxs-lookup"><span data-stu-id="54cee-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="54cee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54cee-104">SYNTAX</span></span>

### <span data-ttu-id="54cee-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="54cee-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54cee-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54cee-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54cee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54cee-108">DESCRIPTION</span></span>
<span data-ttu-id="54cee-109">Uppdatera angivna egenskaper för en IoT-konfiguration för automatisk enhets hantering.</span><span class="sxs-lookup"><span data-stu-id="54cee-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="54cee-110">Obs! konfigurations innehåll ändras inte.</span><span class="sxs-lookup"><span data-stu-id="54cee-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="54cee-111">Konfigurations egenskaper som kan uppdateras är ' etiketter ', ' mått ', ' Priority ' och ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="54cee-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="54cee-112">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management information finns i.</span><span class="sxs-lookup"><span data-stu-id="54cee-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="54cee-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54cee-113">EXAMPLES</span></span>

### <span data-ttu-id="54cee-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54cee-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="54cee-115">Ändra prioriteten för en enhets konfiguration och uppdatera dess mål villkor</span><span class="sxs-lookup"><span data-stu-id="54cee-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="54cee-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="54cee-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="54cee-117">Uppdatera måtten och etiketterna för en enhets konfiguration</span><span class="sxs-lookup"><span data-stu-id="54cee-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="54cee-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54cee-118">PARAMETERS</span></span>

### <span data-ttu-id="54cee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cee-119">-DefaultProfile</span></span>
<span data-ttu-id="54cee-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54cee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54cee-121">-Force</span><span class="sxs-lookup"><span data-stu-id="54cee-121">-Force</span></span>
<span data-ttu-id="54cee-122">Tillåter att konfigurations objekt byts ut även om det har uppdaterats sedan det hämtades förra gången.</span><span class="sxs-lookup"><span data-stu-id="54cee-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="54cee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54cee-123">-InputObject</span></span>
<span data-ttu-id="54cee-124">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="54cee-124">IotHub object</span></span>

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

### <span data-ttu-id="54cee-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="54cee-125">-IotHubName</span></span>
<span data-ttu-id="54cee-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="54cee-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="54cee-127">-Etikett</span><span class="sxs-lookup"><span data-stu-id="54cee-127">-Label</span></span>
<span data-ttu-id="54cee-128">Kart karta som ska användas för mål konfiguration.</span><span class="sxs-lookup"><span data-stu-id="54cee-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="54cee-129">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="54cee-129">-Metric</span></span>
<span data-ttu-id="54cee-130">Samling med frågor för konfigurations mått.</span><span class="sxs-lookup"><span data-stu-id="54cee-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="54cee-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="54cee-131">-Name</span></span>
<span data-ttu-id="54cee-132">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="54cee-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cee-133">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="54cee-133">-Priority</span></span>
<span data-ttu-id="54cee-134">Vikt för enhetens konfiguration om det rör sig om konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="54cee-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="54cee-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cee-135">-ResourceGroupName</span></span>
<span data-ttu-id="54cee-136">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="54cee-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54cee-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54cee-137">-ResourceId</span></span>
<span data-ttu-id="54cee-138">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="54cee-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="54cee-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="54cee-139">-TargetCondition</span></span>
<span data-ttu-id="54cee-140">Mål villkor där en enhets konfiguration gäller.</span><span class="sxs-lookup"><span data-stu-id="54cee-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="54cee-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54cee-141">-Confirm</span></span>
<span data-ttu-id="54cee-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54cee-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54cee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54cee-143">-WhatIf</span></span>
<span data-ttu-id="54cee-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54cee-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54cee-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54cee-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54cee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cee-146">CommonParameters</span></span>
<span data-ttu-id="54cee-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cee-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cee-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cee-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54cee-149">INPUTS</span></span>

### <span data-ttu-id="54cee-150">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="54cee-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="54cee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="54cee-151">System.String</span></span>

## <span data-ttu-id="54cee-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54cee-152">OUTPUTS</span></span>

### <span data-ttu-id="54cee-153">Microsoft. Azure. commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="54cee-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="54cee-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54cee-154">NOTES</span></span>

## <span data-ttu-id="54cee-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54cee-155">RELATED LINKS</span></span>
