---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930697"
---
# <span data-ttu-id="16ae8-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="16ae8-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="16ae8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="16ae8-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ae8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ae8-104">SYNTAX</span></span>

### <span data-ttu-id="16ae8-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="16ae8-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ae8-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ae8-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
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

### <span data-ttu-id="16ae8-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ae8-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ae8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ae8-108">DESCRIPTION</span></span>
<span data-ttu-id="16ae8-109">Cmdleten **New-AzureRmVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="16ae8-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="16ae8-110">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="16ae8-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="16ae8-111">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="16ae8-111">These cmdlets are:</span></span>

- <span data-ttu-id="16ae8-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="16ae8-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="16ae8-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ae8-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="16ae8-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="16ae8-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="16ae8-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ae8-116">EXAMPLES</span></span>

### <span data-ttu-id="16ae8-117">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="16ae8-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="16ae8-118">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="16ae8-119">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="16ae8-120">I det andra kommandot används cmdleten **New-AzureRmVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="16ae8-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="16ae8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ae8-121">PARAMETERS</span></span>

### <span data-ttu-id="16ae8-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="16ae8-122">-AssignIdentity</span></span>
<span data-ttu-id="16ae8-123">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="16ae8-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="16ae8-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="16ae8-125">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="16ae8-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="16ae8-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="16ae8-126">-BootDiagnostic</span></span>
<span data-ttu-id="16ae8-127">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="16ae8-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="16ae8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-128">-DefaultProfile</span></span>
<span data-ttu-id="16ae8-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16ae8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ae8-130">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="16ae8-130">-Extension</span></span>
<span data-ttu-id="16ae8-131">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="16ae8-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="16ae8-132">Du kan använda cmdleten **Add-AzureRmVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="16ae8-132">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="16ae8-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="16ae8-133">-HealthProbeId</span></span>
<span data-ttu-id="16ae8-134">Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="16ae8-135">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="16ae8-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="16ae8-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="16ae8-136">-IdentityId</span></span>
<span data-ttu-id="16ae8-137">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="16ae8-138">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="16ae8-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="16ae8-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="16ae8-139">-IdentityType</span></span>
<span data-ttu-id="16ae8-140">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="16ae8-141">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="16ae8-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="16ae8-142">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="16ae8-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="16ae8-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16ae8-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="16ae8-144">SystemAssigned</span></span>
- <span data-ttu-id="16ae8-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="16ae8-145">UserAssigned</span></span>
- <span data-ttu-id="16ae8-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="16ae8-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="16ae8-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="16ae8-147">None</span></span>

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

### <span data-ttu-id="16ae8-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="16ae8-148">-LicenseType</span></span>
<span data-ttu-id="16ae8-149">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="16ae8-149">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="16ae8-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="16ae8-150">-Location</span></span>
<span data-ttu-id="16ae8-151">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="16ae8-151">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="16ae8-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ae8-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="16ae8-153">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="16ae8-154">Du kan använda cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="16ae8-154">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="16ae8-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-155">-OsProfile</span></span>
<span data-ttu-id="16ae8-156">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="16ae8-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="16ae8-157">Du kan använda cmdleten **set-AzureRmVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="16ae8-157">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="16ae8-158">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="16ae8-158">-Overprovision</span></span>
<span data-ttu-id="16ae8-159">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="16ae8-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="16ae8-160">-PlanName</span></span>
<span data-ttu-id="16ae8-161">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="16ae8-161">Specifies the plan name.</span></span>

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

### <span data-ttu-id="16ae8-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="16ae8-162">-PlanProduct</span></span>
<span data-ttu-id="16ae8-163">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="16ae8-163">Specifies the plan product.</span></span>

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

### <span data-ttu-id="16ae8-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="16ae8-164">-PlanPromotionCode</span></span>
<span data-ttu-id="16ae8-165">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="16ae8-165">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="16ae8-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="16ae8-166">-PlanPublisher</span></span>
<span data-ttu-id="16ae8-167">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="16ae8-167">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="16ae8-168">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="16ae8-168">-Priority</span></span>
<span data-ttu-id="16ae8-169">Anger prioritet för de virtuella datorerna i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="16ae8-169">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="16ae8-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="16ae8-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="16ae8-171">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="16ae8-171">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="16ae8-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="16ae8-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="16ae8-173">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="16ae8-173">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="16ae8-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="16ae8-174">-SkuCapacity</span></span>
<span data-ttu-id="16ae8-175">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-175">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="16ae8-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="16ae8-176">-SkuName</span></span>
<span data-ttu-id="16ae8-177">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-177">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="16ae8-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="16ae8-178">-SkuTier</span></span>
<span data-ttu-id="16ae8-179">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ae8-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="16ae8-180">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="16ae8-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16ae8-181">Standar</span><span class="sxs-lookup"><span data-stu-id="16ae8-181">Standard</span></span>
- <span data-ttu-id="16ae8-182">Basisk</span><span class="sxs-lookup"><span data-stu-id="16ae8-182">Basic</span></span>

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

### <span data-ttu-id="16ae8-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-183">-StorageProfile</span></span>
<span data-ttu-id="16ae8-184">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="16ae8-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="16ae8-185">Du kan använda cmdleten **set-AzureRmVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="16ae8-185">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="16ae8-186">-Tagg</span><span class="sxs-lookup"><span data-stu-id="16ae8-186">-Tag</span></span>
<span data-ttu-id="16ae8-187">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="16ae8-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="16ae8-188">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="16ae8-188">For example:</span></span>

<span data-ttu-id="16ae8-189">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="16ae8-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="16ae8-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="16ae8-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="16ae8-191">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="16ae8-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="16ae8-192">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="16ae8-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16ae8-193">Versal</span><span class="sxs-lookup"><span data-stu-id="16ae8-193">Automatic</span></span>
- <span data-ttu-id="16ae8-194">Manövrer</span><span class="sxs-lookup"><span data-stu-id="16ae8-194">Manual</span></span>

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

### <span data-ttu-id="16ae8-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="16ae8-195">-Zone</span></span>
<span data-ttu-id="16ae8-196">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="16ae8-196">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="16ae8-197">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16ae8-197">-Confirm</span></span>
<span data-ttu-id="16ae8-198">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16ae8-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ae8-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ae8-199">-WhatIf</span></span>
<span data-ttu-id="16ae8-200">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16ae8-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16ae8-201">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16ae8-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ae8-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ae8-202">CommonParameters</span></span>
<span data-ttu-id="16ae8-203">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ae8-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ae8-204">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ae8-204">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ae8-205">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ae8-205">INPUTS</span></span>

### <span data-ttu-id="16ae8-206">Ingen</span><span class="sxs-lookup"><span data-stu-id="16ae8-206">None</span></span>
<span data-ttu-id="16ae8-207">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="16ae8-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16ae8-208">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ae8-208">OUTPUTS</span></span>

### <span data-ttu-id="16ae8-209">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="16ae8-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="16ae8-210">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ae8-210">NOTES</span></span>

## <span data-ttu-id="16ae8-211">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ae8-211">RELATED LINKS</span></span>

[<span data-ttu-id="16ae8-212">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-212">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="16ae8-213">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="16ae8-213">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="16ae8-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ae8-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="16ae8-215">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="16ae8-215">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="16ae8-216">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ae8-216">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
