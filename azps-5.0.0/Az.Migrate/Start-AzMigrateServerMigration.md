---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271853"
---
# <span data-ttu-id="eca70-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="eca70-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="eca70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eca70-102">SYNOPSIS</span></span>
<span data-ttu-id="eca70-103">Startar migreringen för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="eca70-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="eca70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eca70-104">SYNTAX</span></span>

### <span data-ttu-id="eca70-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="eca70-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eca70-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="eca70-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eca70-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eca70-107">DESCRIPTION</span></span>
<span data-ttu-id="eca70-108">Startar migreringen för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="eca70-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="eca70-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eca70-109">EXAMPLES</span></span>

### <span data-ttu-id="eca70-110">Exempel 1: efter ID</span><span class="sxs-lookup"><span data-stu-id="eca70-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="eca70-111">Efter ID</span><span class="sxs-lookup"><span data-stu-id="eca70-111">By id</span></span>

## <span data-ttu-id="eca70-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eca70-112">PARAMETERS</span></span>

### <span data-ttu-id="eca70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca70-113">-DefaultProfile</span></span>
<span data-ttu-id="eca70-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eca70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca70-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca70-115">-InputObject</span></span>
<span data-ttu-id="eca70-116">Anger den replikerade Server för vilken migrering måste initieras.</span><span class="sxs-lookup"><span data-stu-id="eca70-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="eca70-117">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca70-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="eca70-118">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eca70-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eca70-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eca70-119">-SubscriptionId</span></span>
<span data-ttu-id="eca70-120">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="eca70-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="eca70-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="eca70-121">-TargetObjectID</span></span>
<span data-ttu-id="eca70-122">Anger den replcating-Server för vilken migrering måste initieras.</span><span class="sxs-lookup"><span data-stu-id="eca70-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="eca70-123">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca70-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="eca70-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="eca70-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="eca70-125">Anger om käll servern ska stängas av efter migreringen.</span><span class="sxs-lookup"><span data-stu-id="eca70-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="eca70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca70-126">CommonParameters</span></span>
<span data-ttu-id="eca70-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca70-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eca70-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca70-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eca70-129">INPUTS</span></span>

## <span data-ttu-id="eca70-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eca70-130">OUTPUTS</span></span>

### <span data-ttu-id="eca70-131">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="eca70-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="eca70-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eca70-132">NOTES</span></span>

<span data-ttu-id="eca70-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eca70-133">ALIASES</span></span>

<span data-ttu-id="eca70-134">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="eca70-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eca70-135">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="eca70-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eca70-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eca70-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eca70-137">INPUTOBJECT <IMigrationItem> : anger den replikerade Server för vilken migrering måste initieras.</span><span class="sxs-lookup"><span data-stu-id="eca70-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="eca70-138">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca70-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="eca70-139">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="eca70-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="eca70-140">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="eca70-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="eca70-141">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="eca70-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="eca70-142">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="eca70-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="eca70-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="eca70-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="eca70-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eca70-144">RELATED LINKS</span></span>

