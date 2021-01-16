---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391680"
---
# <span data-ttu-id="93467-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="93467-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="93467-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93467-102">SYNOPSIS</span></span>
<span data-ttu-id="93467-103">Hämtar statusen för ett Azure Migrate-jobb.</span><span class="sxs-lookup"><span data-stu-id="93467-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="93467-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93467-104">SYNTAX</span></span>

### <span data-ttu-id="93467-105">ListByName (standard)</span><span class="sxs-lookup"><span data-stu-id="93467-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93467-106">GetById</span><span class="sxs-lookup"><span data-stu-id="93467-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93467-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="93467-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="93467-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="93467-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93467-109">ListById</span><span class="sxs-lookup"><span data-stu-id="93467-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="93467-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93467-110">DESCRIPTION</span></span>
<span data-ttu-id="93467-111">Get-AzMigrateJob cmdlet retrives status för ett Azure Migrate-jobb.</span><span class="sxs-lookup"><span data-stu-id="93467-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="93467-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93467-112">EXAMPLES</span></span>

### <span data-ttu-id="93467-113">Exempel 1: get per jobb-ID</span><span class="sxs-lookup"><span data-stu-id="93467-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="93467-114">Då hämtas ett jobb efter ID.</span><span class="sxs-lookup"><span data-stu-id="93467-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="93467-115">Exempel 2: lista efter resurs grupp och projekt</span><span class="sxs-lookup"><span data-stu-id="93467-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="93467-116">Det här får alla jobb i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="93467-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="93467-117">Exempel 3: Hämta efter resurs grupp, projekt och jobbnamn</span><span class="sxs-lookup"><span data-stu-id="93467-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="93467-118">Detta får ett specifikt jobb.</span><span class="sxs-lookup"><span data-stu-id="93467-118">This gets a specific job.</span></span>

## <span data-ttu-id="93467-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93467-119">PARAMETERS</span></span>

### <span data-ttu-id="93467-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93467-120">-DefaultProfile</span></span>
<span data-ttu-id="93467-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93467-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93467-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="93467-122">-Filter</span></span>
<span data-ttu-id="93467-123">Alternativ för OData-filter.</span><span class="sxs-lookup"><span data-stu-id="93467-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93467-124">-InputObject</span></span>
<span data-ttu-id="93467-125">Anger jobbobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="93467-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="93467-126">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="93467-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="93467-127">-JobID</span></span>
<span data-ttu-id="93467-128">Anger det jobb-ID som informationen måste hämtas för.</span><span class="sxs-lookup"><span data-stu-id="93467-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="93467-129">-JobName</span></span>
<span data-ttu-id="93467-130">Jobb-ID</span><span class="sxs-lookup"><span data-stu-id="93467-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="93467-131">-ProjectID</span></span>
<span data-ttu-id="93467-132">Anger det Azure Migrate-projekt där servrar replikeras.</span><span class="sxs-lookup"><span data-stu-id="93467-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-133">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="93467-133">-ProjectName</span></span>
<span data-ttu-id="93467-134">Namnet på det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="93467-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="93467-135">-ResourceGroupID</span></span>
<span data-ttu-id="93467-136">Anger resurs gruppen för Azure Migrate-projektet i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="93467-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93467-137">-ResourceGroupName</span></span>
<span data-ttu-id="93467-138">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="93467-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93467-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93467-139">-SubscriptionId</span></span>
<span data-ttu-id="93467-140">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="93467-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="93467-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93467-141">CommonParameters</span></span>
<span data-ttu-id="93467-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93467-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93467-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93467-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93467-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93467-144">INPUTS</span></span>

## <span data-ttu-id="93467-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93467-145">OUTPUTS</span></span>

### <span data-ttu-id="93467-146">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="93467-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="93467-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93467-147">NOTES</span></span>

<span data-ttu-id="93467-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="93467-148">ALIASES</span></span>

<span data-ttu-id="93467-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="93467-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93467-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="93467-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93467-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93467-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93467-152">INPUTOBJECT <IJob> : anger jobbobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="93467-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="93467-153">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="93467-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="93467-154">`[ActivityId <String>]`: Aktivitets-ID.</span><span class="sxs-lookup"><span data-stu-id="93467-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="93467-155">`[AllowedAction <String[]>]`: Den tillåtna åtgärden som jobbet är.</span><span class="sxs-lookup"><span data-stu-id="93467-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="93467-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: De påverkade objekt egenskaperna som käll Server, käll moln, mål server, mål moln etc. baserat på informationen i arbets flödes objekt.</span><span class="sxs-lookup"><span data-stu-id="93467-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="93467-157">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="93467-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="93467-158">`[EndTime <DateTime?>]`: Slut tiden.</span><span class="sxs-lookup"><span data-stu-id="93467-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="93467-159">`[Error <IJobErrorDetails[]>]`: Felen.</span><span class="sxs-lookup"><span data-stu-id="93467-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="93467-160">`[CreationTime <DateTime?>]`: Fel när jobbet skapades.</span><span class="sxs-lookup"><span data-stu-id="93467-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="93467-161">`[ErrorLevel <String>]`: Fel nivå fel.</span><span class="sxs-lookup"><span data-stu-id="93467-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="93467-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Felkoden.</span><span class="sxs-lookup"><span data-stu-id="93467-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="93467-163">`[ProviderErrorDetailErrorId <String>]`: Leverantörens fel-ID.</span><span class="sxs-lookup"><span data-stu-id="93467-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="93467-164">`[ProviderErrorDetailErrorMessage <String>]`: Fel meddelandet.</span><span class="sxs-lookup"><span data-stu-id="93467-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="93467-165">`[ProviderErrorDetailPossibleCaus <String>]`: Möjliga orsaker till felet.</span><span class="sxs-lookup"><span data-stu-id="93467-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="93467-166">`[ProviderErrorDetailRecommendedAction <String>]`: Rekommenderad åtgärd för att åtgärda felet.</span><span class="sxs-lookup"><span data-stu-id="93467-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="93467-167">`[ServiceErrorDetailActivityId <String>]`: Aktivitets-ID.</span><span class="sxs-lookup"><span data-stu-id="93467-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="93467-168">`[ServiceErrorDetailCode <String>]`: Felkod.</span><span class="sxs-lookup"><span data-stu-id="93467-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="93467-169">`[ServiceErrorDetailMessage <String>]`: Fel meddelande.</span><span class="sxs-lookup"><span data-stu-id="93467-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="93467-170">`[ServiceErrorDetailPossibleCaus <String>]`: Möjliga orsaker till felet.</span><span class="sxs-lookup"><span data-stu-id="93467-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="93467-171">`[ServiceErrorDetailRecommendedAction <String>]`: Rekommenderad åtgärd för att åtgärda felet.</span><span class="sxs-lookup"><span data-stu-id="93467-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="93467-172">`[TaskId <String>]`: Aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="93467-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="93467-173">`[FriendlyName <String>]`: Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="93467-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="93467-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="93467-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="93467-175">`[StartTime <DateTime?>]`: Start tiden.</span><span class="sxs-lookup"><span data-stu-id="93467-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="93467-176">`[State <String>]`: Jobbets status.</span><span class="sxs-lookup"><span data-stu-id="93467-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="93467-177">Det är ett av följande värden – NotStarted, InProgress, lyckades, misslyckades, annullerat, upphävt eller annat.</span><span class="sxs-lookup"><span data-stu-id="93467-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="93467-178">`[StateDescription <String>]`: Beskrivningen av jobbets status.</span><span class="sxs-lookup"><span data-stu-id="93467-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="93467-179">För att det ska vara klart kan beskrivningen kunna genomföras, PartiallySucceeded, CompletedWithInformation eller hoppas över.</span><span class="sxs-lookup"><span data-stu-id="93467-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="93467-180">`[TargetInstanceType <String>]`: Den påverkade objekts typen {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} klass.</span><span class="sxs-lookup"><span data-stu-id="93467-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="93467-181">`[TargetObjectId <String>]`: Det påverkade objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="93467-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="93467-182">`[TargetObjectName <String>]`: Namnet på det aktuella objektet.</span><span class="sxs-lookup"><span data-stu-id="93467-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="93467-183">`[Task <IAsrTask[]>]`: Aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="93467-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="93467-184">`[AllowedAction <String[]>]`: De uppgifter som gäller för den här uppgiften.</span><span class="sxs-lookup"><span data-stu-id="93467-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="93467-185">`[CustomDetailInstanceType <String>]`: Typen av aktivitets information.</span><span class="sxs-lookup"><span data-stu-id="93467-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="93467-186">`[EndTime <DateTime?>]`: Slut tiden.</span><span class="sxs-lookup"><span data-stu-id="93467-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="93467-187">`[Error <IJobErrorDetails[]>]`: Information om aktivitets fel.</span><span class="sxs-lookup"><span data-stu-id="93467-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="93467-188">`[FriendlyName <String>]`: Namnet.</span><span class="sxs-lookup"><span data-stu-id="93467-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="93467-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Underordnade aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="93467-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="93467-190">`[GroupTaskCustomDetailInstanceType <String>]`: Typen av aktivitets information.</span><span class="sxs-lookup"><span data-stu-id="93467-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="93467-191">`[Name <String>]`: Det unika aktivitets namnet.</span><span class="sxs-lookup"><span data-stu-id="93467-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="93467-192">`[StartTime <DateTime?>]`: Start tiden.</span><span class="sxs-lookup"><span data-stu-id="93467-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="93467-193">`[State <String>]`: Tillståndet.</span><span class="sxs-lookup"><span data-stu-id="93467-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="93467-194">Det är ett av följande värden – NotStarted, InProgress, lyckades, misslyckades, annullerat, upphävt eller annat.</span><span class="sxs-lookup"><span data-stu-id="93467-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="93467-195">`[StateDescription <String>]`: Beskrivningen av uppgifts tillståndet.</span><span class="sxs-lookup"><span data-stu-id="93467-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="93467-196">Till exempel: om du lyckas kan du beskriva en beskrivning, PartiallySucceeded, CompletedWithInformation eller hoppa över.</span><span class="sxs-lookup"><span data-stu-id="93467-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="93467-197">`[TaskId <String>]`: ID.</span><span class="sxs-lookup"><span data-stu-id="93467-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="93467-198">`[TaskType <String>]`: Typen av uppgift.</span><span class="sxs-lookup"><span data-stu-id="93467-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="93467-199">Informationen i egenskapen CustomDetails är beroende av den här typen.</span><span class="sxs-lookup"><span data-stu-id="93467-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="93467-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93467-200">RELATED LINKS</span></span>

