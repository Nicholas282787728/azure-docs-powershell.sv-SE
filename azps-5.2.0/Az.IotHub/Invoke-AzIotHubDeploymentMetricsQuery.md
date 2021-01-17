---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396896"
---
# <span data-ttu-id="5ce32-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="5ce32-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="5ce32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ce32-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce32-103">Kör en IoT Edge Deployment Metric-fråga.</span><span class="sxs-lookup"><span data-stu-id="5ce32-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="5ce32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ce32-104">SYNTAX</span></span>

### <span data-ttu-id="5ce32-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5ce32-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce32-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ce32-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce32-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ce32-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce32-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ce32-108">DESCRIPTION</span></span>
<span data-ttu-id="5ce32-109">Utvärdera en anpassad mål-eller system mått definition i en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="5ce32-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="5ce32-110">Det finns fördefinierade system värden som beräknas av IoT Hub och inte kan anpassas.</span><span class="sxs-lookup"><span data-stu-id="5ce32-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="5ce32-111">"Riktat" visar vilka IoT-enheter som matchar distributions villkoren.</span><span class="sxs-lookup"><span data-stu-id="5ce32-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="5ce32-112">"Använt" visar de riktade enheter för IoT som inte är riktade till en annan distribution av högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="5ce32-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="5ce32-113">"Rapporterar framgång" visar vilka IoT-enheter som har rapporterat att modulerna har distribuerats.</span><span class="sxs-lookup"><span data-stu-id="5ce32-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="5ce32-114">"Rapporterar fel" visar vilka IoT-enheter som har rapporterat att en eller flera moduler inte har distribuerats.</span><span class="sxs-lookup"><span data-stu-id="5ce32-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="5ce32-115">Om du vill undersöka felet kan du fjärrans luta till dessa enheter och Visa loggfilerna.</span><span class="sxs-lookup"><span data-stu-id="5ce32-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="5ce32-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ce32-116">EXAMPLES</span></span>

### <span data-ttu-id="5ce32-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ce32-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="5ce32-118">Utvärdera det anpassade måttet ' warningLimit '.</span><span class="sxs-lookup"><span data-stu-id="5ce32-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="5ce32-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5ce32-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="5ce32-120">Utvärdera om systemet rapporterar framgång.</span><span class="sxs-lookup"><span data-stu-id="5ce32-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="5ce32-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ce32-121">PARAMETERS</span></span>

### <span data-ttu-id="5ce32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce32-122">-DefaultProfile</span></span>
<span data-ttu-id="5ce32-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce32-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce32-124">-InputObject</span></span>
<span data-ttu-id="5ce32-125">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="5ce32-125">IotHub object</span></span>

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

### <span data-ttu-id="5ce32-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5ce32-126">-IotHubName</span></span>
<span data-ttu-id="5ce32-127">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5ce32-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5ce32-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="5ce32-128">-MetricName</span></span>
<span data-ttu-id="5ce32-129">Mål mått för utvärdering.</span><span class="sxs-lookup"><span data-stu-id="5ce32-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="5ce32-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="5ce32-130">-MetricType</span></span>
<span data-ttu-id="5ce32-131">Anger vilken mått samling som ska användas för att slå upp ett mått.</span><span class="sxs-lookup"><span data-stu-id="5ce32-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="5ce32-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ce32-132">-Name</span></span>
<span data-ttu-id="5ce32-133">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="5ce32-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="5ce32-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce32-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ce32-135">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5ce32-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5ce32-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce32-136">-ResourceId</span></span>
<span data-ttu-id="5ce32-137">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="5ce32-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5ce32-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ce32-138">-Confirm</span></span>
<span data-ttu-id="5ce32-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ce32-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce32-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce32-140">-WhatIf</span></span>
<span data-ttu-id="5ce32-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ce32-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce32-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ce32-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce32-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce32-143">CommonParameters</span></span>
<span data-ttu-id="5ce32-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce32-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce32-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce32-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce32-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ce32-146">INPUTS</span></span>

### <span data-ttu-id="5ce32-147">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5ce32-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5ce32-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce32-148">System.String</span></span>

## <span data-ttu-id="5ce32-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ce32-149">OUTPUTS</span></span>

### <span data-ttu-id="5ce32-150">Microsoft. Azure. commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="5ce32-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="5ce32-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ce32-151">NOTES</span></span>

## <span data-ttu-id="5ce32-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ce32-152">RELATED LINKS</span></span>
