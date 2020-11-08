---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271854"
---
# <span data-ttu-id="da6f0-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="da6f0-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="da6f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="da6f0-103">Startar om replikeringen för angiven server.</span><span class="sxs-lookup"><span data-stu-id="da6f0-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="da6f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da6f0-104">SYNTAX</span></span>

### <span data-ttu-id="da6f0-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="da6f0-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="da6f0-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="da6f0-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="da6f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da6f0-107">DESCRIPTION</span></span>
<span data-ttu-id="da6f0-108">Restart-AzMigrateServerReplication cmdlet reparerar replikeringen för den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="da6f0-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="da6f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da6f0-109">EXAMPLES</span></span>

### <span data-ttu-id="da6f0-110">Exempel 1: efter ID.</span><span class="sxs-lookup"><span data-stu-id="da6f0-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="da6f0-111">Efter ID.</span><span class="sxs-lookup"><span data-stu-id="da6f0-111">By id.</span></span>

### <span data-ttu-id="da6f0-112">Exempel 2: efter indata</span><span class="sxs-lookup"><span data-stu-id="da6f0-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="da6f0-113">Efter indata-objekt.</span><span class="sxs-lookup"><span data-stu-id="da6f0-113">By Input Object.</span></span>

## <span data-ttu-id="da6f0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da6f0-114">PARAMETERS</span></span>

### <span data-ttu-id="da6f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6f0-115">-DefaultProfile</span></span>
<span data-ttu-id="da6f0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da6f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da6f0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da6f0-117">-InputObject</span></span>
<span data-ttu-id="da6f0-118">Anger datorobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="da6f0-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="da6f0-119">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da6f0-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da6f0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da6f0-120">-SubscriptionId</span></span>
<span data-ttu-id="da6f0-121">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="da6f0-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="da6f0-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="da6f0-122">-TargetObjectID</span></span>
<span data-ttu-id="da6f0-123">Anger den replcating-server vars omsynkronisering måste initieras.</span><span class="sxs-lookup"><span data-stu-id="da6f0-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="da6f0-124">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da6f0-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="da6f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6f0-125">CommonParameters</span></span>
<span data-ttu-id="da6f0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6f0-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da6f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6f0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da6f0-128">INPUTS</span></span>

## <span data-ttu-id="da6f0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da6f0-129">OUTPUTS</span></span>

### <span data-ttu-id="da6f0-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="da6f0-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="da6f0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da6f0-131">NOTES</span></span>

<span data-ttu-id="da6f0-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da6f0-132">ALIASES</span></span>

<span data-ttu-id="da6f0-133">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="da6f0-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da6f0-134">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="da6f0-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da6f0-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da6f0-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da6f0-136">INPUTOBJECT <IMigrationItem> : anger datorobjektet för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="da6f0-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="da6f0-137">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="da6f0-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="da6f0-138">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="da6f0-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="da6f0-139">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="da6f0-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="da6f0-140">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="da6f0-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="da6f0-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="da6f0-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="da6f0-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da6f0-142">RELATED LINKS</span></span>

