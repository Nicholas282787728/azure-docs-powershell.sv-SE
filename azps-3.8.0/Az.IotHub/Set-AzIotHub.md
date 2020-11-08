---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089143"
---
# <span data-ttu-id="81cb9-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="81cb9-101">Set-AzIotHub</span></span>

## <span data-ttu-id="81cb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="81cb9-103">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="81cb9-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="81cb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81cb9-104">SYNTAX</span></span>

### <span data-ttu-id="81cb9-105">UpdateSku (standard)</span><span class="sxs-lookup"><span data-stu-id="81cb9-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb9-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="81cb9-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cb9-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81cb9-112">DESCRIPTION</span></span>
<span data-ttu-id="81cb9-113">Uppdaterar egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="81cb9-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="81cb9-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81cb9-114">EXAMPLES</span></span>

### <span data-ttu-id="81cb9-115">Exempel 1 uppdatera SKU</span><span class="sxs-lookup"><span data-stu-id="81cb9-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="81cb9-116">Uppdatera SKU: er till S1 och enheter till 5 för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="81cb9-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="81cb9-117">Exempel 2 uppdatera egenskaperna för eventhub</span><span class="sxs-lookup"><span data-stu-id="81cb9-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="81cb9-118">Uppdatera Retentions tiden för telemetri i dagar till 4 för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="81cb9-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="81cb9-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81cb9-119">PARAMETERS</span></span>

### <span data-ttu-id="81cb9-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="81cb9-120">-CloudToDevice</span></span>
<span data-ttu-id="81cb9-121">Egenskaperna för den molnbaserade kommando kön.</span><span class="sxs-lookup"><span data-stu-id="81cb9-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="81cb9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cb9-122">-DefaultProfile</span></span>
<span data-ttu-id="81cb9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="81cb9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81cb9-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="81cb9-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="81cb9-125">Flagga som anger om aviseringar ska aktive ras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="81cb9-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="81cb9-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="81cb9-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="81cb9-127">Lagrings tid i dagar.</span><span class="sxs-lookup"><span data-stu-id="81cb9-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="81cb9-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="81cb9-128">-FallbackRoute</span></span>
<span data-ttu-id="81cb9-129">Reserv väg för routning</span><span class="sxs-lookup"><span data-stu-id="81cb9-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="81cb9-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="81cb9-130">-FileUploadContainerName</span></span>
<span data-ttu-id="81cb9-131">Namnet på den behållare där filerna ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="81cb9-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="81cb9-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="81cb9-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="81cb9-133">Maximalt antal leveranser för meddelanden om fil överföring.</span><span class="sxs-lookup"><span data-stu-id="81cb9-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="81cb9-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="81cb9-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="81cb9-135">TTL-värde för meddelanden i meddelande kön för fil överföring.</span><span class="sxs-lookup"><span data-stu-id="81cb9-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="81cb9-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="81cb9-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="81cb9-137">Dags att leva för för den SAS URI som genereras för fil uppladdning.</span><span class="sxs-lookup"><span data-stu-id="81cb9-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="81cb9-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="81cb9-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="81cb9-139">Lagrings anslutnings sträng som filer laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="81cb9-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="81cb9-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="81cb9-140">-Name</span></span>
<span data-ttu-id="81cb9-141">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="81cb9-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="81cb9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cb9-142">-ResourceGroupName</span></span>
<span data-ttu-id="81cb9-143">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="81cb9-143">Resource Group Name</span></span>

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

### <span data-ttu-id="81cb9-144">-Vägar</span><span class="sxs-lookup"><span data-stu-id="81cb9-144">-Routes</span></span>
<span data-ttu-id="81cb9-145">Vägar som ska läggas till för routning</span><span class="sxs-lookup"><span data-stu-id="81cb9-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="81cb9-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="81cb9-146">-RoutingProperties</span></span>
<span data-ttu-id="81cb9-147">Dirigerings egenskaper för meddelanden till externa slut punkter</span><span class="sxs-lookup"><span data-stu-id="81cb9-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="81cb9-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="81cb9-148">-SkuName</span></span>
<span data-ttu-id="81cb9-149">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="81cb9-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="81cb9-150">-Enheter</span><span class="sxs-lookup"><span data-stu-id="81cb9-150">-Units</span></span>
<span data-ttu-id="81cb9-151">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="81cb9-151">Number of Units</span></span>

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

### <span data-ttu-id="81cb9-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81cb9-152">-Confirm</span></span>
<span data-ttu-id="81cb9-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81cb9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cb9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cb9-154">-WhatIf</span></span>
<span data-ttu-id="81cb9-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81cb9-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cb9-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81cb9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81cb9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cb9-157">CommonParameters</span></span>
<span data-ttu-id="81cb9-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cb9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cb9-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cb9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cb9-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81cb9-160">INPUTS</span></span>

### <span data-ttu-id="81cb9-161">System. String</span><span class="sxs-lookup"><span data-stu-id="81cb9-161">System.String</span></span>

## <span data-ttu-id="81cb9-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81cb9-162">OUTPUTS</span></span>

### <span data-ttu-id="81cb9-163">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="81cb9-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="81cb9-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81cb9-164">NOTES</span></span>

## <span data-ttu-id="81cb9-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81cb9-165">RELATED LINKS</span></span>
