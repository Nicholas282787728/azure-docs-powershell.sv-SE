# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="45c25-101">Större ändringar för Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="45c25-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="45c25-102">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="45c25-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="45c25-103">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="45c25-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="45c25-104">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="45c25-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="45c25-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="45c25-105">Table of Contents</span></span>

- [<span data-ttu-id="45c25-106">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="45c25-107">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="45c25-108">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="45c25-109">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="45c25-110">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="45c25-111">Större ändringar i Sql-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="45c25-112">Större ändringar i Storage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="45c25-113">Större ändringar i Profile-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="45c25-114">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="45c25-115">Följande typer av utdata påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="45c25-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="45c25-116">PSVirtualMachine</span></span>
- <span data-ttu-id="45c25-117">Egenskaperna `DataDiskNames` och `NetworkInterfaceIDs` på den översta nivån av objektet `PSVirtualMachine` har tagits bort från utdatatypen.</span><span class="sxs-lookup"><span data-stu-id="45c25-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="45c25-118">De här egenskaperna har alltid varit tillgängliga i egenskaperna `StorageProfile` och `NetworkProfile` för objektet `PSVirtualMachine` och framöver är de endast tillgängliga där.</span><span class="sxs-lookup"><span data-stu-id="45c25-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="45c25-119">Den här ändringen påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="45c25-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="45c25-120">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="45c25-121">Följande cmdletar påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="45c25-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="45c25-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="45c25-123">Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="45c25-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="45c25-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="45c25-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="45c25-125">Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="45c25-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="45c25-126">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="45c25-127">Följande cmdletar påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="45c25-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="45c25-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="45c25-129">Den här cmdleten har gjorts inaktuell.</span><span class="sxs-lookup"><span data-stu-id="45c25-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="45c25-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c25-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="45c25-131">Utdata från den här cmdleten har ändrats från en lista med ett enda objekt till ett enda objekt. Det här objektet innehåller ID för begäran och statuskod.</span><span class="sxs-lookup"><span data-stu-id="45c25-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="45c25-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c25-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="45c25-133">Den här cmdleten har gjorts inaktuell.</span><span class="sxs-lookup"><span data-stu-id="45c25-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="45c25-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c25-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="45c25-135">Varje element i utdatainformationen (en lista över objekt) för den här cmdleten har jämnats ut. Istället för att returnera objekt med strukturen `{ Id, Location, Name, Tags, Properties }` returnerar den objekt med strukturen `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, som är alla attribut för en Azure-resurs samt alla attribut för en AlertRuleResource på den översta nivån.</span><span class="sxs-lookup"><span data-stu-id="45c25-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="45c25-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45c25-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="45c25-137">Fältet `AutoscaleSettingResourceName` är inaktuellt eftersom det alltid har samma värde som fältet `Name`.</span><span class="sxs-lookup"><span data-stu-id="45c25-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="45c25-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45c25-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="45c25-139">Utdata från den här cmdleten kommer att ändras från `Boolean` till objekt som innehåller `RequestId` och `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="45c25-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="45c25-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45c25-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="45c25-141">Utdata från den här cmdleten kommer att ändras från ett objekt som innehåller ID för begäran, statuskod och den uppdaterade eller nya resursen</span><span class="sxs-lookup"><span data-stu-id="45c25-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="45c25-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="45c25-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="45c25-143">Kommandot kommer att ändras till `Update-AzureRmDiagnsoticSettings`</span><span class="sxs-lookup"><span data-stu-id="45c25-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="45c25-144">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="45c25-145">Följande cmdletar påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="45c25-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="45c25-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="45c25-147">Parametern `EnableBgp` har ändrats för att ta en `boolean` i stället för en `string`</span><span class="sxs-lookup"><span data-stu-id="45c25-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="45c25-148">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="45c25-149">Följande cmdletar påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="45c25-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="45c25-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="45c25-151">Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="45c25-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="45c25-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="45c25-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="45c25-153">Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="45c25-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="45c25-154">Större ändringar i Sql-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="45c25-155">Följande cmdletar påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="45c25-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45c25-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="45c25-157">Parametern `Tag` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="45c25-158">Parametern `GracePeriodWithDataLossHour` har bytt namn till `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="45c25-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="45c25-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45c25-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="45c25-160">Parametern `Tag` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="45c25-161">Parametern `GracePeriodWithDataLossHour` har bytt namn till `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="45c25-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="45c25-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45c25-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="45c25-163">Parametern `Tag` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="45c25-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45c25-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="45c25-165">Parametern `Tag` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="45c25-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45c25-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="45c25-167">Parametern `PartnerResourceGroupName` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="45c25-168">Parametern `PartnerServerName` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="45c25-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="45c25-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45c25-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="45c25-170">Värdet `Usage_Anomaly` är inte längre giltigt för parametern `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="45c25-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="45c25-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45c25-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="45c25-172">Värdet `Usage_Anomaly` är inte längre giltigt för parametern `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="45c25-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="45c25-173">Större ändringar i Storage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="45c25-174">Följande typer av utdataegenskaper påverkades av den här uppdateringen:</span><span class="sxs-lookup"><span data-stu-id="45c25-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="45c25-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="45c25-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="45c25-176">Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="45c25-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="45c25-177">Den här ändringen påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="45c25-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="45c25-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="45c25-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="45c25-179">Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="45c25-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="45c25-180">Den här ändringen påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="45c25-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="45c25-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="45c25-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="45c25-182">Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="45c25-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="45c25-183">Den här ändringen påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="45c25-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="45c25-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="45c25-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="45c25-185">Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="45c25-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="45c25-186">Den här ändringen påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="45c25-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="45c25-187">Större ändringar i Profile-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45c25-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="45c25-188">Följande cmdletar och typer av utdata för cmdletar har ändrats i den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="45c25-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="45c25-189">Större ändringar i Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="45c25-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="45c25-190">Parametern ```EnvironmentName``` har tagits bort och ersatts med ```Environment```. ```Environment``` tar nu en sträng och inte ett ```AzureEnvironment```-objekt</span><span class="sxs-lookup"><span data-stu-id="45c25-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="45c25-191">Select-AzureRmProfile har bytt namn till Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="45c25-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="45c25-192">```Select-AzureRmProfile``` har bytt namn till ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="45c25-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="45c25-193">Save-AzureRmProfile har bytt namn till Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="45c25-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="45c25-194">```Save-AzureRmProfile``` har bytt namn till ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="45c25-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="45c25-195">Större ändringar i typ av utdata för PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="45c25-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="45c25-196">Egenskapen ```TokenCache``` ändrades till en typ som implementerar ```IAzureTokenCache``` i stället för en ```byte[]```</span><span class="sxs-lookup"><span data-stu-id="45c25-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="45c25-197">Större ändringar i typ av utdata för PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="45c25-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="45c25-198">Egenskapen ```AccountType``` har ändrats till ```Type```</span><span class="sxs-lookup"><span data-stu-id="45c25-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="45c25-199">Större ändringar i typ av utdata för PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="45c25-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="45c25-200">Egenskapen ```SubscriptionId``` har ändrats till ```Id```</span><span class="sxs-lookup"><span data-stu-id="45c25-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="45c25-201">Egenskapen ```SubscriptionName``` har ändrats till ```Name```</span><span class="sxs-lookup"><span data-stu-id="45c25-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="45c25-202">Större ändringar i typ av utdata för PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="45c25-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="45c25-203">Egenskapen ```TenantId``` har ändrats till ```Id```</span><span class="sxs-lookup"><span data-stu-id="45c25-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="45c25-204">Egenskapen ```Domain``` har ändrats till ```Directory```</span><span class="sxs-lookup"><span data-stu-id="45c25-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
