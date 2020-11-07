---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754529"
---
# <span data-ttu-id="58b2d-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="58b2d-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="58b2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="58b2d-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="58b2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58b2d-104">SYNTAX</span></span>

### <span data-ttu-id="58b2d-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58b2d-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b2d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="58b2d-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b2d-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="58b2d-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b2d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58b2d-108">DESCRIPTION</span></span>
<span data-ttu-id="58b2d-109">Cmdleten **New-AzVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="58b2d-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="58b2d-110">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="58b2d-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="58b2d-111">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="58b2d-111">These cmdlets are:</span></span>
- <span data-ttu-id="58b2d-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="58b2d-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="58b2d-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="58b2d-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="58b2d-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="58b2d-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="58b2d-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58b2d-116">EXAMPLES</span></span>

### <span data-ttu-id="58b2d-117">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="58b2d-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="58b2d-118">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="58b2d-119">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="58b2d-120">I det andra kommandot används cmdleten **New-AzVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="58b2d-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="58b2d-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58b2d-121">PARAMETERS</span></span>

### <span data-ttu-id="58b2d-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="58b2d-122">-AssignIdentity</span></span>
<span data-ttu-id="58b2d-123">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="58b2d-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="58b2d-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="58b2d-125">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="58b2d-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="58b2d-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="58b2d-126">-BootDiagnostic</span></span>
<span data-ttu-id="58b2d-127">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="58b2d-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="58b2d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-128">-DefaultProfile</span></span>
<span data-ttu-id="58b2d-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58b2d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b2d-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="58b2d-130">-DisableAutoRollback</span></span>
<span data-ttu-id="58b2d-131">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="58b2d-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="58b2d-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="58b2d-132">-EnableUltraSSD</span></span>
<span data-ttu-id="58b2d-133">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="58b2d-134">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="58b2d-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="58b2d-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="58b2d-135">-EvictionPolicy</span></span>
<span data-ttu-id="58b2d-136">Anger avlägsna principer för de virtuella datorerna i skalan.</span><span class="sxs-lookup"><span data-stu-id="58b2d-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="58b2d-137">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="58b2d-137">-Extension</span></span>
<span data-ttu-id="58b2d-138">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="58b2d-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="58b2d-139">Du kan använda cmdleten **Add-AzVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="58b2d-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="58b2d-140">-HealthProbeId</span></span>
<span data-ttu-id="58b2d-141">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="58b2d-142">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="58b2d-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="58b2d-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="58b2d-143">-IdentityId</span></span>
<span data-ttu-id="58b2d-144">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="58b2d-145">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="58b2d-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="58b2d-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="58b2d-146">-IdentityType</span></span>
<span data-ttu-id="58b2d-147">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="58b2d-148">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="58b2d-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="58b2d-149">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="58b2d-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="58b2d-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58b2d-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="58b2d-151">SystemAssigned</span></span>
- <span data-ttu-id="58b2d-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="58b2d-152">UserAssigned</span></span>
- <span data-ttu-id="58b2d-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="58b2d-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="58b2d-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="58b2d-154">None</span></span>

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

### <span data-ttu-id="58b2d-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="58b2d-155">-LicenseType</span></span>
<span data-ttu-id="58b2d-156">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="58b2d-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="58b2d-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="58b2d-157">-Location</span></span>
<span data-ttu-id="58b2d-158">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="58b2d-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="58b2d-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="58b2d-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="58b2d-160">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="58b2d-161">Du kan använda cmdleten **Add-AzVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="58b2d-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="58b2d-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-162">-OsProfile</span></span>
<span data-ttu-id="58b2d-163">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="58b2d-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="58b2d-164">Du kan använda cmdleten **set-AzVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="58b2d-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="58b2d-165">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="58b2d-165">-Overprovision</span></span>
<span data-ttu-id="58b2d-166">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="58b2d-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="58b2d-167">-PlanName</span></span>
<span data-ttu-id="58b2d-168">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="58b2d-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="58b2d-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="58b2d-169">-PlanProduct</span></span>
<span data-ttu-id="58b2d-170">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="58b2d-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="58b2d-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="58b2d-171">-PlanPromotionCode</span></span>
<span data-ttu-id="58b2d-172">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="58b2d-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="58b2d-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="58b2d-173">-PlanPublisher</span></span>
<span data-ttu-id="58b2d-174">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="58b2d-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="58b2d-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="58b2d-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="58b2d-176">Fel domän antal för varje placerings grupp.</span><span class="sxs-lookup"><span data-stu-id="58b2d-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="58b2d-177">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="58b2d-177">-Priority</span></span>
<span data-ttu-id="58b2d-178">Anger prioritet för de virtuella datorerna i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="58b2d-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="58b2d-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="58b2d-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="58b2d-180">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="58b2d-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="58b2d-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="58b2d-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="58b2d-182">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="58b2d-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="58b2d-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="58b2d-183">-SkuCapacity</span></span>
<span data-ttu-id="58b2d-184">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="58b2d-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58b2d-185">-SkuName</span></span>
<span data-ttu-id="58b2d-186">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="58b2d-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="58b2d-187">-SkuTier</span></span>
<span data-ttu-id="58b2d-188">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="58b2d-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="58b2d-189">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="58b2d-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58b2d-190">Standar</span><span class="sxs-lookup"><span data-stu-id="58b2d-190">Standard</span></span>
- <span data-ttu-id="58b2d-191">Basisk</span><span class="sxs-lookup"><span data-stu-id="58b2d-191">Basic</span></span>

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

### <span data-ttu-id="58b2d-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-192">-StorageProfile</span></span>
<span data-ttu-id="58b2d-193">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="58b2d-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="58b2d-194">Du kan använda cmdleten **set-AzVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="58b2d-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="58b2d-195">-Tagg</span><span class="sxs-lookup"><span data-stu-id="58b2d-195">-Tag</span></span>
<span data-ttu-id="58b2d-196">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="58b2d-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58b2d-197">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="58b2d-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58b2d-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="58b2d-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="58b2d-199">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="58b2d-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="58b2d-200">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="58b2d-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58b2d-201">Versal</span><span class="sxs-lookup"><span data-stu-id="58b2d-201">Automatic</span></span>
- <span data-ttu-id="58b2d-202">Manövrer</span><span class="sxs-lookup"><span data-stu-id="58b2d-202">Manual</span></span>

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

### <span data-ttu-id="58b2d-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="58b2d-203">-Zone</span></span>
<span data-ttu-id="58b2d-204">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="58b2d-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="58b2d-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="58b2d-205">-ZoneBalance</span></span>
<span data-ttu-id="58b2d-206">Om du vill tvinga en helt jämn virtuell dator distribution mellan x-zoner om det finns zon avbrott.</span><span class="sxs-lookup"><span data-stu-id="58b2d-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="58b2d-207">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58b2d-207">-Confirm</span></span>
<span data-ttu-id="58b2d-208">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58b2d-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b2d-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b2d-209">-WhatIf</span></span>
<span data-ttu-id="58b2d-210">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58b2d-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58b2d-211">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58b2d-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b2d-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b2d-212">CommonParameters</span></span>
<span data-ttu-id="58b2d-213">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b2d-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b2d-214">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b2d-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b2d-215">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58b2d-215">INPUTS</span></span>

### <span data-ttu-id="58b2d-216">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58b2d-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58b2d-217">System. String</span><span class="sxs-lookup"><span data-stu-id="58b2d-217">System.String</span></span>

### <span data-ttu-id="58b2d-218">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="58b2d-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58b2d-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="58b2d-219">System.Int32</span></span>

### <span data-ttu-id="58b2d-220">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="58b2d-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="58b2d-221">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="58b2d-222">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="58b2d-223">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="58b2d-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="58b2d-224">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="58b2d-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="58b2d-225">System. string []</span><span class="sxs-lookup"><span data-stu-id="58b2d-225">System.String[]</span></span>

### <span data-ttu-id="58b2d-226">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="58b2d-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="58b2d-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58b2d-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="58b2d-228">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="58b2d-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="58b2d-229">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="58b2d-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="58b2d-230">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58b2d-230">OUTPUTS</span></span>

### <span data-ttu-id="58b2d-231">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="58b2d-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="58b2d-232">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58b2d-232">NOTES</span></span>

## <span data-ttu-id="58b2d-233">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58b2d-233">RELATED LINKS</span></span>

[<span data-ttu-id="58b2d-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="58b2d-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="58b2d-236">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="58b2d-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="58b2d-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="58b2d-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="58b2d-238">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="58b2d-238">New-AzVmss</span></span>](./New-AzVmss.md)
