---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758235"
---
# <span data-ttu-id="adbac-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="adbac-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="adbac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adbac-102">SYNOPSIS</span></span>
<span data-ttu-id="adbac-103">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="adbac-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adbac-104">SYNTAX</span></span>

### <span data-ttu-id="adbac-105">UpdateSku (standard)</span><span class="sxs-lookup"><span data-stu-id="adbac-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbac-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="adbac-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbac-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adbac-113">DESCRIPTION</span></span>
<span data-ttu-id="adbac-114">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="adbac-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="adbac-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adbac-115">EXAMPLES</span></span>

### <span data-ttu-id="adbac-116">Exempel 1 uppdatera SKU</span><span class="sxs-lookup"><span data-stu-id="adbac-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="adbac-117">Uppdatera SKU: er till S1 och enheter till 5 för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="adbac-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="adbac-118">Exempel 2 uppdatera egenskaperna för eventhub</span><span class="sxs-lookup"><span data-stu-id="adbac-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="adbac-119">Uppdatera Retentions tiden i dagar till 4 för både telemetri och operationsmonitoringevents händelser för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="adbac-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="adbac-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adbac-120">PARAMETERS</span></span>

### <span data-ttu-id="adbac-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="adbac-121">-CloudToDevice</span></span>
<span data-ttu-id="adbac-122">Egenskaperna för den molnbaserade kommando kön.</span><span class="sxs-lookup"><span data-stu-id="adbac-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbac-123">-DefaultProfile</span></span>
<span data-ttu-id="adbac-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="adbac-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="adbac-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="adbac-126">Flagga som anger om aviseringar ska aktive ras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="adbac-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="adbac-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="adbac-128">Lagrings tid i dagar.</span><span class="sxs-lookup"><span data-stu-id="adbac-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="adbac-129">-FallbackRoute</span></span>
<span data-ttu-id="adbac-130">Reserv väg för routning</span><span class="sxs-lookup"><span data-stu-id="adbac-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="adbac-131">-FileUploadContainerName</span></span>
<span data-ttu-id="adbac-132">Namnet på den behållare där filerna ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="adbac-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="adbac-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="adbac-134">Maximalt antal leveranser för meddelanden om fil överföring.</span><span class="sxs-lookup"><span data-stu-id="adbac-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="adbac-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="adbac-136">TTL-värde för meddelanden i meddelande kön för fil överföring.</span><span class="sxs-lookup"><span data-stu-id="adbac-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="adbac-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="adbac-138">Dags att leva för för den SAS URI som genereras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="adbac-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="adbac-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="adbac-140">Lagrings anslutnings sträng som filer laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="adbac-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="adbac-141">-Name</span></span>
<span data-ttu-id="adbac-142">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="adbac-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="adbac-144">Egenskaper relaterade till operationer.</span><span class="sxs-lookup"><span data-stu-id="adbac-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbac-145">-ResourceGroupName</span></span>
<span data-ttu-id="adbac-146">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="adbac-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-147">-Vägar</span><span class="sxs-lookup"><span data-stu-id="adbac-147">-Routes</span></span>
<span data-ttu-id="adbac-148">Vägar som ska läggas till för routning</span><span class="sxs-lookup"><span data-stu-id="adbac-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="adbac-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-149">-RoutingProperties</span></span>
<span data-ttu-id="adbac-150">Dirigerings egenskaper för meddelanden till externa slut punkter</span><span class="sxs-lookup"><span data-stu-id="adbac-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="adbac-151">-SkuName</span></span>
<span data-ttu-id="adbac-152">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="adbac-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-153">-Enheter</span><span class="sxs-lookup"><span data-stu-id="adbac-153">-Units</span></span>
<span data-ttu-id="adbac-154">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="adbac-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adbac-155">-Confirm</span></span>
<span data-ttu-id="adbac-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adbac-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbac-157">-WhatIf</span></span>
<span data-ttu-id="adbac-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adbac-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbac-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adbac-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbac-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbac-160">CommonParameters</span></span>
<span data-ttu-id="adbac-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbac-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbac-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbac-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbac-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adbac-163">INPUTS</span></span>

### <span data-ttu-id="adbac-164">System. String</span><span class="sxs-lookup"><span data-stu-id="adbac-164">System.String</span></span>
<span data-ttu-id="adbac-165">Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="adbac-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="adbac-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adbac-166">OUTPUTS</span></span>

### <span data-ttu-id="adbac-167">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="adbac-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="adbac-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adbac-168">NOTES</span></span>

## <span data-ttu-id="adbac-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adbac-169">RELATED LINKS</span></span>

