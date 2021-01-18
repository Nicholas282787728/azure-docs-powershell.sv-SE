---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520272"
---
# <span data-ttu-id="32b24-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="32b24-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="32b24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32b24-102">SYNOPSIS</span></span>
<span data-ttu-id="32b24-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="32b24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32b24-104">SYNTAX</span></span>

### <span data-ttu-id="32b24-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="32b24-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b24-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="32b24-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32b24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32b24-107">DESCRIPTION</span></span>
<span data-ttu-id="32b24-108">Cmdleten **New-AzVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="32b24-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="32b24-109">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="32b24-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="32b24-110">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="32b24-110">These cmdlets are:</span></span>
- <span data-ttu-id="32b24-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="32b24-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="32b24-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="32b24-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="32b24-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="32b24-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="32b24-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32b24-115">EXAMPLES</span></span>

### <span data-ttu-id="32b24-116">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="32b24-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="32b24-117">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="32b24-118">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="32b24-119">I det andra kommandot används cmdleten **New-AzVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="32b24-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="32b24-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="32b24-120">Example 2</span></span>

<span data-ttu-id="32b24-121">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="32b24-122">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="32b24-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="32b24-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32b24-123">PARAMETERS</span></span>

### <span data-ttu-id="32b24-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="32b24-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="32b24-125">Den tid som automatiska reparationer har upphävts på grund av en tillstånds ändring på VM.</span><span class="sxs-lookup"><span data-stu-id="32b24-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="32b24-126">Grace-tiden inleds efter att statusen har ändrats.</span><span class="sxs-lookup"><span data-stu-id="32b24-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="32b24-127">Detta gör att du kan undvika för tidigt eller oavsiktlig reparation.</span><span class="sxs-lookup"><span data-stu-id="32b24-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="32b24-128">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="32b24-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="32b24-129">Den minsta tillåtna respitperioden är 30 minuter (PT30M), vilket också är standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="32b24-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="32b24-130">Den maximala respitperioden är 90 minuter (PT90M).</span><span class="sxs-lookup"><span data-stu-id="32b24-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="32b24-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="32b24-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="32b24-132">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="32b24-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="32b24-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="32b24-133">-BootDiagnostic</span></span>
<span data-ttu-id="32b24-134">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="32b24-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="32b24-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-135">-DefaultProfile</span></span>
<span data-ttu-id="32b24-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32b24-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32b24-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="32b24-137">-DisableAutoRollback</span></span>
<span data-ttu-id="32b24-138">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="32b24-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="32b24-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="32b24-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="32b24-140">Aktiverar automatisk reparation på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="32b24-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="32b24-141">-EnableUltraSSD</span></span>
<span data-ttu-id="32b24-142">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="32b24-143">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="32b24-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="32b24-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="32b24-144">-EncryptionAtHost</span></span>
<span data-ttu-id="32b24-145">Med den här parametern aktive ras kryptering för alla diskar, inklusive resurs/Temp-disk på själva värden.</span><span class="sxs-lookup"><span data-stu-id="32b24-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="32b24-146">Standard: krypteringen på värden kommer att inaktive ras såvida den inte är inställd på True för resursen.</span><span class="sxs-lookup"><span data-stu-id="32b24-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="32b24-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="32b24-147">-EvictionPolicy</span></span>
<span data-ttu-id="32b24-148">Anger avlägsna principer för de virtuella datorerna i skalan.</span><span class="sxs-lookup"><span data-stu-id="32b24-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="32b24-149">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="32b24-149">-Extension</span></span>
<span data-ttu-id="32b24-150">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="32b24-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="32b24-151">Du kan använda cmdleten **Add-AzVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="32b24-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="32b24-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="32b24-152">-HealthProbeId</span></span>
<span data-ttu-id="32b24-153">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="32b24-154">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="32b24-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="32b24-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="32b24-155">-IdentityId</span></span>
<span data-ttu-id="32b24-156">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="32b24-157">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="32b24-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="32b24-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="32b24-158">-IdentityType</span></span>
<span data-ttu-id="32b24-159">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="32b24-160">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="32b24-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="32b24-161">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="32b24-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="32b24-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32b24-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="32b24-163">SystemAssigned</span></span>
- <span data-ttu-id="32b24-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="32b24-164">UserAssigned</span></span>
- <span data-ttu-id="32b24-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="32b24-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="32b24-166">Ingen</span><span class="sxs-lookup"><span data-stu-id="32b24-166">None</span></span>

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

### <span data-ttu-id="32b24-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="32b24-167">-LicenseType</span></span>
<span data-ttu-id="32b24-168">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="32b24-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="32b24-169">-Plats</span><span class="sxs-lookup"><span data-stu-id="32b24-169">-Location</span></span>
<span data-ttu-id="32b24-170">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="32b24-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="32b24-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="32b24-171">-MaxPrice</span></span>
<span data-ttu-id="32b24-172">Anger det högsta priset du är villig att betala för en dator/VMSS med punkter.</span><span class="sxs-lookup"><span data-stu-id="32b24-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="32b24-173">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="32b24-173">This price is in US Dollars.</span></span> <span data-ttu-id="32b24-174">Det här priset jämförs med det aktuella priset för den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="32b24-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="32b24-175">Priserna jämförs också med tiden för att skapa eller uppdatera en VM-VMSS och åtgärden fungerar bara om maxPrice är större än det aktuella priset.</span><span class="sxs-lookup"><span data-stu-id="32b24-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="32b24-176">MaxPrice används också för att avlägsna en dator/VMSS med punkter om det nuvarande priset går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="32b24-177">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="32b24-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="32b24-178">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="32b24-178">Example: 0.01538.</span></span>  <span data-ttu-id="32b24-179">-1 anger att den virtuella dator-VMSS inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="32b24-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="32b24-180">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="32b24-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="32b24-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="32b24-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="32b24-182">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="32b24-183">Du kan använda cmdleten **Add-AzVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="32b24-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="32b24-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-184">-OsProfile</span></span>
<span data-ttu-id="32b24-185">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="32b24-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="32b24-186">Du kan använda cmdleten **set-AzVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="32b24-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="32b24-187">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="32b24-187">-Overprovision</span></span>
<span data-ttu-id="32b24-188">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="32b24-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="32b24-189">-PlanName</span></span>
<span data-ttu-id="32b24-190">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="32b24-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="32b24-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="32b24-191">-PlanProduct</span></span>
<span data-ttu-id="32b24-192">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="32b24-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="32b24-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="32b24-193">-PlanPromotionCode</span></span>
<span data-ttu-id="32b24-194">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="32b24-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="32b24-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="32b24-195">-PlanPublisher</span></span>
<span data-ttu-id="32b24-196">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="32b24-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="32b24-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="32b24-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="32b24-198">Fel domän antal för varje placerings grupp.</span><span class="sxs-lookup"><span data-stu-id="32b24-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="32b24-199">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="32b24-199">-Priority</span></span>
<span data-ttu-id="32b24-200">Prioriteten för den virtuella machien i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="32b24-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="32b24-201">Endast värden som stöds är "regular", "dekor" och "Low".</span><span class="sxs-lookup"><span data-stu-id="32b24-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="32b24-202">' Regular ' är för vanlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="32b24-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="32b24-203">"Plats" gäller för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="32b24-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="32b24-204">"Low" är också för en virtuell dator, men ersätts med ' dekor ".</span><span class="sxs-lookup"><span data-stu-id="32b24-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="32b24-205">Använd "plats" istället för "Low".</span><span class="sxs-lookup"><span data-stu-id="32b24-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="32b24-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="32b24-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="32b24-207">Resurs-ID för närhets gruppen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="32b24-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="32b24-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="32b24-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="32b24-209">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="32b24-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="32b24-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="32b24-210">-ScaleInPolicy</span></span>
<span data-ttu-id="32b24-211">De regler som ska användas vid skalning-i en virtuell dators skala uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="32b24-212">Möjliga värden är: ' default ', ' OldestVM ' och ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="32b24-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="32b24-213">"Standard" när en skala för virtuell dator skal för änd ras i, fördelas skalnings uppsättningen först över zoner om den är en Zonal skala.</span><span class="sxs-lookup"><span data-stu-id="32b24-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="32b24-214">Då kommer den att bal anse ras i så stor utsträckning som möjligt.</span><span class="sxs-lookup"><span data-stu-id="32b24-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="32b24-215">De virtuella datorerna som valts för borttagning är de nyaste som inte skyddas från Scale-in i varje fel domän.</span><span class="sxs-lookup"><span data-stu-id="32b24-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="32b24-216">' OldestVM ' när en virtuell dators Scale-uppsättning skal för änd ras-in väljs de äldsta virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="32b24-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="32b24-217">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="32b24-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="32b24-218">Inom varje zon kommer de äldsta virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="32b24-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="32b24-219">' NewestVM ' när en virtuell dators skal uppsättning skal för änd ras-in väljs de senaste virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="32b24-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="32b24-220">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="32b24-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="32b24-221">Inom varje zon kommer de senaste virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="32b24-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="32b24-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="32b24-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="32b24-223">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="32b24-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="32b24-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="32b24-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="32b24-225">Anger att tilläggen inte körs på de extra överetablerade datorerna.</span><span class="sxs-lookup"><span data-stu-id="32b24-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="32b24-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="32b24-226">-SkuCapacity</span></span>
<span data-ttu-id="32b24-227">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="32b24-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="32b24-228">-SkuName</span></span>
<span data-ttu-id="32b24-229">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="32b24-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="32b24-230">-SkuTier</span></span>
<span data-ttu-id="32b24-231">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="32b24-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="32b24-232">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="32b24-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32b24-233">Standar</span><span class="sxs-lookup"><span data-stu-id="32b24-233">Standard</span></span>
- <span data-ttu-id="32b24-234">Basisk</span><span class="sxs-lookup"><span data-stu-id="32b24-234">Basic</span></span>

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

### <span data-ttu-id="32b24-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-235">-StorageProfile</span></span>
<span data-ttu-id="32b24-236">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="32b24-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="32b24-237">Du kan använda cmdleten **set-AzVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="32b24-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="32b24-238">-Tagg</span><span class="sxs-lookup"><span data-stu-id="32b24-238">-Tag</span></span>
<span data-ttu-id="32b24-239">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="32b24-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32b24-240">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="32b24-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="32b24-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="32b24-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="32b24-242">Konfigurerbar längd (i minuter) en virtuell dator som tas bort måste eventuellt godkänna händelsen Avsluta schemalagd händelse innan händelsen är automatiskt godkänd (tids gräns).</span><span class="sxs-lookup"><span data-stu-id="32b24-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="32b24-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="32b24-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="32b24-244">Aktivera avsluta schemalagda händelser</span><span class="sxs-lookup"><span data-stu-id="32b24-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="32b24-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="32b24-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="32b24-246">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="32b24-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="32b24-247">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="32b24-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32b24-248">Versal</span><span class="sxs-lookup"><span data-stu-id="32b24-248">Automatic</span></span>
- <span data-ttu-id="32b24-249">Manövrer</span><span class="sxs-lookup"><span data-stu-id="32b24-249">Manual</span></span>

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

### <span data-ttu-id="32b24-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="32b24-250">-Zone</span></span>
<span data-ttu-id="32b24-251">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="32b24-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="32b24-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="32b24-252">-ZoneBalance</span></span>
<span data-ttu-id="32b24-253">Om du vill tvinga en helt jämn virtuell dator distribution mellan x-zoner om det finns zon avbrott.</span><span class="sxs-lookup"><span data-stu-id="32b24-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="32b24-254">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32b24-254">-Confirm</span></span>
<span data-ttu-id="32b24-255">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32b24-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b24-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b24-256">-WhatIf</span></span>
<span data-ttu-id="32b24-257">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32b24-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32b24-258">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32b24-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b24-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b24-259">CommonParameters</span></span>
<span data-ttu-id="32b24-260">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b24-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b24-261">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32b24-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b24-262">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32b24-262">INPUTS</span></span>

### <span data-ttu-id="32b24-263">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32b24-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32b24-264">System. String</span><span class="sxs-lookup"><span data-stu-id="32b24-264">System.String</span></span>

### <span data-ttu-id="32b24-265">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="32b24-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="32b24-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="32b24-266">System.Int32</span></span>

### <span data-ttu-id="32b24-267">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="32b24-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="32b24-268">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="32b24-269">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="32b24-270">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="32b24-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="32b24-271">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="32b24-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="32b24-272">System. string []</span><span class="sxs-lookup"><span data-stu-id="32b24-272">System.String[]</span></span>

### <span data-ttu-id="32b24-273">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="32b24-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="32b24-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32b24-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="32b24-275">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="32b24-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="32b24-276">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="32b24-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="32b24-277">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32b24-277">OUTPUTS</span></span>

### <span data-ttu-id="32b24-278">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32b24-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="32b24-279">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32b24-279">NOTES</span></span>

## <span data-ttu-id="32b24-280">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32b24-280">RELATED LINKS</span></span>

[<span data-ttu-id="32b24-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="32b24-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="32b24-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="32b24-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="32b24-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="32b24-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="32b24-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="32b24-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="32b24-285">New-AzVmss</span></span>](./New-AzVmss.md)
