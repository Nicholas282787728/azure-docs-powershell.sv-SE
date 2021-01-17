---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402459"
---
# <span data-ttu-id="96d92-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d92-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="96d92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96d92-102">SYNOPSIS</span></span>
<span data-ttu-id="96d92-103">Skapa eller uppdatera DigitalTwinsInstance-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="96d92-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="96d92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96d92-104">SYNTAX</span></span>

### <span data-ttu-id="96d92-105">EventHub (standard)</span><span class="sxs-lookup"><span data-stu-id="96d92-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96d92-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="96d92-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96d92-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96d92-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96d92-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96d92-108">DESCRIPTION</span></span>
<span data-ttu-id="96d92-109">Skapa eller uppdatera DigitalTwinsInstance-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="96d92-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="96d92-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96d92-110">EXAMPLES</span></span>

### <span data-ttu-id="96d92-111">Exempel 1: skapa en AzDigitalTwinsEndpoint för Eventhub</span><span class="sxs-lookup"><span data-stu-id="96d92-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96d92-112">Skapa en AzDigitalTwinsEndpoint för Eventhub by connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="96d92-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="96d92-113">Exempel 2: skapa en AzDigitalTwinsEndpoint för EventGrid</span><span class="sxs-lookup"><span data-stu-id="96d92-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96d92-114">Skapa en AzDigitalTwinsEndpoint för Eventhub by TopicEndpoint och accessKey1</span><span class="sxs-lookup"><span data-stu-id="96d92-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="96d92-115">Exempel 3: skapa en AzDigitalTwinsEndpoint för ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96d92-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96d92-116">Skapa en AzDigitalTwinsEndpoint för ServicBus efter PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="96d92-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="96d92-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96d92-117">PARAMETERS</span></span>

### <span data-ttu-id="96d92-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="96d92-118">-AccessKey1</span></span>
<span data-ttu-id="96d92-119">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96d92-120">-AsJob</span></span>
<span data-ttu-id="96d92-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="96d92-121">Run the command as a job</span></span>

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

### <span data-ttu-id="96d92-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="96d92-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="96d92-123">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="96d92-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="96d92-125">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="96d92-126">-DeadLetterSecret</span></span>
<span data-ttu-id="96d92-127">Lagring hemligt för obeställbara meddelanden.</span><span class="sxs-lookup"><span data-stu-id="96d92-127">Dead letter storage secret.</span></span>
<span data-ttu-id="96d92-128">Kommer att vara Obfuscated under läsning.</span><span class="sxs-lookup"><span data-stu-id="96d92-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="96d92-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d92-129">-DefaultProfile</span></span>
<span data-ttu-id="96d92-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96d92-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="96d92-131">-EndpointDescription</span></span>
<span data-ttu-id="96d92-132">Slut punkts resursen DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96d92-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="96d92-133">För att konstruera kan du läsa avsnittet anteckningar för ENDPOINTDESCRIPTION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="96d92-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="96d92-134">-EndpointName</span></span>
<span data-ttu-id="96d92-135">Namn på slut punkts resurs.</span><span class="sxs-lookup"><span data-stu-id="96d92-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="96d92-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="96d92-136">-EndpointType</span></span>
<span data-ttu-id="96d92-137">Typen av avsluts änd punkt för digital</span><span class="sxs-lookup"><span data-stu-id="96d92-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="96d92-138">-NoWait</span></span>
<span data-ttu-id="96d92-139">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="96d92-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96d92-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="96d92-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="96d92-141">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d92-142">-ResourceGroupName</span></span>
<span data-ttu-id="96d92-143">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96d92-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="96d92-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="96d92-144">-ResourceName</span></span>
<span data-ttu-id="96d92-145">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96d92-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="96d92-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96d92-146">-SubscriptionId</span></span>
<span data-ttu-id="96d92-147">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d92-148">-TopicEndpoint</span></span>
<span data-ttu-id="96d92-149">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="96d92-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d92-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96d92-150">-Confirm</span></span>
<span data-ttu-id="96d92-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96d92-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d92-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d92-152">-WhatIf</span></span>
<span data-ttu-id="96d92-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96d92-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96d92-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96d92-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d92-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d92-155">CommonParameters</span></span>
<span data-ttu-id="96d92-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d92-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d92-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96d92-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d92-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96d92-158">INPUTS</span></span>

### <span data-ttu-id="96d92-159">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="96d92-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="96d92-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96d92-160">OUTPUTS</span></span>

### <span data-ttu-id="96d92-161">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="96d92-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="96d92-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96d92-162">NOTES</span></span>

<span data-ttu-id="96d92-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="96d92-163">ALIASES</span></span>

<span data-ttu-id="96d92-164">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="96d92-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96d92-165">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="96d92-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96d92-166">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96d92-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96d92-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : DigitalTwinsInstance-slutpunkt-resurs.</span><span class="sxs-lookup"><span data-stu-id="96d92-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="96d92-168">`EndpointType <EndpointType>`: Typen av avsluts änd punkt för digital</span><span class="sxs-lookup"><span data-stu-id="96d92-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="96d92-169">`[DeadLetterSecret <String>]`: Hemligt lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="96d92-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="96d92-170">Kommer att vara Obfuscated under läsning.</span><span class="sxs-lookup"><span data-stu-id="96d92-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="96d92-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96d92-171">RELATED LINKS</span></span>

