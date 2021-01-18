---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521742"
---
# <span data-ttu-id="116eb-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116eb-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="116eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="116eb-102">SYNOPSIS</span></span>
<span data-ttu-id="116eb-103">Anger återställnings egenskaper som mål nätverk och virtuell dator storlek för det angivna replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="116eb-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="116eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="116eb-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="116eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="116eb-105">DESCRIPTION</span></span>
<span data-ttu-id="116eb-106">Cmdleten **set-AzRecoveryServicesAsrReplicationProtectedItem** anger återställnings egenskaper för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="116eb-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="116eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="116eb-107">EXAMPLES</span></span>

### <span data-ttu-id="116eb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="116eb-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="116eb-109">Startar åtgärden att uppdatera inställningarna för skyddat objekt med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="116eb-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="116eb-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="116eb-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="116eb-111">Startar åtgärden att uppdatera det replikerade nätverkskortets inställningar för nätverks gränssnitt (NIC-reducering) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="116eb-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="116eb-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="116eb-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="116eb-113">Startar åtgärden att uppdatera det primära NIC-kortet för replikerade objekt (som används för återställda VM-inställningar) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="116eb-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="116eb-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="116eb-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="116eb-115">Startar åtgärden att uppdatera det replikerade objektet NIC (som används för återställda VM-inställningar) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="116eb-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="116eb-116">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="116eb-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="116eb-117">Startar åtgärden att uppdatera det replikerade replikeringssystemet markerat NOC TP aktivera påskyndad nätverks återställning (för Azure-till-Azure Disaster Recovery).</span><span class="sxs-lookup"><span data-stu-id="116eb-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="116eb-118">EnableAcceleratedNetworkingOnRecovery för att inaktivera snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="116eb-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="116eb-119">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="116eb-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="116eb-120">Starta uppdateringen för det angivna krypterade replikerade objektet för att använda krypterings information för VM för redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="116eb-121">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="116eb-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="116eb-122">Starta uppdaterings åtgärden för det angivna replikerade objektet för att använda den angivna närhets placerings gruppen för VM för redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="116eb-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="116eb-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="116eb-123">PARAMETERS</span></span>

### <span data-ttu-id="116eb-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="116eb-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="116eb-125">Anger konfigurations Detaljer för redundanstest och redundanskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="116eb-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="116eb-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="116eb-127">Anger disk konfigurationen till udpated för hanterad virtuell dator (Azure till Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="116eb-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116eb-128">-DefaultProfile</span></span>
<span data-ttu-id="116eb-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="116eb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="116eb-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="116eb-131">Anger den hemliga URL-adressen för disk kryptering med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="116eb-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="116eb-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="116eb-133">Anger det hemliga nyckel valv-ID för disk kryptering (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="116eb-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="116eb-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="116eb-135">Ord listan med disk resurs-ID till disk kryptering ange ARM-ID.</span><span class="sxs-lookup"><span data-stu-id="116eb-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="116eb-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="116eb-137">Anger angivet nätverkskort vid återställnings-VM när redundans använder accelererade nätverk.</span><span class="sxs-lookup"><span data-stu-id="116eb-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="116eb-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="116eb-138">-InputObject</span></span>
<span data-ttu-id="116eb-139">Indatavärdet till cmdleten: objektet skyddat objekt för ASR som motsvarar det replikerade objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="116eb-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="116eb-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="116eb-141">Anger den URL-version för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="116eb-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="116eb-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="116eb-143">Anger det ID för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="116eb-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="116eb-144">-LicenseType</span></span>
<span data-ttu-id="116eb-145">Ange licens typs valet för virtuella datorer med Windows Server.</span><span class="sxs-lookup"><span data-stu-id="116eb-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="116eb-146">Om du har rätt att använda användnings förmånen för Azure Hybrid (hubb) för migreringar och vill ange att nav-inställningen ska användas när det här skyddade objektet inte används, ställer du in licens typen på WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="116eb-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="116eb-147">-Name</span></span>
<span data-ttu-id="116eb-148">Anger namnet på den virtuella återställnings datorn som kommer att skapas på redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="116eb-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="116eb-149">-NicSelectionType</span></span>
<span data-ttu-id="116eb-150">Anger de nätverkskort-egenskaper som anges av användaren eller som standard.</span><span class="sxs-lookup"><span data-stu-id="116eb-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="116eb-151">Du kan ange NotSelected för att återgå till standardvärdena.</span><span class="sxs-lookup"><span data-stu-id="116eb-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="116eb-152">-PrimaryNic</span></span>
<span data-ttu-id="116eb-153">Anger det nätverkskort som ska användas som primärt NIC för recvcovery VM efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="116eb-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="116eb-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="116eb-155">Tillgänglighets uppsättning för replikerat skyddat objekt efter redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="116eb-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="116eb-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="116eb-157">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="116eb-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="116eb-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="116eb-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="116eb-159">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="116eb-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="116eb-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="116eb-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="116eb-161">Anger de mål Server grupper som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="116eb-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="116eb-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="116eb-163">Anger ID för det Azure Virtual Network som det skyddade objektet ska flyttas över.</span><span class="sxs-lookup"><span data-stu-id="116eb-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="116eb-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="116eb-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="116eb-165">Anger ID för nätverks säkerhets gruppen som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="116eb-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="116eb-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="116eb-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="116eb-167">Anger den statiska IP-adressen som ska kopplas till primär NIC vid återställning.</span><span class="sxs-lookup"><span data-stu-id="116eb-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="116eb-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="116eb-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="116eb-169">Anger namnet på under nätet i det virtuella Azure-nätverk som det här NÄTVERKSKORTet i det skyddade objektet ska anslutas till vid redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="116eb-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="116eb-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="116eb-171">Anger resurs-ID för omslags placering för att redundansväxla den virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="116eb-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="116eb-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="116eb-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="116eb-173">Anger ID för den offentliga IP-adressresursen som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="116eb-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="116eb-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="116eb-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="116eb-175">ID för Azure-adressresursen i det återställnings område där det skyddade objektet återställs på redundans.</span><span class="sxs-lookup"><span data-stu-id="116eb-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="116eb-176">-Storlek</span><span class="sxs-lookup"><span data-stu-id="116eb-176">-Size</span></span>
<span data-ttu-id="116eb-177">Anger storleken på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="116eb-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="116eb-178">Värdet ska vara från den uppsättning storlekar som stöds av virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="116eb-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="116eb-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="116eb-179">-TfoAzureVMName</span></span>
<span data-ttu-id="116eb-180">Anger namnet på den virtuella dator för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="116eb-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="116eb-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="116eb-181">-UpdateNic</span></span>
<span data-ttu-id="116eb-182">Anger NÄTVERKSKORTet för den virtuella dator för vilken denna cmdlet ställer in egenskapen för återställnings nätverk måste udpated.</span><span class="sxs-lookup"><span data-stu-id="116eb-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="116eb-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="116eb-183">-UseManagedDisk</span></span>
<span data-ttu-id="116eb-184">Anger om den virtuella Azure-datorn som skapas på redundans ska använda hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="116eb-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="116eb-185">-Confirm</span></span>
<span data-ttu-id="116eb-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="116eb-186">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116eb-187">-WhatIf</span></span>
<span data-ttu-id="116eb-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="116eb-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="116eb-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="116eb-189">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116eb-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116eb-190">CommonParameters</span></span>
<span data-ttu-id="116eb-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116eb-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116eb-192">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="116eb-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116eb-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="116eb-193">INPUTS</span></span>

### <span data-ttu-id="116eb-194">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116eb-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="116eb-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="116eb-195">OUTPUTS</span></span>

### <span data-ttu-id="116eb-196">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="116eb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="116eb-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="116eb-197">NOTES</span></span>

## <span data-ttu-id="116eb-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="116eb-198">RELATED LINKS</span></span>

[<span data-ttu-id="116eb-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116eb-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="116eb-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116eb-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="116eb-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116eb-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
