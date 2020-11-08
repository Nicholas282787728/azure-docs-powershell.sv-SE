---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271850"
---
# <span data-ttu-id="b9286-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="b9286-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="b9286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9286-102">SYNOPSIS</span></span>
<span data-ttu-id="b9286-103">Startar testmigreringen för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="b9286-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="b9286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9286-104">SYNTAX</span></span>

### <span data-ttu-id="b9286-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="b9286-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9286-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="b9286-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9286-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9286-107">DESCRIPTION</span></span>
<span data-ttu-id="b9286-108">Start-AzMigrateTestMigration cmdlet initierar testmigreringen för servern för replikering.</span><span class="sxs-lookup"><span data-stu-id="b9286-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="b9286-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9286-109">EXAMPLES</span></span>

### <span data-ttu-id="b9286-110">Exempel 1: efter dator-ID.</span><span class="sxs-lookup"><span data-stu-id="b9286-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b9286-111">Efter dator-ID.</span><span class="sxs-lookup"><span data-stu-id="b9286-111">By machine id.</span></span>

### <span data-ttu-id="b9286-112">Exempel 2: efter indata</span><span class="sxs-lookup"><span data-stu-id="b9286-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b9286-113">Efter indata-objekt.</span><span class="sxs-lookup"><span data-stu-id="b9286-113">By input object.</span></span>

## <span data-ttu-id="b9286-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9286-114">PARAMETERS</span></span>

### <span data-ttu-id="b9286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9286-115">-DefaultProfile</span></span>
<span data-ttu-id="b9286-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9286-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9286-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9286-117">-InputObject</span></span>
<span data-ttu-id="b9286-118">Anger den replikerade server som testmigreringen måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b9286-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="b9286-119">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9286-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="b9286-120">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b9286-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9286-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9286-121">-SubscriptionId</span></span>
<span data-ttu-id="b9286-122">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b9286-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b9286-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b9286-123">-TargetObjectID</span></span>
<span data-ttu-id="b9286-124">Anger den replikerade server som testmigreringen måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b9286-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="b9286-125">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9286-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="b9286-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="b9286-126">-TestNetworkID</span></span>
<span data-ttu-id="b9286-127">Uppdaterar det virtuella nätverks-ID: t i mål Azure-prenumerationen som ska användas för testning av migrering.</span><span class="sxs-lookup"><span data-stu-id="b9286-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="b9286-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9286-128">CommonParameters</span></span>
<span data-ttu-id="b9286-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9286-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9286-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9286-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9286-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9286-131">INPUTS</span></span>

## <span data-ttu-id="b9286-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9286-132">OUTPUTS</span></span>

### <span data-ttu-id="b9286-133">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="b9286-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b9286-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9286-134">NOTES</span></span>

<span data-ttu-id="b9286-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b9286-135">ALIASES</span></span>

<span data-ttu-id="b9286-136">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b9286-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9286-137">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b9286-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9286-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9286-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9286-139">INPUTOBJECT <IMigrationItem> : anger den replikerade server som testmigreringen måste initieras för.</span><span class="sxs-lookup"><span data-stu-id="b9286-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="b9286-140">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9286-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="b9286-141">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="b9286-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b9286-142">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="b9286-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b9286-143">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="b9286-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b9286-144">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b9286-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b9286-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="b9286-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b9286-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9286-146">RELATED LINKS</span></span>

