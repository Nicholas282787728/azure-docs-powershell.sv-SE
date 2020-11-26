---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270544"
---
# <span data-ttu-id="a8c08-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="a8c08-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="a8c08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8c08-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c08-103">Startar replikering för den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="a8c08-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="a8c08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8c08-104">SYNTAX</span></span>

### <span data-ttu-id="a8c08-105">ByIdDefaultUser (standard)</span><span class="sxs-lookup"><span data-stu-id="a8c08-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8c08-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="a8c08-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8c08-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="a8c08-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8c08-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="a8c08-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8c08-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8c08-109">DESCRIPTION</span></span>
<span data-ttu-id="a8c08-110">New-AzMigrateServerReplication-cmdleten startar replikeringen för en viss upptäckta server i Azure Migrate Project.</span><span class="sxs-lookup"><span data-stu-id="a8c08-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="a8c08-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8c08-111">EXAMPLES</span></span>

### <span data-ttu-id="a8c08-112">Exempel 1: när det bara finns en OS-skiva</span><span class="sxs-lookup"><span data-stu-id="a8c08-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a8c08-113">Detta gäller för scenariot när det bara finns en enda disk som måste skyddas.</span><span class="sxs-lookup"><span data-stu-id="a8c08-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="a8c08-114">Exempel 2: när det finns flera diskar</span><span class="sxs-lookup"><span data-stu-id="a8c08-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a8c08-115">Det här är för scenariot när det finns flera diskar som måste skyddas.</span><span class="sxs-lookup"><span data-stu-id="a8c08-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="a8c08-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8c08-116">PARAMETERS</span></span>

### <span data-ttu-id="a8c08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c08-117">-DefaultProfile</span></span>
<span data-ttu-id="a8c08-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8c08-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="a8c08-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="a8c08-120">Anger vilken encyption som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a8c08-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="a8c08-121">-DiskToInclude</span></span>
<span data-ttu-id="a8c08-122">Anger vilka diskar på käll servern som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="a8c08-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="a8c08-123">För att konstruera kan du läsa avsnittet anteckningar för DISKTOINCLUDE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8c08-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="a8c08-124">-DiskType</span></span>
<span data-ttu-id="a8c08-125">Anger vilken typ av disk som ska användas för Azure VM.</span><span class="sxs-lookup"><span data-stu-id="a8c08-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8c08-126">-InputObject</span></span>
<span data-ttu-id="a8c08-127">Anger vilken server som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="a8c08-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="a8c08-128">Serverobjektet kan hämtas med Get-AzMigrateServer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c08-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="a8c08-129">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8c08-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a8c08-130">-LicenseType</span></span>
<span data-ttu-id="a8c08-131">Anger om Azure Hybrid förmån är tillämpligt för käll servern som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="a8c08-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="a8c08-132">-MachineId</span></span>
<span data-ttu-id="a8c08-133">Anger dator-ID för den upptäckta server som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="a8c08-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="a8c08-134">-OSDiskID</span></span>
<span data-ttu-id="a8c08-135">Anger operativ Systems disken för käll servern som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="a8c08-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c08-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="a8c08-136">-PerformAutoResync</span></span>
<span data-ttu-id="a8c08-137">Anger om replikeringen ska repare ras automatiskt om ändrings spårningen går förlorad för käll servern under replikering.</span><span class="sxs-lookup"><span data-stu-id="a8c08-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="a8c08-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8c08-138">-SubscriptionId</span></span>
<span data-ttu-id="a8c08-139">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a8c08-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a8c08-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a8c08-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="a8c08-141">Anger den tillgänglighets uppsättning som ska användas för VM-creationSpecifies den tillgänglighets uppsättning som ska användas för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a8c08-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="a8c08-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="a8c08-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="a8c08-143">Anger tillgänglighets zonen som ska användas för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a8c08-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="a8c08-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8c08-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="a8c08-145">Anger det lagrings konto som ska användas för startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="a8c08-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="a8c08-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="a8c08-146">-TargetNetworkId</span></span>
<span data-ttu-id="a8c08-147">Anger det virtuella nätverks-ID i mål Azure-prenumerationen som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="a8c08-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="a8c08-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a8c08-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="a8c08-149">Anger det resurs grupps-ID inom mål Azure-prenumerationen som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="a8c08-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="a8c08-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="a8c08-150">-TargetSubnetName</span></span>
<span data-ttu-id="a8c08-151">Anger under nätets namn inom det virtuella mål Netowk som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="a8c08-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="a8c08-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="a8c08-152">-TargetVMName</span></span>
<span data-ttu-id="a8c08-153">Anger namnet på den virtuella Azure VM som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a8c08-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="a8c08-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="a8c08-154">-TargetVMSize</span></span>
<span data-ttu-id="a8c08-155">Anger SKU för den virtuella Azure VM som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a8c08-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="a8c08-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="a8c08-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="a8c08-157">Konto-ID.</span><span class="sxs-lookup"><span data-stu-id="a8c08-157">Account id.</span></span>

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

### <span data-ttu-id="a8c08-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c08-158">CommonParameters</span></span>
<span data-ttu-id="a8c08-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c08-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c08-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8c08-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c08-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8c08-161">INPUTS</span></span>

## <span data-ttu-id="a8c08-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8c08-162">OUTPUTS</span></span>

### <span data-ttu-id="a8c08-163">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="a8c08-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a8c08-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8c08-164">NOTES</span></span>

<span data-ttu-id="a8c08-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a8c08-165">ALIASES</span></span>

<span data-ttu-id="a8c08-166">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a8c08-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8c08-167">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a8c08-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8c08-168">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8c08-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8c08-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: anger de diskar på käll servern som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="a8c08-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="a8c08-170">`DiskId <String>`: Disk-ID.</span><span class="sxs-lookup"><span data-stu-id="a8c08-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="a8c08-171">`IsOSDisk <String>`: Ett värde som anger om disken är OS-disketten.</span><span class="sxs-lookup"><span data-stu-id="a8c08-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="a8c08-172">`LogStorageAccountId <String>`: ID för logganalys-kontot.</span><span class="sxs-lookup"><span data-stu-id="a8c08-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="a8c08-173">`LogStorageAccountSasSecretName <String>`: Nyckel valvets hemliga namn för logg lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a8c08-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="a8c08-174">`[DiskEncryptionSetId <String>]`: ID för DiskEncryptionSet ARM.</span><span class="sxs-lookup"><span data-stu-id="a8c08-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="a8c08-175">`[DiskType <DiskAccountType?>]`: Disk typen.</span><span class="sxs-lookup"><span data-stu-id="a8c08-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="a8c08-176">INPUTOBJECT <IVMwareMachine> : anger vilken server som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="a8c08-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="a8c08-177">Serverobjektet kan hämtas med Get-AzMigrateServer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c08-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="a8c08-178">`[GuestOSDetailOstype <String>]`: Typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="a8c08-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="a8c08-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8c08-179">RELATED LINKS</span></span>
