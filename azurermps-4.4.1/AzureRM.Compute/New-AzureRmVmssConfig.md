---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757802"
---
# <span data-ttu-id="c0d07-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c0d07-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="c0d07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0d07-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d07-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0d07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0d07-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0d07-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d07-106">Cmdleten **New-AzureRmVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="c0d07-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="c0d07-107">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="c0d07-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="c0d07-108">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="c0d07-108">These cmdlets are:</span></span>

- <span data-ttu-id="c0d07-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="c0d07-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="c0d07-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0d07-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="c0d07-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c0d07-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="c0d07-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0d07-113">EXAMPLES</span></span>

### <span data-ttu-id="c0d07-114">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="c0d07-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="c0d07-115">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="c0d07-116">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="c0d07-117">I det andra kommandot används cmdleten **New-AzureRmVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="c0d07-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="c0d07-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0d07-118">PARAMETERS</span></span>

### <span data-ttu-id="c0d07-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0d07-119">-AssignIdentity</span></span>
<span data-ttu-id="c0d07-120">Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c0d07-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d07-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c0d07-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="c0d07-122">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="c0d07-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d07-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c0d07-123">-BootDiagnostic</span></span>
<span data-ttu-id="c0d07-124">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="c0d07-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="c0d07-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-125">-DefaultProfile</span></span>
<span data-ttu-id="c0d07-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d07-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0d07-127">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="c0d07-127">-Extension</span></span>
<span data-ttu-id="c0d07-128">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="c0d07-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="c0d07-129">Du kan använda cmdleten **Add-AzureRmVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c0d07-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="c0d07-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="c0d07-130">-HealthProbeId</span></span>
<span data-ttu-id="c0d07-131">Ange ID för en belastnings Utjämnings sökning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c0d07-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="c0d07-132">HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="c0d07-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="c0d07-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c0d07-133">-IdentityType</span></span>
<span data-ttu-id="c0d07-134">Ange identiteten för den virtuella datorns skal uppsättning om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="c0d07-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d07-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c0d07-135">-LicenseType</span></span>
<span data-ttu-id="c0d07-136">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="c0d07-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="c0d07-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0d07-137">-Location</span></span>
<span data-ttu-id="c0d07-138">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="c0d07-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="c0d07-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0d07-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="c0d07-140">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="c0d07-141">Du kan använda cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c0d07-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="c0d07-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-142">-OsProfile</span></span>
<span data-ttu-id="c0d07-143">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c0d07-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="c0d07-144">Du kan använda cmdleten **set-AzureRmVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="c0d07-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="c0d07-145">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="c0d07-145">-Overprovision</span></span>
<span data-ttu-id="c0d07-146">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="c0d07-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c0d07-147">-PlanName</span></span>
<span data-ttu-id="c0d07-148">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="c0d07-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="c0d07-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c0d07-149">-PlanProduct</span></span>
<span data-ttu-id="c0d07-150">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="c0d07-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="c0d07-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c0d07-151">-PlanPromotionCode</span></span>
<span data-ttu-id="c0d07-152">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="c0d07-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="c0d07-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c0d07-153">-PlanPublisher</span></span>
<span data-ttu-id="c0d07-154">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="c0d07-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="c0d07-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c0d07-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="c0d07-156">Ange återställnings princip.</span><span class="sxs-lookup"><span data-stu-id="c0d07-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d07-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="c0d07-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="c0d07-158">Anger principen för rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="c0d07-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="c0d07-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c0d07-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="c0d07-160">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="c0d07-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="c0d07-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c0d07-161">-SkuCapacity</span></span>
<span data-ttu-id="c0d07-162">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d07-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c0d07-163">-SkuName</span></span>
<span data-ttu-id="c0d07-164">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="c0d07-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c0d07-165">-SkuTier</span></span>
<span data-ttu-id="c0d07-166">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="c0d07-167">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c0d07-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0d07-168">Standar</span><span class="sxs-lookup"><span data-stu-id="c0d07-168">Standard</span></span>
- <span data-ttu-id="c0d07-169">Basisk</span><span class="sxs-lookup"><span data-stu-id="c0d07-169">Basic</span></span>

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

### <span data-ttu-id="c0d07-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-170">-StorageProfile</span></span>
<span data-ttu-id="c0d07-171">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c0d07-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="c0d07-172">Du kan använda cmdleten **set-AzureRmVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="c0d07-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="c0d07-173">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c0d07-173">-Tag</span></span>
<span data-ttu-id="c0d07-174">Anger de taggar som ska kopplas till VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0d07-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="c0d07-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c0d07-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="c0d07-176">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c0d07-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="c0d07-177">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c0d07-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0d07-178">Versal</span><span class="sxs-lookup"><span data-stu-id="c0d07-178">Automatic</span></span>
- <span data-ttu-id="c0d07-179">Manövrer</span><span class="sxs-lookup"><span data-stu-id="c0d07-179">Manual</span></span>

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

### <span data-ttu-id="c0d07-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="c0d07-180">-Zone</span></span>
<span data-ttu-id="c0d07-181">Anger zon listan för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c0d07-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c0d07-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0d07-182">-Confirm</span></span>
<span data-ttu-id="c0d07-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0d07-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d07-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d07-184">-WhatIf</span></span>
<span data-ttu-id="c0d07-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0d07-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0d07-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0d07-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d07-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d07-187">CommonParameters</span></span>
<span data-ttu-id="c0d07-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d07-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d07-189">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d07-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d07-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0d07-190">INPUTS</span></span>

## <span data-ttu-id="c0d07-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0d07-191">OUTPUTS</span></span>

### <span data-ttu-id="c0d07-192">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c0d07-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c0d07-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0d07-193">NOTES</span></span>

## <span data-ttu-id="c0d07-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0d07-194">RELATED LINKS</span></span>

[<span data-ttu-id="c0d07-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="c0d07-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c0d07-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="c0d07-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0d07-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c0d07-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c0d07-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="c0d07-199">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c0d07-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


