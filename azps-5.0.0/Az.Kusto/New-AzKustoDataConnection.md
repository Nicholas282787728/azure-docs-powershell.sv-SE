---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272223"
---
# <span data-ttu-id="cc75b-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="cc75b-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="cc75b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc75b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc75b-103">Skapar eller uppdaterar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="cc75b-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="cc75b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc75b-104">SYNTAX</span></span>

### <span data-ttu-id="cc75b-105">CreateExpandedEventHub (standard)</span><span class="sxs-lookup"><span data-stu-id="cc75b-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cc75b-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="cc75b-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc75b-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="cc75b-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cc75b-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="cc75b-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc75b-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="cc75b-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc75b-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc75b-110">DESCRIPTION</span></span>
<span data-ttu-id="cc75b-111">Skapar eller uppdaterar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="cc75b-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="cc75b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc75b-112">EXAMPLES</span></span>

### <span data-ttu-id="cc75b-113">Exempel 1: skapa en ny EventHub-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="cc75b-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="cc75b-114">Med kommandot ovan skapas en ny EventHub-dataanslutning med namnet "myeventhubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="cc75b-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="cc75b-115">Exempel 2: skapa en ny EventGrid-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="cc75b-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="cc75b-116">Med kommandot ovan skapas en ny EventGrid-dataanslutning med namnet "myeventgriddc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="cc75b-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="cc75b-117">Exempel 3: skapa en ny IotHub-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="cc75b-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="cc75b-118">Med kommandot ovan skapas en ny IotHub-dataanslutning med namnet "myiothubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="cc75b-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="cc75b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc75b-119">PARAMETERS</span></span>

### <span data-ttu-id="cc75b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc75b-120">-AsJob</span></span>
<span data-ttu-id="cc75b-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cc75b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="cc75b-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="cc75b-122">-BlobStorageEventType</span></span>
<span data-ttu-id="cc75b-123">Namnet på händelse typen för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="cc75b-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-124">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="cc75b-124">-ClusterName</span></span>
<span data-ttu-id="cc75b-125">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cc75b-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cc75b-126">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="cc75b-126">-Compression</span></span>
<span data-ttu-id="cc75b-127">Komprimerings typen Event Hub-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="cc75b-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cc75b-128">-ConsumerGroup</span></span>
<span data-ttu-id="cc75b-129">Gruppen Event/IoT Hub konsument.</span><span class="sxs-lookup"><span data-stu-id="cc75b-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="cc75b-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc75b-130">-DatabaseName</span></span>
<span data-ttu-id="cc75b-131">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cc75b-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cc75b-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="cc75b-132">-DataFormat</span></span>
<span data-ttu-id="cc75b-133">Meddelandets data format.</span><span class="sxs-lookup"><span data-stu-id="cc75b-133">The data format of the message.</span></span>
<span data-ttu-id="cc75b-134">Alternativt kan data formatet läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="cc75b-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc75b-135">-DefaultProfile</span></span>
<span data-ttu-id="cc75b-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc75b-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc75b-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="cc75b-137">-EventHubResourceId</span></span>
<span data-ttu-id="cc75b-138">Resurs-ID för händelsehubben som ska användas för att skapa en data anslutning/händelse rutnät är konfigurerat för att skicka händelser.</span><span class="sxs-lookup"><span data-stu-id="cc75b-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="cc75b-139">-EventSystemProperty</span></span>
<span data-ttu-id="cc75b-140">System egenskaper för hubben Event/IoT.</span><span class="sxs-lookup"><span data-stu-id="cc75b-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="cc75b-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="cc75b-142">Om värdet är true, betyder det att intag ska ignorera den första posten i alla filer.</span><span class="sxs-lookup"><span data-stu-id="cc75b-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="cc75b-143">-IotHubResourceId</span></span>
<span data-ttu-id="cc75b-144">ID för IoT Hub som används för att skapa en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="cc75b-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-145">-Sort</span><span class="sxs-lookup"><span data-stu-id="cc75b-145">-Kind</span></span>
<span data-ttu-id="cc75b-146">Typ av slut punkt för data anslutningen</span><span class="sxs-lookup"><span data-stu-id="cc75b-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-147">-Plats</span><span class="sxs-lookup"><span data-stu-id="cc75b-147">-Location</span></span>
<span data-ttu-id="cc75b-148">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="cc75b-148">Resource location.</span></span>

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

### <span data-ttu-id="cc75b-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="cc75b-149">-MappingRuleName</span></span>
<span data-ttu-id="cc75b-150">Kart regeln som ska användas för att överföra data.</span><span class="sxs-lookup"><span data-stu-id="cc75b-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="cc75b-151">Alternativt kan mappnings informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="cc75b-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="cc75b-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc75b-152">-Name</span></span>
<span data-ttu-id="cc75b-153">Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="cc75b-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-154">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cc75b-154">-NoWait</span></span>
<span data-ttu-id="cc75b-155">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cc75b-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc75b-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc75b-156">-ResourceGroupName</span></span>
<span data-ttu-id="cc75b-157">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cc75b-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cc75b-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="cc75b-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="cc75b-159">Namnet på delnings princip.</span><span class="sxs-lookup"><span data-stu-id="cc75b-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cc75b-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="cc75b-161">Resurs-ID för lagrings kontot där data finns.</span><span class="sxs-lookup"><span data-stu-id="cc75b-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc75b-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc75b-162">-SubscriptionId</span></span>
<span data-ttu-id="cc75b-163">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cc75b-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc75b-164">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cc75b-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cc75b-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="cc75b-165">-TableName</span></span>
<span data-ttu-id="cc75b-166">Tabellen där uppgifterna ska förtäras.</span><span class="sxs-lookup"><span data-stu-id="cc75b-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="cc75b-167">Eventuellt kan tabell informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="cc75b-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="cc75b-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc75b-168">-Confirm</span></span>
<span data-ttu-id="cc75b-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc75b-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc75b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc75b-170">-WhatIf</span></span>
<span data-ttu-id="cc75b-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc75b-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc75b-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc75b-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc75b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc75b-173">CommonParameters</span></span>
<span data-ttu-id="cc75b-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc75b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc75b-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc75b-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc75b-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc75b-176">INPUTS</span></span>

## <span data-ttu-id="cc75b-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc75b-177">OUTPUTS</span></span>

### <span data-ttu-id="cc75b-178">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="cc75b-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="cc75b-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc75b-179">NOTES</span></span>

<span data-ttu-id="cc75b-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc75b-180">ALIASES</span></span>

## <span data-ttu-id="cc75b-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc75b-181">RELATED LINKS</span></span>

