---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088020"
---
# <span data-ttu-id="965ff-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="965ff-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="965ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="965ff-102">SYNOPSIS</span></span>
<span data-ttu-id="965ff-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="965ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="965ff-104">SYNTAX</span></span>

### <span data-ttu-id="965ff-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="965ff-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="965ff-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="965ff-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965ff-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="965ff-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="965ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="965ff-108">DESCRIPTION</span></span>
<span data-ttu-id="965ff-109">Cmdleten **New-AzVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="965ff-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="965ff-110">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="965ff-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="965ff-111">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="965ff-111">These cmdlets are:</span></span>
- <span data-ttu-id="965ff-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="965ff-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="965ff-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="965ff-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="965ff-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="965ff-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="965ff-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="965ff-116">EXAMPLES</span></span>

### <span data-ttu-id="965ff-117">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="965ff-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="965ff-118">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="965ff-119">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="965ff-120">I det andra kommandot används cmdleten **New-AzVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="965ff-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="965ff-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="965ff-121">PARAMETERS</span></span>

### <span data-ttu-id="965ff-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="965ff-122">-AssignIdentity</span></span>
<span data-ttu-id="965ff-123">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="965ff-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="965ff-125">Den tid som automatiska reparationer har upphävts på grund av en tillstånds ändring på VM.</span><span class="sxs-lookup"><span data-stu-id="965ff-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="965ff-126">Grace-tiden inleds efter att statusen har ändrats.</span><span class="sxs-lookup"><span data-stu-id="965ff-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="965ff-127">Detta gör att du kan undvika för tidigt eller oavsiktlig reparation.</span><span class="sxs-lookup"><span data-stu-id="965ff-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="965ff-128">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="965ff-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="965ff-129">Standardvärdet är 5 minuter (PT5M).</span><span class="sxs-lookup"><span data-stu-id="965ff-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="965ff-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="965ff-131">Procent andelen (kapaciteten för scaleset) för virtuella datorer som kommer att repare ras samtidigt.</span><span class="sxs-lookup"><span data-stu-id="965ff-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="965ff-132">Standardvärdet är 20%.</span><span class="sxs-lookup"><span data-stu-id="965ff-132">The default value is 20%.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="965ff-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="965ff-134">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="965ff-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="965ff-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="965ff-135">-BootDiagnostic</span></span>
<span data-ttu-id="965ff-136">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="965ff-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-137">-DefaultProfile</span></span>
<span data-ttu-id="965ff-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="965ff-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="965ff-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="965ff-139">-DisableAutoRollback</span></span>
<span data-ttu-id="965ff-140">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="965ff-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="965ff-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="965ff-142">Aktiverar automatisk reparation på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="965ff-143">-EnableUltraSSD</span></span>
<span data-ttu-id="965ff-144">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="965ff-145">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="965ff-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="965ff-146">-EvictionPolicy</span></span>
<span data-ttu-id="965ff-147">Anger avlägsna principer för de virtuella datorerna i skalan.</span><span class="sxs-lookup"><span data-stu-id="965ff-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-148">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="965ff-148">-Extension</span></span>
<span data-ttu-id="965ff-149">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="965ff-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="965ff-150">Du kan använda cmdleten **Add-AzVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="965ff-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="965ff-151">-HealthProbeId</span></span>
<span data-ttu-id="965ff-152">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="965ff-153">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="965ff-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="965ff-154">-IdentityId</span></span>
<span data-ttu-id="965ff-155">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="965ff-156">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="965ff-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="965ff-157">-IdentityType</span></span>
<span data-ttu-id="965ff-158">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="965ff-159">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="965ff-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="965ff-160">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="965ff-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="965ff-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="965ff-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="965ff-162">SystemAssigned</span></span>
- <span data-ttu-id="965ff-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="965ff-163">UserAssigned</span></span>
- <span data-ttu-id="965ff-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="965ff-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="965ff-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="965ff-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="965ff-166">-LicenseType</span></span>
<span data-ttu-id="965ff-167">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="965ff-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-168">-Plats</span><span class="sxs-lookup"><span data-stu-id="965ff-168">-Location</span></span>
<span data-ttu-id="965ff-169">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="965ff-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="965ff-170">-MaxPrice</span></span>
<span data-ttu-id="965ff-171">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="965ff-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="965ff-172">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="965ff-172">This price is in US Dollars.</span></span> <span data-ttu-id="965ff-173">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="965ff-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="965ff-174">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="965ff-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="965ff-175">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="965ff-176">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="965ff-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="965ff-177">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="965ff-177">Example: 0.01538.</span></span>  <span data-ttu-id="965ff-178">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="965ff-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="965ff-179">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="965ff-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="965ff-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="965ff-181">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="965ff-182">Du kan använda cmdleten **Add-AzVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="965ff-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-183">-OsProfile</span></span>
<span data-ttu-id="965ff-184">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="965ff-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="965ff-185">Du kan använda cmdleten **set-AzVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="965ff-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-186">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="965ff-186">-Overprovision</span></span>
<span data-ttu-id="965ff-187">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="965ff-188">-PlanName</span></span>
<span data-ttu-id="965ff-189">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="965ff-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="965ff-190">-PlanProduct</span></span>
<span data-ttu-id="965ff-191">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="965ff-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="965ff-192">-PlanPromotionCode</span></span>
<span data-ttu-id="965ff-193">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="965ff-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="965ff-194">-PlanPublisher</span></span>
<span data-ttu-id="965ff-195">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="965ff-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="965ff-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="965ff-197">Fel domän antal för varje placerings grupp.</span><span class="sxs-lookup"><span data-stu-id="965ff-197">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-198">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="965ff-198">-Priority</span></span>
<span data-ttu-id="965ff-199">Prioriteten för den virtuella machien i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="965ff-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="965ff-200">Endast värden som stöds är "regular", "dekor" och "Low".</span><span class="sxs-lookup"><span data-stu-id="965ff-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="965ff-201">' Regular ' är för vanlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="965ff-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="965ff-202">"Plats" gäller för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="965ff-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="965ff-203">"Low" är också för en virtuell dator, men ersätts med ' dekor ".</span><span class="sxs-lookup"><span data-stu-id="965ff-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="965ff-204">Använd "plats" istället för "Low".</span><span class="sxs-lookup"><span data-stu-id="965ff-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="965ff-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="965ff-206">Resurs-ID för närhets gruppen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="965ff-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="965ff-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="965ff-208">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="965ff-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="965ff-209">-ScaleInPolicy</span></span>
<span data-ttu-id="965ff-210">De regler som ska användas vid skalning-i en virtuell dators skala uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="965ff-211">Möjliga värden är: ' default ', ' OldestVM ' och ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="965ff-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="965ff-212">"Standard" när en skala för virtuell dator skal för änd ras i, fördelas skalnings uppsättningen först över zoner om den är en Zonal skala.</span><span class="sxs-lookup"><span data-stu-id="965ff-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="965ff-213">Då kommer den att bal anse ras i så stor utsträckning som möjligt.</span><span class="sxs-lookup"><span data-stu-id="965ff-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="965ff-214">De virtuella datorerna som valts för borttagning är de nyaste som inte skyddas från Scale-in i varje fel domän.</span><span class="sxs-lookup"><span data-stu-id="965ff-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="965ff-215">' OldestVM ' när en virtuell dators Scale-uppsättning skal för änd ras-in väljs de äldsta virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="965ff-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="965ff-216">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="965ff-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="965ff-217">Inom varje zon kommer de äldsta virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="965ff-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="965ff-218">' NewestVM ' när en virtuell dators skal uppsättning skal för änd ras-in väljs de senaste virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="965ff-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="965ff-219">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="965ff-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="965ff-220">Inom varje zon kommer de senaste virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="965ff-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="965ff-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="965ff-222">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="965ff-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="965ff-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="965ff-224">Anger att tilläggen inte körs på de extra överetablerade datorerna.</span><span class="sxs-lookup"><span data-stu-id="965ff-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="965ff-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="965ff-225">-SkuCapacity</span></span>
<span data-ttu-id="965ff-226">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="965ff-227">-SkuName</span></span>
<span data-ttu-id="965ff-228">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="965ff-229">-SkuTier</span></span>
<span data-ttu-id="965ff-230">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="965ff-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="965ff-231">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="965ff-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="965ff-232">Standar</span><span class="sxs-lookup"><span data-stu-id="965ff-232">Standard</span></span>
- <span data-ttu-id="965ff-233">Basisk</span><span class="sxs-lookup"><span data-stu-id="965ff-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-234">-StorageProfile</span></span>
<span data-ttu-id="965ff-235">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="965ff-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="965ff-236">Du kan använda cmdleten **set-AzVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="965ff-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-237">-Tagg</span><span class="sxs-lookup"><span data-stu-id="965ff-237">-Tag</span></span>
<span data-ttu-id="965ff-238">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="965ff-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="965ff-239">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="965ff-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="965ff-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="965ff-241">Konfigurerbar längd (i minuter) en virtuell dator som tas bort måste eventuellt godkänna händelsen Avsluta schemalagd händelse innan händelsen är automatiskt godkänd (tids gräns).</span><span class="sxs-lookup"><span data-stu-id="965ff-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="965ff-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="965ff-243">Aktivera avsluta schemalagda händelser</span><span class="sxs-lookup"><span data-stu-id="965ff-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="965ff-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="965ff-245">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="965ff-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="965ff-246">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="965ff-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="965ff-247">Versal</span><span class="sxs-lookup"><span data-stu-id="965ff-247">Automatic</span></span>
- <span data-ttu-id="965ff-248">Manövrer</span><span class="sxs-lookup"><span data-stu-id="965ff-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-249">-Zone</span><span class="sxs-lookup"><span data-stu-id="965ff-249">-Zone</span></span>
<span data-ttu-id="965ff-250">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="965ff-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965ff-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="965ff-251">-ZoneBalance</span></span>
<span data-ttu-id="965ff-252">Om du vill tvinga en helt jämn virtuell dator distribution mellan x-zoner om det finns zon avbrott.</span><span class="sxs-lookup"><span data-stu-id="965ff-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="965ff-253">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="965ff-253">-Confirm</span></span>
<span data-ttu-id="965ff-254">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="965ff-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="965ff-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="965ff-255">-WhatIf</span></span>
<span data-ttu-id="965ff-256">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="965ff-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="965ff-257">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="965ff-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="965ff-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965ff-258">CommonParameters</span></span>
<span data-ttu-id="965ff-259">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965ff-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965ff-260">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="965ff-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965ff-261">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="965ff-261">INPUTS</span></span>

### <span data-ttu-id="965ff-262">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="965ff-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="965ff-263">System. String</span><span class="sxs-lookup"><span data-stu-id="965ff-263">System.String</span></span>

### <span data-ttu-id="965ff-264">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="965ff-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="965ff-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="965ff-265">System.Int32</span></span>

### <span data-ttu-id="965ff-266">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="965ff-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="965ff-267">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="965ff-268">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="965ff-269">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="965ff-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="965ff-270">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="965ff-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="965ff-271">System. string []</span><span class="sxs-lookup"><span data-stu-id="965ff-271">System.String[]</span></span>

### <span data-ttu-id="965ff-272">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="965ff-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="965ff-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="965ff-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="965ff-274">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="965ff-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="965ff-275">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="965ff-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="965ff-276">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="965ff-276">OUTPUTS</span></span>

### <span data-ttu-id="965ff-277">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="965ff-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="965ff-278">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="965ff-278">NOTES</span></span>

## <span data-ttu-id="965ff-279">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="965ff-279">RELATED LINKS</span></span>

[<span data-ttu-id="965ff-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="965ff-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="965ff-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="965ff-282">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="965ff-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="965ff-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="965ff-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="965ff-284">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="965ff-284">New-AzVmss</span></span>](./New-AzVmss.md)
