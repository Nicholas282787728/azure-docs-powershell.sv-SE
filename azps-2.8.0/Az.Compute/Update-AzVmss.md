---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744876"
---
# <span data-ttu-id="0976a-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-101">Update-AzVmss</span></span>

## <span data-ttu-id="0976a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0976a-102">SYNOPSIS</span></span>
<span data-ttu-id="0976a-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="0976a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0976a-104">SYNTAX</span></span>

### <span data-ttu-id="0976a-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="0976a-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0976a-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="0976a-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0976a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0976a-107">DESCRIPTION</span></span>
<span data-ttu-id="0976a-108">Cmdleten **Update-AzVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="0976a-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="0976a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0976a-109">EXAMPLES</span></span>

### <span data-ttu-id="0976a-110">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="0976a-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="0976a-111">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till tillståndet för ett lokalt VMSS-objekt, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="0976a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0976a-112">PARAMETERS</span></span>

### <span data-ttu-id="0976a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0976a-113">-AsJob</span></span>
<span data-ttu-id="0976a-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="0976a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0976a-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0976a-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="0976a-116">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="0976a-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="0976a-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="0976a-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="0976a-118">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0976a-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0976a-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="0976a-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="0976a-120">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="0976a-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="0976a-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="0976a-121">-CustomData</span></span>
<span data-ttu-id="0976a-122">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="0976a-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="0976a-123">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0976a-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="0976a-124">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="0976a-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="0976a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0976a-125">-DefaultProfile</span></span>
<span data-ttu-id="0976a-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0976a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0976a-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="0976a-127">-DisableAutoRollback</span></span>
<span data-ttu-id="0976a-128">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="0976a-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="0976a-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="0976a-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="0976a-130">Anger att denna cmdlet inaktiverar lösenordsautentisering för Linux OS.</span><span class="sxs-lookup"><span data-stu-id="0976a-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="0976a-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="0976a-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="0976a-132">Anger om de virtuella Windows-datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="0976a-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="0976a-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="0976a-133">-IdentityId</span></span>
<span data-ttu-id="0976a-134">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0976a-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="0976a-135">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="0976a-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="0976a-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0976a-136">-IdentityType</span></span>
<span data-ttu-id="0976a-137">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0976a-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="0976a-138">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="0976a-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="0976a-139">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0976a-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="0976a-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0976a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976a-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0976a-141">SystemAssigned</span></span>
- <span data-ttu-id="0976a-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="0976a-142">UserAssigned</span></span>
- <span data-ttu-id="0976a-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="0976a-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="0976a-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="0976a-144">None</span></span>

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

### <span data-ttu-id="0976a-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="0976a-145">-ImageReferenceId</span></span>
<span data-ttu-id="0976a-146">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="0976a-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="0976a-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="0976a-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="0976a-148">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="0976a-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="0976a-149">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="0976a-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="0976a-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="0976a-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="0976a-151">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="0976a-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0976a-152">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="0976a-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0976a-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="0976a-153">-ImageReferenceSku</span></span>
<span data-ttu-id="0976a-154">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="0976a-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="0976a-155">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0976a-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="0976a-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="0976a-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="0976a-157">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="0976a-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="0976a-158">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="0976a-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="0976a-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="0976a-159">-ImageUri</span></span>
<span data-ttu-id="0976a-160">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="0976a-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="0976a-161">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="0976a-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="0976a-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0976a-162">-LicenseType</span></span>
<span data-ttu-id="0976a-163">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="0976a-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="0976a-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0976a-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="0976a-165">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0976a-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="0976a-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0976a-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976a-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="0976a-167">StandardLRS</span></span>
- <span data-ttu-id="0976a-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="0976a-168">PremiumLRS</span></span>

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

### <span data-ttu-id="0976a-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0976a-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="0976a-170">Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.</span><span class="sxs-lookup"><span data-stu-id="0976a-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="0976a-171">Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="0976a-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="0976a-172">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="0976a-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="0976a-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="0976a-173">-MaxPrice</span></span>
<span data-ttu-id="0976a-174">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="0976a-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="0976a-175">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="0976a-175">This price is in US Dollars.</span></span> <span data-ttu-id="0976a-176">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="0976a-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="0976a-177">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="0976a-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="0976a-178">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="0976a-179">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="0976a-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="0976a-180">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="0976a-180">Example: 0.01538.</span></span>  <span data-ttu-id="0976a-181">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="0976a-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="0976a-182">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="0976a-182">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="0976a-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0976a-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="0976a-184">Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.</span><span class="sxs-lookup"><span data-stu-id="0976a-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="0976a-185">Det här villkoret kontrol leras innan en batch startas.</span><span class="sxs-lookup"><span data-stu-id="0976a-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="0976a-186">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="0976a-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="0976a-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0976a-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="0976a-188">Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.</span><span class="sxs-lookup"><span data-stu-id="0976a-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="0976a-189">Denna kontroll sker efter att varje kommando har uppgraderats.</span><span class="sxs-lookup"><span data-stu-id="0976a-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="0976a-190">Om denna procents ATS överskrids avbryts den rullande uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="0976a-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="0976a-191">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="0976a-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="0976a-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="0976a-192">-OsDiskCaching</span></span>
<span data-ttu-id="0976a-193">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="0976a-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="0976a-194">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0976a-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976a-195">Ingen</span><span class="sxs-lookup"><span data-stu-id="0976a-195">None</span></span>
- <span data-ttu-id="0976a-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0976a-196">ReadOnly</span></span>
- <span data-ttu-id="0976a-197">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0976a-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0976a-198">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="0976a-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="0976a-199">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="0976a-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="0976a-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0976a-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="0976a-201">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="0976a-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="0976a-202">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="0976a-202">-Overprovision</span></span>
<span data-ttu-id="0976a-203">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="0976a-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="0976a-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="0976a-205">Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.</span><span class="sxs-lookup"><span data-stu-id="0976a-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="0976a-206">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="0976a-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="0976a-207">Standardvärdet är 0 sekunder (PT0S).</span><span class="sxs-lookup"><span data-stu-id="0976a-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="0976a-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0976a-208">-PlanName</span></span>
<span data-ttu-id="0976a-209">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="0976a-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="0976a-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="0976a-210">-PlanProduct</span></span>
<span data-ttu-id="0976a-211">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="0976a-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="0976a-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="0976a-212">-PlanPromotionCode</span></span>
<span data-ttu-id="0976a-213">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="0976a-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="0976a-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="0976a-214">-PlanPublisher</span></span>
<span data-ttu-id="0976a-215">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0976a-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="0976a-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="0976a-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="0976a-217">Anger om virtuell dator agent ska etableras på de virtuella Windows-datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="0976a-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0976a-218">-ResourceGroupName</span></span>
<span data-ttu-id="0976a-219">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="0976a-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="0976a-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0976a-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="0976a-221">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="0976a-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="0976a-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0976a-222">-SkuCapacity</span></span>
<span data-ttu-id="0976a-223">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="0976a-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0976a-224">-SkuName</span></span>
<span data-ttu-id="0976a-225">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="0976a-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0976a-226">-SkuTier</span></span>
<span data-ttu-id="0976a-227">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="0976a-228">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0976a-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976a-229">Standar</span><span class="sxs-lookup"><span data-stu-id="0976a-229">Standard</span></span>
- <span data-ttu-id="0976a-230">Basisk</span><span class="sxs-lookup"><span data-stu-id="0976a-230">Basic</span></span>

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

### <span data-ttu-id="0976a-231">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0976a-231">-Tag</span></span>
<span data-ttu-id="0976a-232">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0976a-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0976a-233">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="0976a-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0976a-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0976a-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="0976a-235">Konfigurerbar längd (i minuter) en virtuell dator som tas bort måste eventuellt godkänna händelsen Avsluta schemalagd händelse innan händelsen är automatiskt godkänd (tids gräns).</span><span class="sxs-lookup"><span data-stu-id="0976a-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="0976a-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="0976a-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="0976a-237">Anger om den schemalagda händelsen Avbryt är aktive rad eller inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="0976a-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="0976a-238">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="0976a-238">-TimeZone</span></span>
<span data-ttu-id="0976a-239">Anger tids zonen för Windows OS.</span><span class="sxs-lookup"><span data-stu-id="0976a-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="0976a-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="0976a-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="0976a-241">Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0976a-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="0976a-242">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="0976a-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="0976a-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="0976a-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="0976a-244">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="0976a-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="0976a-245">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0976a-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976a-246">Versal</span><span class="sxs-lookup"><span data-stu-id="0976a-246">Automatic</span></span>
- <span data-ttu-id="0976a-247">Manövrer</span><span class="sxs-lookup"><span data-stu-id="0976a-247">Manual</span></span>
- <span data-ttu-id="0976a-248">Rullar</span><span class="sxs-lookup"><span data-stu-id="0976a-248">Rolling</span></span>

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

### <span data-ttu-id="0976a-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="0976a-249">-VhdContainer</span></span>
<span data-ttu-id="0976a-250">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="0976a-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0976a-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0976a-252">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="0976a-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="0976a-253">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0976a-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="0976a-254">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="0976a-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="0976a-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0976a-255">-VMScaleSetName</span></span>
<span data-ttu-id="0976a-256">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="0976a-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0976a-257">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0976a-257">-Confirm</span></span>
<span data-ttu-id="0976a-258">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0976a-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0976a-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0976a-259">-WhatIf</span></span>
<span data-ttu-id="0976a-260">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0976a-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0976a-261">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0976a-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0976a-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0976a-262">CommonParameters</span></span>
<span data-ttu-id="0976a-263">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0976a-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0976a-264">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0976a-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0976a-265">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0976a-265">INPUTS</span></span>

### <span data-ttu-id="0976a-266">System. String</span><span class="sxs-lookup"><span data-stu-id="0976a-266">System.String</span></span>

### <span data-ttu-id="0976a-267">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0976a-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0976a-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0976a-268">System.Boolean</span></span>

## <span data-ttu-id="0976a-269">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0976a-269">OUTPUTS</span></span>

### <span data-ttu-id="0976a-270">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0976a-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0976a-271">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0976a-271">NOTES</span></span>

## <span data-ttu-id="0976a-272">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0976a-272">RELATED LINKS</span></span>

[<span data-ttu-id="0976a-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="0976a-274">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="0976a-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="0976a-276">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0976a-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0976a-278">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0976a-279">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0976a-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


