# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Större ändringar för Microsoft Azure PowerShell 4.0.0

Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar. I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet. Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.

## <a name="table-of-contents"></a>Innehållsförteckning

- [Större ändringar i Compute-cmdletar](#breaking-changes-to-compute-cmdlets)
- [Större ändringar i EventHub-cmdletar](#breaking-changes-to-eventhub-cmdlets)
- [Större ändringar i Insights-cmdletar](#breaking-changes-to-insights-cmdlets)
- [Större ändringar i Network-cmdletar](#breaking-changes-to-network-cmdlets)
- [Större ändringar i ServiceBus-cmdletar](#breaking-changes-to-servicebus-cmdlets)
- [Större ändringar i Sql-cmdletar](#breaking-changes-to-sql-cmdlets)
- [Större ändringar i Storage-cmdletar](#breaking-changes-to-storage-cmdlets)
- [Större ändringar i Profile-cmdletar](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a>Större ändringar i Compute-cmdletar

Följande typer av utdata påverkades av den här uppdateringen:

### <a name="psvirtualmachine"></a>PSVirtualMachine
- Egenskaperna `DataDiskNames` och `NetworkInterfaceIDs` på den översta nivån av objektet `PSVirtualMachine` har tagits bort från utdatatypen. De här egenskaperna har alltid varit tillgängliga i egenskaperna `StorageProfile` och `NetworkProfile` för objektet `PSVirtualMachine` och framöver är de endast tillgängliga där.
- Den här ändringen påverkar följande cmdletar:
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Större ändringar i EventHub-cmdletar

Följande cmdletar påverkades av den här uppdateringen:

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`

## <a name="breaking-changes-to-insights-cmdlets"></a>Större ändringar i Insights-cmdletar

Följande cmdletar påverkades av den här uppdateringen:
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- Den här cmdleten har gjorts inaktuell.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- Utdata från den här cmdleten har ändrats från en lista med ett enda objekt till ett enda objekt. Det här objektet innehåller ID för begäran och statuskod.
    
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
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- Den här cmdleten har gjorts inaktuell.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- Varje element i utdatainformationen (en lista över objekt) för den här cmdleten har jämnats ut. Istället för att returnera objekt med strukturen `{ Id, Location, Name, Tags, Properties }` returnerar den objekt med strukturen `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, som är alla attribut för en Azure-resurs samt alla attribut för en AlertRuleResource på den översta nivån.
    
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
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- Fältet `AutoscaleSettingResourceName` är inaktuellt eftersom det alltid har samma värde som fältet `Name`.

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
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- Utdata från den här cmdleten kommer att ändras från `Boolean` till objekt som innehåller `RequestId` och `StatusCode`

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
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- Utdata från den här cmdleten kommer att ändras från ett objekt som innehåller ID för begäran, statuskod och den uppdaterade eller nya resursen
    
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
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- Kommandot kommer att ändras till `Update-AzureRmDiagnsoticSettings`

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Större ändringar i Network-cmdletar

Följande cmdletar påverkades av den här uppdateringen:

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- Parametern `EnableBgp` har ändrats för att ta en `boolean` i stället för en `string`

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Större ändringar i ServiceBus-cmdletar

Följande cmdletar påverkades av den här uppdateringen:

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- Egenskapen `ResourceGroupName` har tagits bort från utdatatypen `NamespaceAttributes`

## <a name="breaking-changes-to-sql-cmdlets"></a>Större ändringar i Sql-cmdletar

Följande cmdletar påverkades av den här uppdateringen:

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- Parametern `Tag` har tagits bort
- Parametern `GracePeriodWithDataLossHour` har bytt namn till `GracePeriodWithDataLossHours`

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- Parametern `Tag` har tagits bort
- Parametern `GracePeriodWithDataLossHour` har bytt namn till `GracePeriodWithDataLossHours`

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- Parametern `Tag` har tagits bort

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- Parametern `Tag` har tagits bort

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- Parametern `PartnerResourceGroupName` har tagits bort
- Parametern `PartnerServerName` har tagits bort

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- Värdet `Usage_Anomaly` är inte längre giltigt för parametern `ExcludedDetectionType`

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- Värdet `Usage_Anomaly` är inte längre giltigt för parametern `ExcludedDetectionType`

## <a name="breaking-changes-to-storage-cmdlets"></a>Större ändringar i Storage-cmdletar

Följande typer av utdataegenskaper påverkades av den här uppdateringen:

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Den här ändringen påverkar följande cmdletar:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Den här ändringen påverkar följande cmdletar:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- Den här ändringen påverkar följande cmdletar:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- Följande egenskaper har tagits bort från den här typen (_Obs_! De finns fortfarande i egenskapen `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- Den här ändringen påverkar följande cmdletar:
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

## <a name="breaking-changes-to-profile-cmdlets"></a>Större ändringar i Profile-cmdletar

Följande cmdletar och typer av utdata för cmdletar har ändrats i den här uppdateringen.

### <a name="add-azurermaccount-breaking-changes"></a>Större ändringar i Add-AzureRmAccount

- Parametern ```EnvironmentName``` har tagits bort och ersatts med ```Environment```. ```Environment``` tar nu en sträng och inte ett ```AzureEnvironment```-objekt

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile har bytt namn till Import-AzureRmContext

```Select-AzureRmProfile``` har bytt namn till ```Import-AzureRmContext```

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile har bytt namn till Save-AzureRmContext

```Save-AzureRmProfile``` har bytt namn till ```Save-AzureRmContext```

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>Större ändringar i typ av utdata för PSAzureContext

- Egenskapen ```TokenCache``` ändrades till en typ som implementerar ```IAzureTokenCache``` i stället för en ```byte[]```

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>Större ändringar i typ av utdata för PSAzureAccount

- Egenskapen ```AccountType``` har ändrats till ```Type```

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>Större ändringar i typ av utdata för PSAzureSubscription
- Egenskapen ```SubscriptionId``` har ändrats till ```Id```

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

- Egenskapen ```SubscriptionName``` har ändrats till ```Name```

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>Större ändringar i typ av utdata för PSAzureTenant

- Egenskapen ```TenantId``` har ändrats till ```Id```

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

- Egenskapen ```Domain``` har ändrats till ```Directory```

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
