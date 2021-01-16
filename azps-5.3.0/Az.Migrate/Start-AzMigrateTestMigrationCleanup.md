---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523437"
---
# <span data-ttu-id="b802d-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="b802d-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="b802d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b802d-102">SYNOPSIS</span></span>
<span data-ttu-id="b802d-103">Rensar testmigreringen för servern som replikerar.</span><span class="sxs-lookup"><span data-stu-id="b802d-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="b802d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b802d-104">SYNTAX</span></span>

### <span data-ttu-id="b802d-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="b802d-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b802d-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="b802d-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b802d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b802d-107">DESCRIPTION</span></span>
<span data-ttu-id="b802d-108">Start-AzMigrateTestMigrationCleanup cmdlet initierar rensning av testmigreringen för servern för replikering.</span><span class="sxs-lookup"><span data-stu-id="b802d-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="b802d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b802d-109">EXAMPLES</span></span>

### <span data-ttu-id="b802d-110">Exempel 1: efter dator-ID.</span><span class="sxs-lookup"><span data-stu-id="b802d-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b802d-111">Efter dator-ID.</span><span class="sxs-lookup"><span data-stu-id="b802d-111">By machine id.</span></span>

### <span data-ttu-id="b802d-112">Exempel 2: efter indata</span><span class="sxs-lookup"><span data-stu-id="b802d-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b802d-113">Efter indata-objekt.</span><span class="sxs-lookup"><span data-stu-id="b802d-113">By input object.</span></span>

## <span data-ttu-id="b802d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b802d-114">PARAMETERS</span></span>

### <span data-ttu-id="b802d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b802d-115">-DefaultProfile</span></span>
<span data-ttu-id="b802d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b802d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b802d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b802d-117">-InputObject</span></span>
<span data-ttu-id="b802d-118">Anger den replikerade server som test migrations rensningen måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b802d-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b802d-119">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b802d-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802d-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b802d-120">-SubscriptionId</span></span>
<span data-ttu-id="b802d-121">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b802d-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b802d-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b802d-122">-TargetObjectID</span></span>
<span data-ttu-id="b802d-123">Anger den replikerade server som test migrations rensningen måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b802d-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b802d-124">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b802d-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b802d-125">CommonParameters</span></span>
<span data-ttu-id="b802d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b802d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b802d-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b802d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b802d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b802d-128">INPUTS</span></span>

## <span data-ttu-id="b802d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b802d-129">OUTPUTS</span></span>

### <span data-ttu-id="b802d-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="b802d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b802d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b802d-131">NOTES</span></span>

<span data-ttu-id="b802d-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b802d-132">ALIASES</span></span>

<span data-ttu-id="b802d-133">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b802d-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b802d-134">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b802d-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b802d-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b802d-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b802d-136">INPUTOBJECT <IMigrationItem> : anger den replikerade server som test migrations rensning måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b802d-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="b802d-137">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet</span><span class="sxs-lookup"><span data-stu-id="b802d-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="b802d-138">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="b802d-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b802d-139">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="b802d-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b802d-140">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="b802d-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b802d-141">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b802d-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b802d-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="b802d-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b802d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b802d-143">RELATED LINKS</span></span>

