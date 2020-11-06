---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575282"
---
# <span data-ttu-id="9276f-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9276f-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="9276f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9276f-102">SYNOPSIS</span></span>
<span data-ttu-id="9276f-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9276f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9276f-104">SYNTAX</span></span>

### <span data-ttu-id="9276f-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9276f-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9276f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
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

### <span data-ttu-id="9276f-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276f-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9276f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9276f-108">DESCRIPTION</span></span>
<span data-ttu-id="9276f-109">Cmdleten **New-AzureRmVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="9276f-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="9276f-110">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="9276f-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="9276f-111">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="9276f-111">These cmdlets are:</span></span>
- <span data-ttu-id="9276f-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="9276f-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="9276f-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9276f-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="9276f-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9276f-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="9276f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9276f-116">EXAMPLES</span></span>

### <span data-ttu-id="9276f-117">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="9276f-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="9276f-118">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="9276f-119">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="9276f-120">I det andra kommandot används cmdleten **New-AzureRmVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="9276f-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="9276f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9276f-121">PARAMETERS</span></span>

### <span data-ttu-id="9276f-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9276f-122">-AssignIdentity</span></span>
<span data-ttu-id="9276f-123">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9276f-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="9276f-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="9276f-125">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="9276f-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="9276f-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9276f-126">-BootDiagnostic</span></span>
<span data-ttu-id="9276f-127">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="9276f-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="9276f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-128">-DefaultProfile</span></span>
<span data-ttu-id="9276f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9276f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276f-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="9276f-130">-DisableAutoRollback</span></span>
<span data-ttu-id="9276f-131">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="9276f-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="9276f-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="9276f-132">-EnableUltraSSD</span></span>
<span data-ttu-id="9276f-133">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="9276f-134">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="9276f-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="9276f-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="9276f-135">-EvictionPolicy</span></span>
<span data-ttu-id="9276f-136">Anger avlägsna principer för de virtuella datorerna i skalan.</span><span class="sxs-lookup"><span data-stu-id="9276f-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="9276f-137">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="9276f-137">-Extension</span></span>
<span data-ttu-id="9276f-138">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="9276f-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="9276f-139">Du kan använda cmdleten **Add-AzureRmVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="9276f-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="9276f-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="9276f-140">-HealthProbeId</span></span>
<span data-ttu-id="9276f-141">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="9276f-142">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="9276f-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="9276f-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9276f-143">-IdentityId</span></span>
<span data-ttu-id="9276f-144">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9276f-145">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="9276f-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="9276f-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9276f-146">-IdentityType</span></span>
<span data-ttu-id="9276f-147">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="9276f-148">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="9276f-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="9276f-149">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="9276f-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9276f-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9276f-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="9276f-151">SystemAssigned</span></span>
- <span data-ttu-id="9276f-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="9276f-152">UserAssigned</span></span>
- <span data-ttu-id="9276f-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="9276f-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="9276f-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="9276f-154">None</span></span>

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

### <span data-ttu-id="9276f-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9276f-155">-LicenseType</span></span>
<span data-ttu-id="9276f-156">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="9276f-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="9276f-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="9276f-157">-Location</span></span>
<span data-ttu-id="9276f-158">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="9276f-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="9276f-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9276f-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="9276f-160">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="9276f-161">Du kan använda cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="9276f-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="9276f-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-162">-OsProfile</span></span>
<span data-ttu-id="9276f-163">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9276f-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="9276f-164">Du kan använda cmdleten **set-AzureRmVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="9276f-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="9276f-165">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="9276f-165">-Overprovision</span></span>
<span data-ttu-id="9276f-166">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="9276f-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9276f-167">-PlanName</span></span>
<span data-ttu-id="9276f-168">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="9276f-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="9276f-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="9276f-169">-PlanProduct</span></span>
<span data-ttu-id="9276f-170">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="9276f-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="9276f-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="9276f-171">-PlanPromotionCode</span></span>
<span data-ttu-id="9276f-172">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="9276f-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="9276f-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9276f-173">-PlanPublisher</span></span>
<span data-ttu-id="9276f-174">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="9276f-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="9276f-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="9276f-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="9276f-176">Fel domän antal för varje placerings grupp.</span><span class="sxs-lookup"><span data-stu-id="9276f-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="9276f-177">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="9276f-177">-Priority</span></span>
<span data-ttu-id="9276f-178">Anger prioritet för de virtuella datorerna i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="9276f-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="9276f-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="9276f-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="9276f-180">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="9276f-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="9276f-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9276f-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="9276f-182">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="9276f-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="9276f-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9276f-183">-SkuCapacity</span></span>
<span data-ttu-id="9276f-184">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="9276f-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9276f-185">-SkuName</span></span>
<span data-ttu-id="9276f-186">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="9276f-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9276f-187">-SkuTier</span></span>
<span data-ttu-id="9276f-188">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="9276f-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="9276f-189">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9276f-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9276f-190">Standar</span><span class="sxs-lookup"><span data-stu-id="9276f-190">Standard</span></span>
- <span data-ttu-id="9276f-191">Basisk</span><span class="sxs-lookup"><span data-stu-id="9276f-191">Basic</span></span>

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

### <span data-ttu-id="9276f-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-192">-StorageProfile</span></span>
<span data-ttu-id="9276f-193">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9276f-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="9276f-194">Du kan använda cmdleten **set-AzureRmVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="9276f-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="9276f-195">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9276f-195">-Tag</span></span>
<span data-ttu-id="9276f-196">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9276f-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9276f-197">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9276f-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9276f-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="9276f-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="9276f-199">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="9276f-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="9276f-200">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9276f-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9276f-201">Versal</span><span class="sxs-lookup"><span data-stu-id="9276f-201">Automatic</span></span>
- <span data-ttu-id="9276f-202">Manövrer</span><span class="sxs-lookup"><span data-stu-id="9276f-202">Manual</span></span>

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

### <span data-ttu-id="9276f-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="9276f-203">-Zone</span></span>
<span data-ttu-id="9276f-204">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9276f-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9276f-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="9276f-205">-ZoneBalance</span></span>
<span data-ttu-id="9276f-206">Om du vill tvinga en helt jämn virtuell dator distribution mellan x-zoner om det finns zon avbrott.</span><span class="sxs-lookup"><span data-stu-id="9276f-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="9276f-207">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9276f-207">-Confirm</span></span>
<span data-ttu-id="9276f-208">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9276f-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9276f-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9276f-209">-WhatIf</span></span>
<span data-ttu-id="9276f-210">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9276f-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9276f-211">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9276f-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9276f-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9276f-212">CommonParameters</span></span>
<span data-ttu-id="9276f-213">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9276f-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9276f-214">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9276f-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9276f-215">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9276f-215">INPUTS</span></span>

### <span data-ttu-id="9276f-216">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9276f-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9276f-217">System. String</span><span class="sxs-lookup"><span data-stu-id="9276f-217">System.String</span></span>

### <span data-ttu-id="9276f-218">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9276f-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9276f-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9276f-219">System.Int32</span></span>

### <span data-ttu-id="9276f-220">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9276f-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9276f-221">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="9276f-222">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="9276f-223">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9276f-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="9276f-224">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="9276f-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="9276f-225">System. string []</span><span class="sxs-lookup"><span data-stu-id="9276f-225">System.String[]</span></span>

### <span data-ttu-id="9276f-226">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="9276f-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="9276f-227">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9276f-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="9276f-228">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9276f-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="9276f-229">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9276f-229">OUTPUTS</span></span>

### <span data-ttu-id="9276f-230">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9276f-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9276f-231">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9276f-231">NOTES</span></span>

## <span data-ttu-id="9276f-232">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9276f-232">RELATED LINKS</span></span>

[<span data-ttu-id="9276f-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="9276f-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="9276f-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="9276f-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9276f-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="9276f-236">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9276f-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="9276f-237">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9276f-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
