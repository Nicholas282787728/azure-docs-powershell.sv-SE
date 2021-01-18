---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521127"
---
# <span data-ttu-id="da7cb-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="da7cb-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="da7cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="da7cb-103">Uppdaterar mål egenskaperna för servern som replikerar.</span><span class="sxs-lookup"><span data-stu-id="da7cb-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="da7cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da7cb-104">SYNTAX</span></span>

### <span data-ttu-id="da7cb-105">ByIDVMwareCbt (standard)</span><span class="sxs-lookup"><span data-stu-id="da7cb-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="da7cb-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="da7cb-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="da7cb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da7cb-107">DESCRIPTION</span></span>
<span data-ttu-id="da7cb-108">Set-AzMigrateServerReplication cmdlet uppdaterar mål egenskaperna för den replikerande servern.</span><span class="sxs-lookup"><span data-stu-id="da7cb-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="da7cb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da7cb-109">EXAMPLES</span></span>

### <span data-ttu-id="da7cb-110">Exempel 1: uppdatera efter ID</span><span class="sxs-lookup"><span data-stu-id="da7cb-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="da7cb-111">Efter ID.</span><span class="sxs-lookup"><span data-stu-id="da7cb-111">By id.</span></span>

## <span data-ttu-id="da7cb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da7cb-112">PARAMETERS</span></span>

### <span data-ttu-id="da7cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7cb-113">-DefaultProfile</span></span>
<span data-ttu-id="da7cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da7cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7cb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da7cb-115">-InputObject</span></span>
<span data-ttu-id="da7cb-116">Anger den replikerade server som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="da7cb-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="da7cb-117">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="da7cb-118">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da7cb-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da7cb-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="da7cb-119">-NicToUpdate</span></span>
<span data-ttu-id="da7cb-120">Uppdaterar NÄTVERKSKORTet för den virtuella Azure VM.</span><span class="sxs-lookup"><span data-stu-id="da7cb-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="da7cb-121">För att konstruera kan du läsa avsnittet anteckningar för NICTOUPDATE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da7cb-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7cb-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da7cb-122">-SubscriptionId</span></span>
<span data-ttu-id="da7cb-123">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="da7cb-123">The subscription Id.</span></span>

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

### <span data-ttu-id="da7cb-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="da7cb-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="da7cb-125">Anger den tillgänglighets uppsättning som ska användas för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="da7cb-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="da7cb-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="da7cb-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="da7cb-127">Anger tillgänglighets zonen som ska användas för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="da7cb-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="da7cb-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="da7cb-128">-TargetNetworkId</span></span>
<span data-ttu-id="da7cb-129">Uppdaterar det virtuella nätverks-ID: t i den mål Azure-prenumeration som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="da7cb-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="da7cb-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="da7cb-130">-TargetObjectID</span></span>
<span data-ttu-id="da7cb-131">Anger den replcating-server som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="da7cb-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="da7cb-132">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="da7cb-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="da7cb-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="da7cb-134">Uppdaterar resurs grupps-ID: t i den mål Azure-prenumeration som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="da7cb-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="da7cb-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="da7cb-135">-TargetVMName</span></span>
<span data-ttu-id="da7cb-136">Anger den replcating-server som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="da7cb-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="da7cb-137">ID ska hämtas med hjälp av Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="da7cb-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="da7cb-138">-TargetVMSize</span></span>
<span data-ttu-id="da7cb-139">Uppdaterar SKU för den virtuella Azure VM som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="da7cb-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="da7cb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7cb-140">CommonParameters</span></span>
<span data-ttu-id="da7cb-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7cb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7cb-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da7cb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7cb-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da7cb-143">INPUTS</span></span>

## <span data-ttu-id="da7cb-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da7cb-144">OUTPUTS</span></span>

### <span data-ttu-id="da7cb-145">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="da7cb-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="da7cb-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da7cb-146">NOTES</span></span>

<span data-ttu-id="da7cb-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da7cb-147">ALIASES</span></span>

<span data-ttu-id="da7cb-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="da7cb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da7cb-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="da7cb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da7cb-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da7cb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da7cb-151">INPUTOBJECT <IMigrationItem> : anger den replikerade server som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="da7cb-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="da7cb-152">Serverobjektet kan hämtas med Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="da7cb-153">`[Location <String>]`: Resurs plats</span><span class="sxs-lookup"><span data-stu-id="da7cb-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="da7cb-154">`[CurrentJobId <String>]`: ARM-ID för jobbet som körs.</span><span class="sxs-lookup"><span data-stu-id="da7cb-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="da7cb-155">`[CurrentJobName <String>]`: Jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="da7cb-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="da7cb-156">`[CurrentJobStartTime <DateTime?>]`: Start tiden för jobbet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="da7cb-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Anpassade inställningar för migreringstabellen.</span><span class="sxs-lookup"><span data-stu-id="da7cb-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="da7cb-158">NICTOUPDATE <IVMwareCbtNicInput [] >: uppdaterar NÄTVERKSKORTet för den virtuella Azure VM.</span><span class="sxs-lookup"><span data-stu-id="da7cb-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="da7cb-159">`IsPrimaryNic <String>`: Ett värde som anger om detta är det primära NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="da7cb-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="da7cb-160">`NicId <String>`: NIC-ID.</span><span class="sxs-lookup"><span data-stu-id="da7cb-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="da7cb-161">`[IsSelectedForMigration <String>]`: Ett värde som anger om detta nätverkskort är markerat för migrering.</span><span class="sxs-lookup"><span data-stu-id="da7cb-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="da7cb-162">`[TargetStaticIPAddress <String>]`: Den statiska IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="da7cb-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="da7cb-163">`[TargetSubnetName <String>]`: Mål under nätets namn.</span><span class="sxs-lookup"><span data-stu-id="da7cb-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="da7cb-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da7cb-164">RELATED LINKS</span></span>

