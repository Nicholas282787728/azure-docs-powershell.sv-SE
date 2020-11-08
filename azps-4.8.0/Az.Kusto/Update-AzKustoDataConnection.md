---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262219"
---
# <span data-ttu-id="8d27e-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="8d27e-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="8d27e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d27e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d27e-103">Uppdaterar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="8d27e-103">Updates a data connection.</span></span>

## <span data-ttu-id="8d27e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d27e-104">SYNTAX</span></span>

### <span data-ttu-id="8d27e-105">UpdateExpandedEventHub (standard)</span><span class="sxs-lookup"><span data-stu-id="8d27e-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d27e-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8d27e-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d27e-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="8d27e-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d27e-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8d27e-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d27e-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="8d27e-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d27e-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="8d27e-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d27e-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d27e-111">DESCRIPTION</span></span>
<span data-ttu-id="8d27e-112">Uppdaterar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="8d27e-112">Updates a data connection.</span></span>

## <span data-ttu-id="8d27e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d27e-113">EXAMPLES</span></span>

### <span data-ttu-id="8d27e-114">Exempel 1: uppdatera en befintlig EventHub-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="8d27e-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-115">Kommandot ovan uppdaterar den befintliga EventHub-dataanslutningen med namnet "myeventhubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8d27e-116">Exempel 2: uppdatera en befintlig EventGrid-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="8d27e-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-117">Kommandot ovan uppdaterar den befintliga EventGrid-dataanslutningen med namnet "myeventgriddc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8d27e-118">Exempel 3: uppdatera en befintlig IotHub-dataanslutning</span><span class="sxs-lookup"><span data-stu-id="8d27e-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-119">Kommandot ovan uppdaterar den befintliga IotHub-dataanslutningen med namnet "myiothubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8d27e-120">Exempel 4: uppdatera en befintlig EventHub-dataanslutning via identitet</span><span class="sxs-lookup"><span data-stu-id="8d27e-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-121">Kommandot ovan uppdaterar den befintliga EventHub-dataanslutningen med namnet "myeventhubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8d27e-122">Exempel 5: uppdatera en befintlig EventGrid-dataanslutning via identitet</span><span class="sxs-lookup"><span data-stu-id="8d27e-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-123">Kommandot ovan uppdaterar den befintliga EventGrid-dataanslutningen med namnet "myeventgriddc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8d27e-124">Exempel 6: uppdatera en befintlig IotHub-dataanslutning via identitet</span><span class="sxs-lookup"><span data-stu-id="8d27e-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8d27e-125">Kommandot ovan uppdaterar den befintliga IotHub-dataanslutningen med namnet "myiothubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8d27e-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="8d27e-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d27e-126">PARAMETERS</span></span>

### <span data-ttu-id="8d27e-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d27e-127">-AsJob</span></span>
<span data-ttu-id="8d27e-128">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="8d27e-128">Run the command as a job</span></span>

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

### <span data-ttu-id="8d27e-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="8d27e-129">-BlobStorageEventType</span></span>
<span data-ttu-id="8d27e-130">Namnet på händelse typen för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="8d27e-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="8d27e-131">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="8d27e-131">-ClusterName</span></span>
<span data-ttu-id="8d27e-132">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-133">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="8d27e-133">-Compression</span></span>
<span data-ttu-id="8d27e-134">Komprimerings typen Event Hub-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d27e-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8d27e-135">-ConsumerGroup</span></span>
<span data-ttu-id="8d27e-136">Gruppen Event/IoT Hub konsument.</span><span class="sxs-lookup"><span data-stu-id="8d27e-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="8d27e-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d27e-137">-DatabaseName</span></span>
<span data-ttu-id="8d27e-138">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="8d27e-139">-DataFormat</span></span>
<span data-ttu-id="8d27e-140">Meddelandets data format.</span><span class="sxs-lookup"><span data-stu-id="8d27e-140">The data format of the message.</span></span>
<span data-ttu-id="8d27e-141">Alternativt kan data formatet läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="8d27e-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="8d27e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d27e-142">-DefaultProfile</span></span>
<span data-ttu-id="8d27e-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d27e-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d27e-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8d27e-144">-EventHubResourceId</span></span>
<span data-ttu-id="8d27e-145">Resurs-ID för händelsehubben som ska användas för att skapa en data anslutning/händelse rutnät är konfigurerat för att skicka händelser.</span><span class="sxs-lookup"><span data-stu-id="8d27e-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="8d27e-146">-EventSystemProperty</span></span>
<span data-ttu-id="8d27e-147">System egenskaper för hubben Event/IoT.</span><span class="sxs-lookup"><span data-stu-id="8d27e-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="8d27e-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="8d27e-149">Om värdet är true, betyder det att intag ska ignorera den första posten i alla filer.</span><span class="sxs-lookup"><span data-stu-id="8d27e-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="8d27e-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d27e-150">-InputObject</span></span>
<span data-ttu-id="8d27e-151">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8d27e-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8d27e-152">-IotHubResourceId</span></span>
<span data-ttu-id="8d27e-153">ID för IoT Hub som används för att skapa en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="8d27e-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-154">-Sort</span><span class="sxs-lookup"><span data-stu-id="8d27e-154">-Kind</span></span>
<span data-ttu-id="8d27e-155">Typ av slut punkt för data anslutningen</span><span class="sxs-lookup"><span data-stu-id="8d27e-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="8d27e-156">-Plats</span><span class="sxs-lookup"><span data-stu-id="8d27e-156">-Location</span></span>
<span data-ttu-id="8d27e-157">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="8d27e-157">Resource location.</span></span>

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

### <span data-ttu-id="8d27e-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="8d27e-158">-MappingRuleName</span></span>
<span data-ttu-id="8d27e-159">Kart regeln som ska användas för att överföra data.</span><span class="sxs-lookup"><span data-stu-id="8d27e-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="8d27e-160">Alternativt kan mappnings informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="8d27e-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="8d27e-161">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d27e-161">-Name</span></span>
<span data-ttu-id="8d27e-162">Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8d27e-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-163">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8d27e-163">-NoWait</span></span>
<span data-ttu-id="8d27e-164">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="8d27e-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d27e-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d27e-165">-ResourceGroupName</span></span>
<span data-ttu-id="8d27e-166">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="8d27e-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="8d27e-168">Namnet på delnings princip.</span><span class="sxs-lookup"><span data-stu-id="8d27e-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8d27e-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="8d27e-170">Resurs-ID för lagrings kontot där data finns.</span><span class="sxs-lookup"><span data-stu-id="8d27e-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d27e-171">-SubscriptionId</span></span>
<span data-ttu-id="8d27e-172">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d27e-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d27e-173">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8d27e-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d27e-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="8d27e-174">-TableName</span></span>
<span data-ttu-id="8d27e-175">Tabellen där uppgifterna ska förtäras.</span><span class="sxs-lookup"><span data-stu-id="8d27e-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="8d27e-176">Eventuellt kan tabell informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="8d27e-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="8d27e-177">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d27e-177">-Confirm</span></span>
<span data-ttu-id="8d27e-178">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d27e-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d27e-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d27e-179">-WhatIf</span></span>
<span data-ttu-id="8d27e-180">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d27e-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d27e-181">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d27e-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d27e-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d27e-182">CommonParameters</span></span>
<span data-ttu-id="8d27e-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d27e-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d27e-184">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d27e-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d27e-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d27e-185">INPUTS</span></span>

### <span data-ttu-id="8d27e-186">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8d27e-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8d27e-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d27e-187">OUTPUTS</span></span>

### <span data-ttu-id="8d27e-188">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="8d27e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="8d27e-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d27e-189">NOTES</span></span>

<span data-ttu-id="8d27e-190">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8d27e-190">ALIASES</span></span>

<span data-ttu-id="8d27e-191">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8d27e-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d27e-192">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8d27e-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d27e-193">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d27e-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d27e-194">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8d27e-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d27e-195">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8d27e-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8d27e-196">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8d27e-197">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8d27e-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8d27e-198">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8d27e-199">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8d27e-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d27e-200">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="8d27e-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8d27e-201">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8d27e-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8d27e-202">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d27e-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8d27e-203">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d27e-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d27e-204">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8d27e-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8d27e-205">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d27e-205">RELATED LINKS</span></span>

