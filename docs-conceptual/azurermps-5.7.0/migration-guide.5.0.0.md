# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Större ändringar för Microsoft Azure PowerShell 5.0.0

Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar. I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet. Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.

## <a name="table-of-contents"></a>Innehållsförteckning

- [Större ändringar i ApiManagement-cmdletar](#breaking-changes-to-apimanagement-cmdlets)
- [Större ändringar i Batch-cmdletar](#breaking-changes-to-batch-cmdlets)
- [Större ändringar i Compute-cmdletar](#breaking-changes-to-compute-cmdlets)
- [Större ändringar i EventHub-cmdletar](#breaking-changes-to-eventhub-cmdlets)
- [Större ändringar i Insights-cmdletar](#breaking-changes-to-insights-cmdlets)
- [Större ändringar i Network-cmdletar](#breaking-changes-to-network-cmdlets)
- [Större ändringar i Resources-cmdletar](#breaking-changes-to-resources-cmdlets)
- [Större ändringar i ServiceBus-cmdletar](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Större ändringar i ApiManagement-cmdletar

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Parametrarna ”UserName” och ”Password” ersätts av PSCredential

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Större ändringar i Batch-cmdletar

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Parametern `Password` ersätts av en säker sträng

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Parametern `Password` ersätts av en säker sträng

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Parametern `Password` ersätts av en säker sträng

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Växeln `RunElevated` har tagits bort och ersatts med `UserIdentity`.

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- `PSMultiInstanceSettings`-konstruktorn tar inte längre en obligatorisk `numberOfInstances`-parameter. Den tar i stället en nödvändig `coordinationCommandLine`-parameter.

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - Egenskapen `RunElevated` har tagits bort på `PSCloudTask`. Egenskapen `UserIdentity` har lagts till för att ersätta `RunElevated`.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Flera typer**

- Egenskapen `SchedulingError` på `PSExitConditions` har bytt namn till `PreProcessingError`.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Flera typer**

- Egenskapen `SchedulingError` på `PSJobPreparationTaskExecutionInformation` har bytt namn till `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` och `PSTaskExecutionInformation` till `FailureInformation`.
  - `FailureInformation` returneras när ett fel uppstår i uppgiften. Det här omfattar alla tidigare fall av schemaläggningsfel, slutkoder för aktiviteter utan nollor och fel vid uppladdning av filer från den nya funktionen för utdatafiler.
  - Det här är strukturerat på samma sätt som tidigare, så du behöver inte göra några ändringar i koden när du använder den här typen.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Det här påverkar dessutom: Get-AzureBatchPool, Get-AzureBatchSubtask och Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - `TargetDedicated` har tagits bort och ersatts med `TargetDedicatedComputeNodes` och `TargetLowPriorityComputeNodes`.
 - `TargetDedicatedComputeNodes` har ett alias `TargetDedicated`.

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Det här påverkar dessutom: Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Egenskaperna `TargetDedicated` och `CurrentDedicated` på `PSCloudPool` har bytt namn till `TargetDedicatedComputeNodes` och `CurrentDedicatedComputeNodes`.

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**PSCloudPool-typ**

- `ResizeError` har bytt namn till `ResizeErrors` på `PSCloudPool` och det är nu en samling.

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- Egenskapen `TargetDedicated` på `PSPoolSpecification` har bytt namn till `TargetDedicatedComputeNodes`.

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - `Name` har tagits bort och ersatts med `Path`.
 - `Path` har ett alias `Name`.

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Det här påverkar dessutom: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>Typen **PSNodeFile**

 - Egenskapen `Name` på `PSNodeFile` har bytt namn till `Path`.

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Egenskaperna `PreviousState` och `State` för `PSSubtaskInformation` är inte längre är av typen `TaskState`.De är istället av typen `SubtaskState`.
  - Till skillnad från `TaskState` har inte `SubtaskState` något `Active`-värde eftersom det inte är möjligt för underuppgifter att vara i tillståndet `Active`.

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Större ändringar i Compute-cmdletar

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Parametrarna ”UserName” och ”Password” ersätts av PSCredential

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Större ändringar i EventHub-cmdletar

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- Cmdleten ”New-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”New-AzureRmEventHubAuthorizationRule”
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- Cmdleten ”Get-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Get-AzureRmEventHubAuthorizationRule”
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- Cmdleten ”Set-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Set-AzureRmEventHubAuthorizationRule”
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- Cmdleten ”Remove-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Remove-AzureRmEventHubAuthorizationRule”
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- Cmdleten ”New-AzureRmEventHubNamespaceKey” har tagits bort. Använd cmdleten ”New-AzureRmEventHubKey”
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- Cmdleten ”Get-AzureRmEventHubNamespaceKey” har tagits bort. Använd cmdleten ”Get-AzureRmEventHubKey”
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes. 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes. 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes. 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Större ändringar i Insights-cmdletar

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Cmdleten **Add-AzureRMLogAlertRule** har gjorts inaktuell
- Efter den 1 oktober kommer den här cmdleten inte längre att ha någon effekt eftersom den här funktionen kommer att övergå till aktivitetsloggaviseringar. Mer information finns i https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- Cmdleten **Get-AzureRMUsage** har gjorts inaktuell

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Ändring i utdata: Fältet EventChannels från EventData-objektet (som returneras av de här cmdletarna) kommer att bli inaktuellt eftersom det nu returnerar ett konstant värde (Admin, Åtgärd.)

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Ändring i utdata: Utdata från den här cmdleten jämnas ut. Det innebär att egenskapsfältet kommer att tas bort för att förbättra användarupplevelsen.

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Ändring i utdata: Fältet AutoscaleSettingResourceName kommer att bli inaktuellt eftersom det alltid är samma som fältet Name.

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Ändring i utdata: Typen av utdata kommer att ändras så att ett enda objekt som innehåller ID för begäran och statuskod returneras.

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Större ändringar i Network-cmdletar

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Större ändringar i Resources-cmdletar

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Parametern ”Password” ersätts av SecureString

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Större ändringar i ServiceBus-cmdletar

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- Cmdleten ”Get-AzureRmServiceBusTopicAuthorizationRule” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- Cmdleten ”Get-AzureRmServiceBusTopicKey” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- Cmdleten ”New-AzureRmServiceBusTopicAuthorizationRule” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- Cmdleten ”New-AzureRmServiceBusTopicKey” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- Cmdleten ”Remove-AzureRmServiceBusTopicAuthorizationRule” har tagits bort. Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- Cmdleten ”Set-AzureRmServiceBusTopicAuthorizationRule” har tagits bort. Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- Cmdleten ”New-AzureRmServiceBusNamespaceKey” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusKey”.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- Cmdleten ”Get-AzureRmServiceBusQueueAuthorizationRule” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- Cmdleten ”Get-AzureRmServiceBusQueueKey” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- Cmdleten ”New-AzureRmServiceBusQueueAuthorizationRule” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- Cmdleten ”New-AzureRmServiceBusQueueKey” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- Cmdleten ”Remove-AzureRmServiceBusQueueAuthorizationRule” har tagits bort. Använd cmdleten ”GRemove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- Cmdleten ”Set-AzureRmServiceBusQueueAuthorizationRule” har tagits bort. Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- Cmdleten ”Get-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- Cmdleten ”Get-AzureRmServiceBusNamespaceKey” har tagits bort. Använd cmdleten ”Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- Cmdleten ”New-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- Cmdleten ”Remove-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- Cmdleten ”Set-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort. Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.

### <a name="type-namespaceattributes"></a>**Typen NamespaceAttributes**
- Följande egenskaper har tagits bort
    - Enabled
    - Status
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**Typen QueueAttribute**
- Följande egenskaper har angetts som föråldrade:
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a>**Typen TopicAttribute**
- Följande egenskaper har angetts som föråldrade:
    - Plats
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a>**Typen SubscriptionAttribute**
- Följande egenskaper har angetts som föråldrade
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Plats
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```