---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925030"
---
# <span data-ttu-id="b4be4-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b4be4-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="b4be4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4be4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4be4-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="b4be4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4be4-104">SYNTAX</span></span>

### <span data-ttu-id="b4be4-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b4be4-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4be4-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4be4-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4be4-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4be4-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4be4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4be4-108">DESCRIPTION</span></span>
<span data-ttu-id="b4be4-109">Cmdleten **New-AzVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="b4be4-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="b4be4-110">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="b4be4-111">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="b4be4-111">These cmdlets are:</span></span>

- <span data-ttu-id="b4be4-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="b4be4-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="b4be4-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4be4-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="b4be4-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b4be4-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="b4be4-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4be4-116">EXAMPLES</span></span>

### <span data-ttu-id="b4be4-117">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="b4be4-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="b4be4-118">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="b4be4-119">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="b4be4-120">I det andra kommandot används cmdleten **New-AzVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="b4be4-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="b4be4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4be4-121">PARAMETERS</span></span>

### <span data-ttu-id="b4be4-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b4be4-122">-AssignIdentity</span></span>
<span data-ttu-id="b4be4-123">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b4be4-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="b4be4-125">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="b4be4-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b4be4-126">-BootDiagnostic</span></span>
<span data-ttu-id="b4be4-127">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="b4be4-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-128">-DefaultProfile</span></span>
<span data-ttu-id="b4be4-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4be4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-130">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="b4be4-130">-Extension</span></span>
<span data-ttu-id="b4be4-131">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="b4be4-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="b4be4-132">Du kan använda cmdleten **Add-AzVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="b4be4-133">-HealthProbeId</span></span>
<span data-ttu-id="b4be4-134">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="b4be4-135">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="b4be4-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="b4be4-136">-IdentityId</span></span>
<span data-ttu-id="b4be4-137">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="b4be4-138">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="b4be4-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b4be4-139">-IdentityType</span></span>
<span data-ttu-id="b4be4-140">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="b4be4-141">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="b4be4-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="b4be4-142">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="b4be4-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b4be4-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4be4-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b4be4-144">SystemAssigned</span></span>
- <span data-ttu-id="b4be4-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="b4be4-145">UserAssigned</span></span>
- <span data-ttu-id="b4be4-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="b4be4-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="b4be4-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4be4-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b4be4-148">-LicenseType</span></span>
<span data-ttu-id="b4be4-149">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="b4be4-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4be4-150">-Location</span></span>
<span data-ttu-id="b4be4-151">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="b4be4-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4be4-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="b4be4-153">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="b4be4-154">Du kan använda cmdleten **Add-AzVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-155">-OsProfile</span></span>
<span data-ttu-id="b4be4-156">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="b4be4-157">Du kan använda cmdleten **set-AzVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="b4be4-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-158">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="b4be4-158">-Overprovision</span></span>
<span data-ttu-id="b4be4-159">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b4be4-160">-PlanName</span></span>
<span data-ttu-id="b4be4-161">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b4be4-162">-PlanProduct</span></span>
<span data-ttu-id="b4be4-163">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="b4be4-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="b4be4-164">-PlanPromotionCode</span></span>
<span data-ttu-id="b4be4-165">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="b4be4-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b4be4-166">-PlanPublisher</span></span>
<span data-ttu-id="b4be4-167">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="b4be4-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-168">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="b4be4-168">-Priority</span></span>
<span data-ttu-id="b4be4-169">Anger prioritet för de virtuella datorerna i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b4be4-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="b4be4-171">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="b4be4-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b4be4-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="b4be4-173">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="b4be4-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b4be4-174">-SkuCapacity</span></span>
<span data-ttu-id="b4be4-175">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4be4-176">-SkuName</span></span>
<span data-ttu-id="b4be4-177">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b4be4-178">-SkuTier</span></span>
<span data-ttu-id="b4be4-179">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="b4be4-180">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b4be4-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4be4-181">Standar</span><span class="sxs-lookup"><span data-stu-id="b4be4-181">Standard</span></span>
- <span data-ttu-id="b4be4-182">Basisk</span><span class="sxs-lookup"><span data-stu-id="b4be4-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-183">-StorageProfile</span></span>
<span data-ttu-id="b4be4-184">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="b4be4-185">Du kan använda cmdleten **set-AzVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="b4be4-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-186">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b4be4-186">-Tag</span></span>
<span data-ttu-id="b4be4-187">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b4be4-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4be4-188">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b4be4-188">For example:</span></span>

<span data-ttu-id="b4be4-189">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b4be4-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b4be4-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="b4be4-191">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="b4be4-192">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b4be4-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4be4-193">Versal</span><span class="sxs-lookup"><span data-stu-id="b4be4-193">Automatic</span></span>
- <span data-ttu-id="b4be4-194">Manövrer</span><span class="sxs-lookup"><span data-stu-id="b4be4-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="b4be4-195">-Zone</span></span>
<span data-ttu-id="b4be4-196">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b4be4-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-197">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4be4-197">-Confirm</span></span>
<span data-ttu-id="b4be4-198">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4be4-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4be4-199">-WhatIf</span></span>
<span data-ttu-id="b4be4-200">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4be4-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4be4-201">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4be4-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be4-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4be4-202">CommonParameters</span></span>
<span data-ttu-id="b4be4-203">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4be4-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4be4-204">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4be4-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4be4-205">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4be4-205">INPUTS</span></span>

### <span data-ttu-id="b4be4-206">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4be4-206">None</span></span>
<span data-ttu-id="b4be4-207">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b4be4-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4be4-208">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4be4-208">OUTPUTS</span></span>

### <span data-ttu-id="b4be4-209">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4be4-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4be4-210">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4be4-210">NOTES</span></span>

## <span data-ttu-id="b4be4-211">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4be4-211">RELATED LINKS</span></span>

[<span data-ttu-id="b4be4-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="b4be4-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b4be4-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="b4be4-214">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4be4-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="b4be4-215">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b4be4-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b4be4-216">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b4be4-216">New-AzVmss</span></span>](./New-AzVmss.md)
