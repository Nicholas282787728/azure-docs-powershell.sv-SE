---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521124"
---
# <span data-ttu-id="03eac-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="03eac-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="03eac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03eac-102">SYNOPSIS</span></span>
<span data-ttu-id="03eac-103">Stoppar replikering för den migrerade servern.</span><span class="sxs-lookup"><span data-stu-id="03eac-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="03eac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03eac-104">SYNTAX</span></span>

### <span data-ttu-id="03eac-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="03eac-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03eac-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="03eac-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03eac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03eac-107">DESCRIPTION</span></span>
<span data-ttu-id="03eac-108">Remove-AzMigrateServerReplication-cmdleten stoppar replikeringen för en migrerad Server.</span><span class="sxs-lookup"><span data-stu-id="03eac-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="03eac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03eac-109">EXAMPLES</span></span>

### <span data-ttu-id="03eac-110">Exempel 1: ta bort efter ID.</span><span class="sxs-lookup"><span data-stu-id="03eac-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="03eac-111">Synkronisera efter ID.</span><span class="sxs-lookup"><span data-stu-id="03eac-111">Resync by id.</span></span>

### <span data-ttu-id="03eac-112">Exempel 2: ta bort med indatavärdet</span><span class="sxs-lookup"><span data-stu-id="03eac-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="03eac-113">Efter namn.</span><span class="sxs-lookup"><span data-stu-id="03eac-113">By name.</span></span>

## <span data-ttu-id="03eac-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03eac-114">PARAMETERS</span></span>

### <span data-ttu-id="03eac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03eac-115">-DefaultProfile</span></span>
<span data-ttu-id="03eac-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03eac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03eac-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="03eac-117">-ForceRemove</span></span>
<span data-ttu-id="03eac-118">Anger om replikeringen måste göras borttagen.</span><span class="sxs-lookup"><span data-stu-id="03eac-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="03eac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03eac-119">-InputObject</span></span>
<span data-ttu-id="03eac-120">Anger datorobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="03eac-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="03eac-121">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="03eac-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03eac-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03eac-122">-SubscriptionId</span></span>
<span data-ttu-id="03eac-123">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="03eac-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="03eac-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="03eac-124">-TargetObjectID</span></span>
<span data-ttu-id="03eac-125">Anger den replcating-server som replicatio måste avaktiveras för.</span><span class="sxs-lookup"><span data-stu-id="03eac-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="03eac-126">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03eac-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="03eac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03eac-127">CommonParameters</span></span>
<span data-ttu-id="03eac-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03eac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03eac-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03eac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03eac-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03eac-130">INPUTS</span></span>

## <span data-ttu-id="03eac-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03eac-131">OUTPUTS</span></span>

### <span data-ttu-id="03eac-132">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="03eac-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="03eac-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03eac-133">NOTES</span></span>

<span data-ttu-id="03eac-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="03eac-134">ALIASES</span></span>

<span data-ttu-id="03eac-135">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="03eac-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03eac-136">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="03eac-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03eac-137">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03eac-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03eac-138">INPUTOBJECT <IMigrationItem> : anger datorobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="03eac-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="03eac-139">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="03eac-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="03eac-140">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="03eac-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="03eac-141">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="03eac-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="03eac-142">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="03eac-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="03eac-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="03eac-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="03eac-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03eac-144">RELATED LINKS</span></span>

