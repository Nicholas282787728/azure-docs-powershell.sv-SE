---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916405"
---
# <span data-ttu-id="01a1e-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="01a1e-101">Set-AzIotHub</span></span>

## <span data-ttu-id="01a1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="01a1e-103">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="01a1e-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="01a1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01a1e-104">SYNTAX</span></span>

### <span data-ttu-id="01a1e-105">UpdateSku (standard)</span><span class="sxs-lookup"><span data-stu-id="01a1e-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a1e-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="01a1e-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01a1e-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01a1e-113">DESCRIPTION</span></span>
<span data-ttu-id="01a1e-114">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="01a1e-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="01a1e-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01a1e-115">EXAMPLES</span></span>

### <span data-ttu-id="01a1e-116">Exempel 1 uppdatera SKU</span><span class="sxs-lookup"><span data-stu-id="01a1e-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="01a1e-117">Uppdatera SKU: er till S1 och enheter till 5 för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="01a1e-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="01a1e-118">Exempel 2 uppdatera egenskaperna för eventhub</span><span class="sxs-lookup"><span data-stu-id="01a1e-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="01a1e-119">Uppdatera Retentions tiden i dagar till 4 för både telemetri och operationsmonitoringevents händelser för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="01a1e-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="01a1e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01a1e-120">PARAMETERS</span></span>

### <span data-ttu-id="01a1e-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="01a1e-121">-CloudToDevice</span></span>
<span data-ttu-id="01a1e-122">Egenskaperna för den molnbaserade kommando kön.</span><span class="sxs-lookup"><span data-stu-id="01a1e-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a1e-123">-DefaultProfile</span></span>
<span data-ttu-id="01a1e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="01a1e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01a1e-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="01a1e-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="01a1e-126">Flagga som anger om aviseringar ska aktive ras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="01a1e-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="01a1e-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="01a1e-128">Lagrings tid i dagar.</span><span class="sxs-lookup"><span data-stu-id="01a1e-128">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="01a1e-129">-FallbackRoute</span></span>
<span data-ttu-id="01a1e-130">Reserv väg för routning</span><span class="sxs-lookup"><span data-stu-id="01a1e-130">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="01a1e-131">-FileUploadContainerName</span></span>
<span data-ttu-id="01a1e-132">Namnet på den behållare där filerna ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="01a1e-132">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="01a1e-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="01a1e-134">Maximalt antal leveranser för meddelanden om fil överföring.</span><span class="sxs-lookup"><span data-stu-id="01a1e-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="01a1e-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="01a1e-136">TTL-värde för meddelanden i meddelande kön för fil överföring.</span><span class="sxs-lookup"><span data-stu-id="01a1e-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="01a1e-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="01a1e-138">Dags att leva för för den SAS URI som genereras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="01a1e-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="01a1e-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="01a1e-140">Lagrings anslutnings sträng som filer laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="01a1e-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="01a1e-141">-Name</span></span>
<span data-ttu-id="01a1e-142">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="01a1e-142">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="01a1e-144">Egenskaper relaterade till operationer.</span><span class="sxs-lookup"><span data-stu-id="01a1e-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a1e-145">-ResourceGroupName</span></span>
<span data-ttu-id="01a1e-146">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="01a1e-146">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-147">-Vägar</span><span class="sxs-lookup"><span data-stu-id="01a1e-147">-Routes</span></span>
<span data-ttu-id="01a1e-148">Vägar som ska läggas till för routning</span><span class="sxs-lookup"><span data-stu-id="01a1e-148">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="01a1e-149">-RoutingProperties</span></span>
<span data-ttu-id="01a1e-150">Dirigerings egenskaper för meddelanden till externa slut punkter</span><span class="sxs-lookup"><span data-stu-id="01a1e-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="01a1e-151">-SkuName</span></span>
<span data-ttu-id="01a1e-152">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="01a1e-152">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-153">-Enheter</span><span class="sxs-lookup"><span data-stu-id="01a1e-153">-Units</span></span>
<span data-ttu-id="01a1e-154">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="01a1e-154">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01a1e-155">-Confirm</span></span>
<span data-ttu-id="01a1e-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01a1e-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a1e-157">-WhatIf</span></span>
<span data-ttu-id="01a1e-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01a1e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01a1e-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01a1e-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a1e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a1e-160">CommonParameters</span></span>
<span data-ttu-id="01a1e-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a1e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a1e-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a1e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a1e-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01a1e-163">INPUTS</span></span>

### <span data-ttu-id="01a1e-164">System. String</span><span class="sxs-lookup"><span data-stu-id="01a1e-164">System.String</span></span>

## <span data-ttu-id="01a1e-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01a1e-165">OUTPUTS</span></span>

### <span data-ttu-id="01a1e-166">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="01a1e-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="01a1e-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01a1e-167">NOTES</span></span>

## <span data-ttu-id="01a1e-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01a1e-168">RELATED LINKS</span></span>
