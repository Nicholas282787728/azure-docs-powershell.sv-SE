---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259472"
---
# <span data-ttu-id="fcb89-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcb89-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="fcb89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcb89-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb89-103">Uppdatera mutable-fälten för konfigurations registreringen.</span><span class="sxs-lookup"><span data-stu-id="fcb89-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="fcb89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcb89-104">SYNTAX</span></span>

### <span data-ttu-id="fcb89-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fcb89-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fcb89-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fcb89-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb89-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcb89-108">DESCRIPTION</span></span>
<span data-ttu-id="fcb89-109">Uppdatera angivna egenskaper för en IoT-konfiguration för automatisk enhets hantering.</span><span class="sxs-lookup"><span data-stu-id="fcb89-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="fcb89-110">Obs! konfigurations innehåll ändras inte.</span><span class="sxs-lookup"><span data-stu-id="fcb89-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="fcb89-111">Konfigurations egenskaper som kan uppdateras är ' etiketter ', ' mått ', ' Priority ' och ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="fcb89-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="fcb89-112">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management information finns i.</span><span class="sxs-lookup"><span data-stu-id="fcb89-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="fcb89-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcb89-113">EXAMPLES</span></span>

### <span data-ttu-id="fcb89-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fcb89-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="fcb89-115">Ändra prioriteten för en enhets konfiguration och uppdatera dess mål villkor</span><span class="sxs-lookup"><span data-stu-id="fcb89-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="fcb89-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcb89-116">PARAMETERS</span></span>

### <span data-ttu-id="fcb89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb89-117">-DefaultProfile</span></span>
<span data-ttu-id="fcb89-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb89-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb89-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fcb89-119">-Force</span></span>
<span data-ttu-id="fcb89-120">Tillåter att konfigurations objekt byts ut även om det har uppdaterats sedan det hämtades förra gången.</span><span class="sxs-lookup"><span data-stu-id="fcb89-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="fcb89-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb89-121">-InputObject</span></span>
<span data-ttu-id="fcb89-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="fcb89-122">IotHub object</span></span>

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

### <span data-ttu-id="fcb89-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fcb89-123">-IotHubName</span></span>
<span data-ttu-id="fcb89-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="fcb89-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fcb89-125">-Etikett</span><span class="sxs-lookup"><span data-stu-id="fcb89-125">-Label</span></span>
<span data-ttu-id="fcb89-126">Kart karta som ska användas för mål konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fcb89-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="fcb89-127">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="fcb89-127">-Metric</span></span>
<span data-ttu-id="fcb89-128">Samling med frågor för konfigurations mått.</span><span class="sxs-lookup"><span data-stu-id="fcb89-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="fcb89-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcb89-129">-Name</span></span>
<span data-ttu-id="fcb89-130">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="fcb89-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="fcb89-131">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="fcb89-131">-Priority</span></span>
<span data-ttu-id="fcb89-132">Vikt för enhetens konfiguration om det rör sig om konkurrerande regler (högst vinner).</span><span class="sxs-lookup"><span data-stu-id="fcb89-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="fcb89-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb89-133">-ResourceGroupName</span></span>
<span data-ttu-id="fcb89-134">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fcb89-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fcb89-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcb89-135">-ResourceId</span></span>
<span data-ttu-id="fcb89-136">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="fcb89-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fcb89-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="fcb89-137">-TargetCondition</span></span>
<span data-ttu-id="fcb89-138">Mål villkor där en enhets konfiguration gäller.</span><span class="sxs-lookup"><span data-stu-id="fcb89-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="fcb89-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fcb89-139">-Confirm</span></span>
<span data-ttu-id="fcb89-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fcb89-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb89-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb89-141">-WhatIf</span></span>
<span data-ttu-id="fcb89-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fcb89-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb89-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fcb89-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb89-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb89-144">CommonParameters</span></span>
<span data-ttu-id="fcb89-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb89-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb89-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb89-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb89-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcb89-147">INPUTS</span></span>

### <span data-ttu-id="fcb89-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fcb89-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fcb89-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb89-149">System.String</span></span>

## <span data-ttu-id="fcb89-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcb89-150">OUTPUTS</span></span>

### <span data-ttu-id="fcb89-151">Microsoft. Azure. commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcb89-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="fcb89-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcb89-152">NOTES</span></span>

## <span data-ttu-id="fcb89-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcb89-153">RELATED LINKS</span></span>
