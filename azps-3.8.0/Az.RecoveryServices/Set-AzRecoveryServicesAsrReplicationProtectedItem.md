---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091257"
---
# <span data-ttu-id="969d7-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="969d7-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="969d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="969d7-102">SYNOPSIS</span></span>
<span data-ttu-id="969d7-103">Anger återställnings egenskaper som mål nätverk och virtuell dator storlek för det angivna replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="969d7-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="969d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="969d7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="969d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="969d7-105">DESCRIPTION</span></span>
<span data-ttu-id="969d7-106">Cmdleten **set-AzRecoveryServicesAsrReplicationProtectedItem** anger återställnings egenskaper för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="969d7-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="969d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="969d7-107">EXAMPLES</span></span>

### <span data-ttu-id="969d7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="969d7-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="969d7-109">Startar åtgärden att uppdatera inställningarna för skyddat objekt med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="969d7-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="969d7-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="969d7-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="969d7-111">Startar åtgärden att uppdatera det replikerade nätverkskortets inställningar för nätverks gränssnitt (NIC-reducering) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="969d7-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="969d7-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="969d7-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="969d7-113">Startar åtgärden att uppdatera det primära NIC-kortet för replikerade objekt (som används för återställda VM-inställningar) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="969d7-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="969d7-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="969d7-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="969d7-115">Startar åtgärden att uppdatera det replikerade objektet NIC (som används för återställda VM-inställningar) med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="969d7-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="969d7-116">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="969d7-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="969d7-117">Startar åtgärden att uppdatera det replikerade replikeringssystemet markerat NOC TP aktivera påskyndad nätverks återställning (för Azure-till-Azure Disaster Recovery).</span><span class="sxs-lookup"><span data-stu-id="969d7-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="969d7-118">EnableAcceleratedNetworkingOnRecovery för att inaktivera snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="969d7-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="969d7-119">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="969d7-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="969d7-120">Starta uppdateringen för det angivna krypterade replikerade objektet för att använda krypterings information för VM för redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="969d7-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="969d7-121">PARAMETERS</span></span>

### <span data-ttu-id="969d7-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="969d7-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="969d7-123">Anger konfigurations Detaljer för redundanstest och redundanskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="969d7-123">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="969d7-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="969d7-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="969d7-125">Anger disk konfigurationen till udpated för hanterad virtuell dator (Azure till Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="969d7-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="969d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969d7-126">-DefaultProfile</span></span>
<span data-ttu-id="969d7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="969d7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="969d7-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="969d7-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="969d7-129">Anger den hemliga URL-adressen för disk kryptering med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="969d7-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="969d7-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="969d7-131">Anger det hemliga nyckel valv-ID för disk kryptering (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="969d7-132">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="969d7-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="969d7-133">Ord listan med disk resurs-ID till disk kryptering ange ARM-ID.</span><span class="sxs-lookup"><span data-stu-id="969d7-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="969d7-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="969d7-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="969d7-135">Anger angivet nätverkskort vid återställnings-VM när redundans använder accelererade nätverk.</span><span class="sxs-lookup"><span data-stu-id="969d7-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="969d7-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="969d7-136">-InputObject</span></span>
<span data-ttu-id="969d7-137">Indatavärdet till cmdleten: objektet skyddat objekt för ASR som motsvarar det replikerade objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="969d7-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="969d7-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="969d7-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="969d7-139">Anger den URL-version för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="969d7-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="969d7-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="969d7-141">Anger det ID för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="969d7-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="969d7-142">-LicenseType</span></span>
<span data-ttu-id="969d7-143">Ange licens typs valet för virtuella datorer med Windows Server.</span><span class="sxs-lookup"><span data-stu-id="969d7-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="969d7-144">Om du har rätt att använda användnings förmånen för Azure Hybrid (hubb) för migreringar och vill ange att nav-inställningen ska användas när det här skyddade objektet inte används, ställer du in licens typen på WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="969d7-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="969d7-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="969d7-145">-Name</span></span>
<span data-ttu-id="969d7-146">Anger namnet på den virtuella återställnings datorn som kommer att skapas på redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="969d7-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="969d7-147">-NicSelectionType</span></span>
<span data-ttu-id="969d7-148">Anger de nätverkskort-egenskaper som anges av användaren eller som standard.</span><span class="sxs-lookup"><span data-stu-id="969d7-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="969d7-149">Du kan ange NotSelected för att återgå till standardvärdena.</span><span class="sxs-lookup"><span data-stu-id="969d7-149">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="969d7-150">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="969d7-150">-PrimaryNic</span></span>
<span data-ttu-id="969d7-151">Anger det nätverkskort som ska användas som primärt NIC för recvcovery VM efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="969d7-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="969d7-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="969d7-153">Tillgänglighets uppsättning för replikerat skyddat objekt efter redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="969d7-154">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="969d7-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="969d7-155">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="969d7-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="969d7-156">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="969d7-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="969d7-157">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="969d7-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="969d7-158">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="969d7-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="969d7-159">Anger de mål Server grupper som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="969d7-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="969d7-160">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="969d7-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="969d7-161">Anger ID för det Azure Virtual Network som det skyddade objektet ska flyttas över.</span><span class="sxs-lookup"><span data-stu-id="969d7-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="969d7-162">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="969d7-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="969d7-163">Anger ID för nätverks säkerhets gruppen som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="969d7-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="969d7-164">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="969d7-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="969d7-165">Anger den statiska IP-adressen som ska kopplas till primär NIC vid återställning.</span><span class="sxs-lookup"><span data-stu-id="969d7-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="969d7-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="969d7-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="969d7-167">Anger namnet på under nätet i det virtuella Azure-nätverk som det här NÄTVERKSKORTet i det skyddade objektet ska anslutas till vid redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="969d7-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="969d7-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="969d7-169">Anger ID för den offentliga IP-adressresursen som ska kopplas till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="969d7-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="969d7-170">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="969d7-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="969d7-171">ID för Azure-adressresursen i det återställnings område där det skyddade objektet återställs på redundans.</span><span class="sxs-lookup"><span data-stu-id="969d7-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="969d7-172">-Storlek</span><span class="sxs-lookup"><span data-stu-id="969d7-172">-Size</span></span>
<span data-ttu-id="969d7-173">Anger storleken på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="969d7-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="969d7-174">Värdet ska vara från den uppsättning storlekar som stöds av virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="969d7-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="969d7-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="969d7-175">-TfoAzureVMName</span></span>
<span data-ttu-id="969d7-176">Anger namnet på den virtuella dator för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="969d7-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="969d7-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="969d7-177">-UpdateNic</span></span>
<span data-ttu-id="969d7-178">Anger NÄTVERKSKORTet för den virtuella dator för vilken denna cmdlet ställer in egenskapen för återställnings nätverk måste udpated.</span><span class="sxs-lookup"><span data-stu-id="969d7-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="969d7-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="969d7-179">-UseManagedDisk</span></span>
<span data-ttu-id="969d7-180">Anger om den virtuella Azure-datorn som skapas på redundans ska använda hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="969d7-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="969d7-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="969d7-181">-Confirm</span></span>
<span data-ttu-id="969d7-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="969d7-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969d7-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969d7-183">-WhatIf</span></span>
<span data-ttu-id="969d7-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="969d7-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="969d7-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="969d7-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969d7-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969d7-186">CommonParameters</span></span>
<span data-ttu-id="969d7-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969d7-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969d7-188">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="969d7-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969d7-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="969d7-189">INPUTS</span></span>

### <span data-ttu-id="969d7-190">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="969d7-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="969d7-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="969d7-191">OUTPUTS</span></span>

### <span data-ttu-id="969d7-192">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="969d7-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="969d7-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="969d7-193">NOTES</span></span>

## <span data-ttu-id="969d7-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="969d7-194">RELATED LINKS</span></span>

[<span data-ttu-id="969d7-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="969d7-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="969d7-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="969d7-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="969d7-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="969d7-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
