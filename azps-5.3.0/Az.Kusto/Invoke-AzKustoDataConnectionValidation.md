---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: fa75072cdb29d7aedc7a78ba4e20950b904f1c7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525962"
---
# <span data-ttu-id="c7dbb-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="c7dbb-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="c7dbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dbb-103">Kontrollerar att data anslutnings parametrarna är giltiga.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="c7dbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7dbb-104">SYNTAX</span></span>

### <span data-ttu-id="c7dbb-105">DataExpandedEventHub (standard)</span><span class="sxs-lookup"><span data-stu-id="c7dbb-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c7dbb-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="c7dbb-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c7dbb-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="c7dbb-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="c7dbb-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c7dbb-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7dbb-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c7dbb-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7dbb-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7dbb-113">DESCRIPTION</span></span>
<span data-ttu-id="c7dbb-114">Kontrollerar att data anslutnings parametrarna är giltiga.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="c7dbb-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7dbb-115">EXAMPLES</span></span>

### <span data-ttu-id="c7dbb-116">Exempel 1: validera parametrarna för data anslutning för EventHub</span><span class="sxs-lookup"><span data-stu-id="c7dbb-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-117">Kommandot ovan verifierar EventHub Data Connection med namnet "myeventhubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c7dbb-118">Exempel 2: verifiera EventGrid</span><span class="sxs-lookup"><span data-stu-id="c7dbb-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-119">Kommandot ovan verifierar EventGrid data anslutning med namnet "myeventgriddc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c7dbb-120">Exempel 3: verifiera IotHub</span><span class="sxs-lookup"><span data-stu-id="c7dbb-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-121">Kommandot ovan verifierar IotHub data anslutning med namnet "myiothubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c7dbb-122">Exempel 4: validera parametrar för en EventHub-dataanslutning via identitet</span><span class="sxs-lookup"><span data-stu-id="c7dbb-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-123">Kommandot ovan verifierar EventHub Data Connection med namnet "myeventhubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c7dbb-124">Exempel 5: validera EventGrid Data Connection-parametrar via identitet</span><span class="sxs-lookup"><span data-stu-id="c7dbb-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-125">Kommandot ovan verifierar EventGrid data anslutning med namnet "myeventgriddc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c7dbb-126">Exempel 6: validera IotHub Data Connection-parametrar via identitet</span><span class="sxs-lookup"><span data-stu-id="c7dbb-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="c7dbb-127">Kommandot ovan verifierar IotHub data anslutning med namnet "myiothubdc" för databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c7dbb-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c7dbb-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7dbb-128">PARAMETERS</span></span>

### <span data-ttu-id="c7dbb-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="c7dbb-129">-BlobStorageEventType</span></span>
<span data-ttu-id="c7dbb-130">Namnet på händelse typen för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="c7dbb-131">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="c7dbb-131">-ClusterName</span></span>
<span data-ttu-id="c7dbb-132">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-133">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="c7dbb-133">-Compression</span></span>
<span data-ttu-id="c7dbb-134">Komprimerings typen Event Hub-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c7dbb-135">-ConsumerGroup</span></span>
<span data-ttu-id="c7dbb-136">Gruppen Event/IoT Hub konsument.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="c7dbb-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-137">-DatabaseName</span></span>
<span data-ttu-id="c7dbb-138">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-139">-DataConnectionName</span></span>
<span data-ttu-id="c7dbb-140">Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="c7dbb-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="c7dbb-141">-DataFormat</span></span>
<span data-ttu-id="c7dbb-142">Meddelandets data format.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-142">The data format of the message.</span></span>
<span data-ttu-id="c7dbb-143">Alternativt kan data formatet läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="c7dbb-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7dbb-144">-DefaultProfile</span></span>
<span data-ttu-id="c7dbb-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7dbb-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c7dbb-146">-EventHubResourceId</span></span>
<span data-ttu-id="c7dbb-147">Resurs-ID för händelsehubben som ska användas för att skapa en data anslutning/händelse rutnät är konfigurerat för att skicka händelser.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="c7dbb-148">-EventSystemProperty</span></span>
<span data-ttu-id="c7dbb-149">System egenskaper för hubben Event/IoT.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="c7dbb-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="c7dbb-151">Om värdet är true, betyder det att intag ska ignorera den första posten i alla filer.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="c7dbb-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7dbb-152">-InputObject</span></span>
<span data-ttu-id="c7dbb-153">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c7dbb-154">-IotHubResourceId</span></span>
<span data-ttu-id="c7dbb-155">ID för IoT Hub som används för att skapa en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-156">-Sort</span><span class="sxs-lookup"><span data-stu-id="c7dbb-156">-Kind</span></span>
<span data-ttu-id="c7dbb-157">Typ av slut punkt för data anslutningen</span><span class="sxs-lookup"><span data-stu-id="c7dbb-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="c7dbb-158">-Plats</span><span class="sxs-lookup"><span data-stu-id="c7dbb-158">-Location</span></span>
<span data-ttu-id="c7dbb-159">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-159">Resource location.</span></span>

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

### <span data-ttu-id="c7dbb-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-160">-MappingRuleName</span></span>
<span data-ttu-id="c7dbb-161">Kart regeln som ska användas för att överföra data.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="c7dbb-162">Alternativt kan mappnings informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="c7dbb-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-163">-ResourceGroupName</span></span>
<span data-ttu-id="c7dbb-164">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="c7dbb-166">Namnet på delnings princip.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c7dbb-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="c7dbb-168">Resurs-ID för lagrings kontot där data finns.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7dbb-169">-SubscriptionId</span></span>
<span data-ttu-id="c7dbb-170">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c7dbb-171">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7dbb-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="c7dbb-172">-TableName</span></span>
<span data-ttu-id="c7dbb-173">Tabellen där uppgifterna ska förtäras.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="c7dbb-174">Eventuellt kan tabell informationen läggas till i varje meddelande.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="c7dbb-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7dbb-175">-Confirm</span></span>
<span data-ttu-id="c7dbb-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7dbb-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7dbb-177">-WhatIf</span></span>
<span data-ttu-id="c7dbb-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7dbb-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7dbb-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dbb-180">CommonParameters</span></span>
<span data-ttu-id="c7dbb-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dbb-182">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7dbb-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dbb-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7dbb-183">INPUTS</span></span>

### <span data-ttu-id="c7dbb-184">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c7dbb-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c7dbb-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7dbb-185">OUTPUTS</span></span>

### <span data-ttu-id="c7dbb-186">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="c7dbb-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="c7dbb-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7dbb-187">NOTES</span></span>

<span data-ttu-id="c7dbb-188">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c7dbb-188">ALIASES</span></span>

<span data-ttu-id="c7dbb-189">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c7dbb-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7dbb-190">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7dbb-191">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7dbb-192">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c7dbb-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7dbb-193">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c7dbb-194">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c7dbb-195">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c7dbb-196">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c7dbb-197">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c7dbb-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7dbb-198">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c7dbb-199">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c7dbb-200">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c7dbb-201">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c7dbb-202">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c7dbb-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c7dbb-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7dbb-203">RELATED LINKS</span></span>

