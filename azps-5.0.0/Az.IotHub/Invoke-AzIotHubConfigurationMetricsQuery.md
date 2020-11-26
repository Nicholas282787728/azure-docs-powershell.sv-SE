---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273498"
---
# <span data-ttu-id="d2807-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="d2807-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="d2807-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2807-102">SYNOPSIS</span></span>
<span data-ttu-id="d2807-103">Kör en IoT-fråga om enhets konfigurations mått.</span><span class="sxs-lookup"><span data-stu-id="d2807-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="d2807-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2807-104">SYNTAX</span></span>

### <span data-ttu-id="d2807-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d2807-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2807-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2807-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2807-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d2807-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2807-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2807-108">DESCRIPTION</span></span>
<span data-ttu-id="d2807-109">Utvärdera en anpassad mål-eller system mått definition i en IoT-enhets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2807-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="d2807-110">Det finns fördefinierade system värden som beräknas av IoT Hub och inte kan anpassas.</span><span class="sxs-lookup"><span data-stu-id="d2807-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="d2807-111">"Riktat" anger antalet enheter som matchar mål villkoret.</span><span class="sxs-lookup"><span data-stu-id="d2807-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="d2807-112">"Använt" angivet antal enheter som har ändrats med konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d2807-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="d2807-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2807-113">EXAMPLES</span></span>

### <span data-ttu-id="d2807-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d2807-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="d2807-115">Utvärdera det anpassade måttet ' warningLimit '.</span><span class="sxs-lookup"><span data-stu-id="d2807-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="d2807-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d2807-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="d2807-117">Utvärdera systemet som "tillämpat"-mått.</span><span class="sxs-lookup"><span data-stu-id="d2807-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="d2807-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2807-118">PARAMETERS</span></span>

### <span data-ttu-id="d2807-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2807-119">-DefaultProfile</span></span>
<span data-ttu-id="d2807-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2807-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2807-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2807-121">-InputObject</span></span>
<span data-ttu-id="d2807-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="d2807-122">IotHub object</span></span>

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

### <span data-ttu-id="d2807-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d2807-123">-IotHubName</span></span>
<span data-ttu-id="d2807-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="d2807-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d2807-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d2807-125">-MetricName</span></span>
<span data-ttu-id="d2807-126">Mål mått för utvärdering.</span><span class="sxs-lookup"><span data-stu-id="d2807-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="d2807-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="d2807-127">-MetricType</span></span>
<span data-ttu-id="d2807-128">Anger vilken mått samling som ska användas för att slå upp ett mått.</span><span class="sxs-lookup"><span data-stu-id="d2807-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2807-129">-Name</span></span>
<span data-ttu-id="d2807-130">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d2807-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="d2807-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2807-131">-ResourceGroupName</span></span>
<span data-ttu-id="d2807-132">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d2807-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d2807-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2807-133">-ResourceId</span></span>
<span data-ttu-id="d2807-134">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="d2807-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d2807-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2807-135">-Confirm</span></span>
<span data-ttu-id="d2807-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2807-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2807-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2807-137">-WhatIf</span></span>
<span data-ttu-id="d2807-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2807-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2807-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2807-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2807-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2807-140">CommonParameters</span></span>
<span data-ttu-id="d2807-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2807-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2807-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2807-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2807-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2807-143">INPUTS</span></span>

### <span data-ttu-id="d2807-144">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d2807-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d2807-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d2807-145">System.String</span></span>

## <span data-ttu-id="d2807-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2807-146">OUTPUTS</span></span>

### <span data-ttu-id="d2807-147">Microsoft. Azure. commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="d2807-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="d2807-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2807-148">NOTES</span></span>

## <span data-ttu-id="d2807-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2807-149">RELATED LINKS</span></span>