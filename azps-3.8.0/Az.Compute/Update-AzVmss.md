---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092313"
---
# <span data-ttu-id="42644-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-101">Update-AzVmss</span></span>

## <span data-ttu-id="42644-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42644-102">SYNOPSIS</span></span>
<span data-ttu-id="42644-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="42644-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42644-104">SYNTAX</span></span>

### <span data-ttu-id="42644-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="42644-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42644-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="42644-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42644-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42644-107">DESCRIPTION</span></span>
<span data-ttu-id="42644-108">Cmdleten **Update-AzVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="42644-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="42644-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42644-109">EXAMPLES</span></span>

### <span data-ttu-id="42644-110">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="42644-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="42644-111">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till tillståndet för ett lokalt VMSS-objekt, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="42644-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42644-112">PARAMETERS</span></span>

### <span data-ttu-id="42644-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42644-113">-AsJob</span></span>
<span data-ttu-id="42644-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="42644-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="42644-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="42644-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="42644-116">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="42644-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="42644-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="42644-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="42644-118">Den tid som automatiska reparationer har upphävts på grund av en tillstånds ändring på VM.</span><span class="sxs-lookup"><span data-stu-id="42644-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="42644-119">Grace-tiden inleds efter att statusen har ändrats.</span><span class="sxs-lookup"><span data-stu-id="42644-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="42644-120">Detta gör att du kan undvika för tidigt eller oavsiktlig reparation.</span><span class="sxs-lookup"><span data-stu-id="42644-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="42644-121">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="42644-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="42644-122">Standardvärdet är 5 minuter (PT5M).</span><span class="sxs-lookup"><span data-stu-id="42644-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="42644-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="42644-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="42644-124">Procent andelen (kapaciteten för scaleset) för virtuella datorer som kommer att repare ras samtidigt.</span><span class="sxs-lookup"><span data-stu-id="42644-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="42644-125">Standardvärdet är 20%.</span><span class="sxs-lookup"><span data-stu-id="42644-125">The default value is 20%.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="42644-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="42644-127">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="42644-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="42644-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="42644-129">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="42644-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="42644-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="42644-130">-CustomData</span></span>
<span data-ttu-id="42644-131">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="42644-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="42644-132">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="42644-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="42644-133">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="42644-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="42644-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42644-134">-DefaultProfile</span></span>
<span data-ttu-id="42644-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42644-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42644-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="42644-136">-DisableAutoRollback</span></span>
<span data-ttu-id="42644-137">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="42644-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="42644-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="42644-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="42644-139">Anger att denna cmdlet inaktiverar lösenordsautentisering för Linux OS.</span><span class="sxs-lookup"><span data-stu-id="42644-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="42644-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="42644-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="42644-141">Aktivera eller inaktivera automatisk reparation på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="42644-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="42644-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="42644-143">Anger om de virtuella Windows-datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="42644-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="42644-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="42644-144">-IdentityId</span></span>
<span data-ttu-id="42644-145">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="42644-146">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="42644-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="42644-147">-IdentityType</span></span>
<span data-ttu-id="42644-148">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="42644-149">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="42644-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="42644-150">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="42644-151">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42644-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42644-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="42644-152">SystemAssigned</span></span>
- <span data-ttu-id="42644-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="42644-153">UserAssigned</span></span>
- <span data-ttu-id="42644-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="42644-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="42644-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="42644-155">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="42644-156">-ImageReferenceId</span></span>
<span data-ttu-id="42644-157">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="42644-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="42644-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="42644-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="42644-159">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="42644-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="42644-160">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="42644-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="42644-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="42644-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="42644-162">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="42644-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="42644-163">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="42644-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="42644-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="42644-164">-ImageReferenceSku</span></span>
<span data-ttu-id="42644-165">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="42644-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="42644-166">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42644-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="42644-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="42644-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="42644-168">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="42644-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="42644-169">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="42644-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="42644-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="42644-170">-ImageUri</span></span>
<span data-ttu-id="42644-171">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="42644-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="42644-172">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="42644-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="42644-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="42644-173">-LicenseType</span></span>
<span data-ttu-id="42644-174">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="42644-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="42644-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="42644-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="42644-176">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="42644-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="42644-177">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42644-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42644-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="42644-178">StandardLRS</span></span>
- <span data-ttu-id="42644-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="42644-179">PremiumLRS</span></span>

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

### <span data-ttu-id="42644-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="42644-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="42644-181">Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.</span><span class="sxs-lookup"><span data-stu-id="42644-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="42644-182">Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="42644-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="42644-183">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="42644-183">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="42644-184">-MaxPrice</span></span>
<span data-ttu-id="42644-185">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="42644-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="42644-186">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="42644-186">This price is in US Dollars.</span></span> <span data-ttu-id="42644-187">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="42644-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="42644-188">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="42644-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="42644-189">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="42644-190">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="42644-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="42644-191">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="42644-191">Example: 0.01538.</span></span>  <span data-ttu-id="42644-192">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="42644-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="42644-193">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="42644-193">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="42644-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="42644-195">Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.</span><span class="sxs-lookup"><span data-stu-id="42644-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="42644-196">Det här villkoret kontrol leras innan en batch startas.</span><span class="sxs-lookup"><span data-stu-id="42644-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="42644-197">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="42644-197">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="42644-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="42644-199">Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.</span><span class="sxs-lookup"><span data-stu-id="42644-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="42644-200">Denna kontroll sker efter att varje kommando har uppgraderats.</span><span class="sxs-lookup"><span data-stu-id="42644-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="42644-201">Om denna procents ATS överskrids avbryts den rullande uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="42644-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="42644-202">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="42644-202">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="42644-203">-OsDiskCaching</span></span>
<span data-ttu-id="42644-204">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="42644-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="42644-205">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42644-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42644-206">Ingen</span><span class="sxs-lookup"><span data-stu-id="42644-206">None</span></span>
- <span data-ttu-id="42644-207">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="42644-207">ReadOnly</span></span>
- <span data-ttu-id="42644-208">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="42644-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="42644-209">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="42644-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="42644-210">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="42644-210">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="42644-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="42644-212">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="42644-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="42644-213">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="42644-213">-Overprovision</span></span>
<span data-ttu-id="42644-214">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="42644-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="42644-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="42644-216">Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.</span><span class="sxs-lookup"><span data-stu-id="42644-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="42644-217">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="42644-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="42644-218">Standardvärdet är 0 sekunder (PT0S).</span><span class="sxs-lookup"><span data-stu-id="42644-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="42644-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="42644-219">-PlanName</span></span>
<span data-ttu-id="42644-220">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="42644-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="42644-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="42644-221">-PlanProduct</span></span>
<span data-ttu-id="42644-222">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="42644-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="42644-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="42644-223">-PlanPromotionCode</span></span>
<span data-ttu-id="42644-224">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="42644-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="42644-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="42644-225">-PlanPublisher</span></span>
<span data-ttu-id="42644-226">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="42644-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="42644-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="42644-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="42644-228">Anger om virtuell dator agent ska etableras på de virtuella Windows-datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="42644-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="42644-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="42644-230">Resurs-ID för närhets gruppen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="42644-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="42644-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42644-231">-ResourceGroupName</span></span>
<span data-ttu-id="42644-232">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="42644-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42644-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="42644-233">-ScaleInPolicy</span></span>
<span data-ttu-id="42644-234">De regler som ska användas vid skalning-i en virtuell dators skala uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="42644-235">Möjliga värden är: ' default ', ' OldestVM ' och ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="42644-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="42644-236">"Standard" när en skala för virtuell dator skal för änd ras i, fördelas skalnings uppsättningen först över zoner om den är en Zonal skala.</span><span class="sxs-lookup"><span data-stu-id="42644-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="42644-237">Då kommer den att bal anse ras i så stor utsträckning som möjligt.</span><span class="sxs-lookup"><span data-stu-id="42644-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="42644-238">De virtuella datorerna som valts för borttagning är de nyaste som inte skyddas från Scale-in i varje fel domän.</span><span class="sxs-lookup"><span data-stu-id="42644-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="42644-239">' OldestVM ' när en virtuell dators Scale-uppsättning skal för änd ras-in väljs de äldsta virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="42644-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="42644-240">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="42644-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="42644-241">Inom varje zon kommer de äldsta virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="42644-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="42644-242">' NewestVM ' när en virtuell dators skal uppsättning skal för änd ras-in väljs de senaste virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="42644-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="42644-243">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="42644-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="42644-244">Inom varje zon kommer de senaste virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="42644-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="42644-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="42644-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="42644-246">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="42644-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="42644-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="42644-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="42644-248">Anger att tilläggen inte körs på de extra överetablerade datorerna.</span><span class="sxs-lookup"><span data-stu-id="42644-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="42644-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="42644-249">-SkuCapacity</span></span>
<span data-ttu-id="42644-250">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-250">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="42644-251">-SkuName</span></span>
<span data-ttu-id="42644-252">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="42644-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="42644-253">-SkuTier</span></span>
<span data-ttu-id="42644-254">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="42644-255">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42644-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42644-256">Standar</span><span class="sxs-lookup"><span data-stu-id="42644-256">Standard</span></span>
- <span data-ttu-id="42644-257">Basisk</span><span class="sxs-lookup"><span data-stu-id="42644-257">Basic</span></span>

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

### <span data-ttu-id="42644-258">-Tagg</span><span class="sxs-lookup"><span data-stu-id="42644-258">-Tag</span></span>
<span data-ttu-id="42644-259">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="42644-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42644-260">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="42644-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="42644-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="42644-262">Konfigurerbar längd (i minuter) en virtuell dator som tas bort måste eventuellt godkänna händelsen Avsluta schemalagd händelse innan händelsen är automatiskt godkänd (tids gräns).</span><span class="sxs-lookup"><span data-stu-id="42644-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="42644-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="42644-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="42644-264">Anger om den schemalagda händelsen Avbryt är aktive rad eller inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="42644-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42644-265">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="42644-265">-TimeZone</span></span>
<span data-ttu-id="42644-266">Anger tids zonen för Windows OS.</span><span class="sxs-lookup"><span data-stu-id="42644-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="42644-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="42644-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="42644-268">Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="42644-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="42644-269">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="42644-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42644-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="42644-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="42644-271">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="42644-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="42644-272">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42644-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42644-273">Versal</span><span class="sxs-lookup"><span data-stu-id="42644-273">Automatic</span></span>
- <span data-ttu-id="42644-274">Manövrer</span><span class="sxs-lookup"><span data-stu-id="42644-274">Manual</span></span>
- <span data-ttu-id="42644-275">Rullar</span><span class="sxs-lookup"><span data-stu-id="42644-275">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="42644-276">-VhdContainer</span></span>
<span data-ttu-id="42644-277">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="42644-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42644-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="42644-279">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="42644-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="42644-280">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="42644-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="42644-281">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="42644-281">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42644-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="42644-282">-VMScaleSetName</span></span>
<span data-ttu-id="42644-283">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="42644-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42644-284">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42644-284">-Confirm</span></span>
<span data-ttu-id="42644-285">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42644-285">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42644-286">-WhatIf</span></span>
<span data-ttu-id="42644-287">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42644-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42644-288">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42644-288">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42644-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42644-289">CommonParameters</span></span>
<span data-ttu-id="42644-290">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42644-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42644-291">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42644-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42644-292">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42644-292">INPUTS</span></span>

### <span data-ttu-id="42644-293">System. String</span><span class="sxs-lookup"><span data-stu-id="42644-293">System.String</span></span>

### <span data-ttu-id="42644-294">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42644-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="42644-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42644-295">System.Boolean</span></span>

## <span data-ttu-id="42644-296">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42644-296">OUTPUTS</span></span>

### <span data-ttu-id="42644-297">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42644-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="42644-298">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42644-298">NOTES</span></span>

## <span data-ttu-id="42644-299">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42644-299">RELATED LINKS</span></span>

[<span data-ttu-id="42644-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="42644-301">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="42644-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="42644-303">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="42644-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="42644-305">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="42644-306">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42644-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


