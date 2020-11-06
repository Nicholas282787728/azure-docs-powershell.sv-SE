---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580231"
---
# <span data-ttu-id="41320-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="41320-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41320-102">SYNOPSIS</span></span>
<span data-ttu-id="41320-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41320-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41320-104">SYNTAX</span></span>

### <span data-ttu-id="41320-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="41320-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41320-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="41320-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41320-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41320-107">DESCRIPTION</span></span>
<span data-ttu-id="41320-108">Cmdleten **Update-AzureRmVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="41320-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="41320-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41320-109">EXAMPLES</span></span>

### <span data-ttu-id="41320-110">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="41320-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="41320-111">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till tillståndet för ett lokalt VMSS-objekt, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="41320-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41320-112">PARAMETERS</span></span>

### <span data-ttu-id="41320-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41320-113">-AsJob</span></span>
<span data-ttu-id="41320-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="41320-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="41320-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="41320-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="41320-116">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="41320-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="41320-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="41320-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="41320-118">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="41320-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="41320-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="41320-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="41320-120">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="41320-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="41320-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="41320-121">-CustomData</span></span>
<span data-ttu-id="41320-122">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="41320-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="41320-123">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="41320-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="41320-124">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="41320-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="41320-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41320-125">-DefaultProfile</span></span>
<span data-ttu-id="41320-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41320-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41320-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="41320-127">-DisableAutoRollback</span></span>
<span data-ttu-id="41320-128">Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system</span><span class="sxs-lookup"><span data-stu-id="41320-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="41320-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="41320-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="41320-130">Anger att denna cmdlet inaktiverar lösenordsautentisering för Linux OS.</span><span class="sxs-lookup"><span data-stu-id="41320-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="41320-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="41320-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="41320-132">Anger om de virtuella Windows-datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="41320-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="41320-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="41320-133">-IdentityId</span></span>
<span data-ttu-id="41320-134">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="41320-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="41320-135">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="41320-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="41320-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="41320-136">-IdentityType</span></span>
<span data-ttu-id="41320-137">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="41320-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="41320-138">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="41320-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="41320-139">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="41320-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="41320-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41320-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41320-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="41320-141">SystemAssigned</span></span>
- <span data-ttu-id="41320-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="41320-142">UserAssigned</span></span>
- <span data-ttu-id="41320-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="41320-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="41320-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="41320-144">None</span></span>

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

### <span data-ttu-id="41320-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="41320-145">-ImageReferenceId</span></span>
<span data-ttu-id="41320-146">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="41320-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="41320-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="41320-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="41320-148">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="41320-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="41320-149">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="41320-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="41320-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="41320-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="41320-151">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="41320-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="41320-152">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="41320-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="41320-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="41320-153">-ImageReferenceSku</span></span>
<span data-ttu-id="41320-154">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="41320-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="41320-155">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41320-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="41320-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="41320-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="41320-157">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="41320-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="41320-158">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="41320-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="41320-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="41320-159">-ImageUri</span></span>
<span data-ttu-id="41320-160">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="41320-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="41320-161">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="41320-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="41320-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="41320-162">-LicenseType</span></span>
<span data-ttu-id="41320-163">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="41320-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="41320-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="41320-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="41320-165">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="41320-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="41320-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41320-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41320-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="41320-167">StandardLRS</span></span>
- <span data-ttu-id="41320-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="41320-168">PremiumLRS</span></span>

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

### <span data-ttu-id="41320-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="41320-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="41320-170">Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.</span><span class="sxs-lookup"><span data-stu-id="41320-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="41320-171">Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="41320-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="41320-172">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="41320-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="41320-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="41320-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="41320-174">Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.</span><span class="sxs-lookup"><span data-stu-id="41320-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="41320-175">Det här villkoret kontrol leras innan en batch startas.</span><span class="sxs-lookup"><span data-stu-id="41320-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="41320-176">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="41320-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="41320-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="41320-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="41320-178">Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.</span><span class="sxs-lookup"><span data-stu-id="41320-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="41320-179">Denna kontroll sker efter att varje kommando har uppgraderats.</span><span class="sxs-lookup"><span data-stu-id="41320-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="41320-180">Om denna procents ATS överskrids avbryts den rullande uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="41320-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="41320-181">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="41320-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="41320-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="41320-182">-OsDiskCaching</span></span>
<span data-ttu-id="41320-183">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="41320-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="41320-184">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41320-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41320-185">Ingen</span><span class="sxs-lookup"><span data-stu-id="41320-185">None</span></span>
- <span data-ttu-id="41320-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="41320-186">ReadOnly</span></span>
- <span data-ttu-id="41320-187">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="41320-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="41320-188">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="41320-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="41320-189">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="41320-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="41320-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="41320-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="41320-191">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="41320-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="41320-192">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="41320-192">-Overprovision</span></span>
<span data-ttu-id="41320-193">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="41320-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="41320-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="41320-195">Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.</span><span class="sxs-lookup"><span data-stu-id="41320-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="41320-196">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="41320-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="41320-197">Standardvärdet är 0 sekunder (PT0S).</span><span class="sxs-lookup"><span data-stu-id="41320-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="41320-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="41320-198">-PlanName</span></span>
<span data-ttu-id="41320-199">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="41320-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="41320-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="41320-200">-PlanProduct</span></span>
<span data-ttu-id="41320-201">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="41320-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="41320-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="41320-202">-PlanPromotionCode</span></span>
<span data-ttu-id="41320-203">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="41320-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="41320-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="41320-204">-PlanPublisher</span></span>
<span data-ttu-id="41320-205">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="41320-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="41320-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="41320-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="41320-207">Anger om virtuell dator agent ska etableras på de virtuella Windows-datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="41320-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41320-208">-ResourceGroupName</span></span>
<span data-ttu-id="41320-209">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="41320-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41320-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="41320-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="41320-211">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="41320-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="41320-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="41320-212">-SkuCapacity</span></span>
<span data-ttu-id="41320-213">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="41320-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="41320-214">-SkuName</span></span>
<span data-ttu-id="41320-215">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="41320-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="41320-216">-SkuTier</span></span>
<span data-ttu-id="41320-217">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="41320-218">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41320-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41320-219">Standar</span><span class="sxs-lookup"><span data-stu-id="41320-219">Standard</span></span>
- <span data-ttu-id="41320-220">Basisk</span><span class="sxs-lookup"><span data-stu-id="41320-220">Basic</span></span>

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

### <span data-ttu-id="41320-221">-Tagg</span><span class="sxs-lookup"><span data-stu-id="41320-221">-Tag</span></span>
<span data-ttu-id="41320-222">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41320-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41320-223">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="41320-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41320-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="41320-224">-TimeZone</span></span>
<span data-ttu-id="41320-225">Anger tids zonen för Windows OS.</span><span class="sxs-lookup"><span data-stu-id="41320-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="41320-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="41320-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="41320-227">Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="41320-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="41320-228">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="41320-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="41320-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="41320-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="41320-230">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="41320-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="41320-231">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41320-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41320-232">Versal</span><span class="sxs-lookup"><span data-stu-id="41320-232">Automatic</span></span>
- <span data-ttu-id="41320-233">Manövrer</span><span class="sxs-lookup"><span data-stu-id="41320-233">Manual</span></span>
- <span data-ttu-id="41320-234">Rullar</span><span class="sxs-lookup"><span data-stu-id="41320-234">Rolling</span></span>

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

### <span data-ttu-id="41320-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="41320-235">-VhdContainer</span></span>
<span data-ttu-id="41320-236">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="41320-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41320-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="41320-238">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="41320-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="41320-239">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="41320-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="41320-240">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="41320-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41320-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="41320-241">-VMScaleSetName</span></span>
<span data-ttu-id="41320-242">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="41320-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41320-243">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41320-243">-Confirm</span></span>
<span data-ttu-id="41320-244">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41320-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41320-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41320-245">-WhatIf</span></span>
<span data-ttu-id="41320-246">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41320-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41320-247">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41320-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41320-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41320-248">CommonParameters</span></span>
<span data-ttu-id="41320-249">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41320-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41320-250">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41320-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41320-251">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41320-251">INPUTS</span></span>

### <span data-ttu-id="41320-252">System. String</span><span class="sxs-lookup"><span data-stu-id="41320-252">System.String</span></span>

### <span data-ttu-id="41320-253">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41320-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="41320-254">Parametrar: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41320-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="41320-255">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41320-255">OUTPUTS</span></span>

### <span data-ttu-id="41320-256">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41320-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="41320-257">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41320-257">NOTES</span></span>

## <span data-ttu-id="41320-258">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41320-258">RELATED LINKS</span></span>

[<span data-ttu-id="41320-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="41320-260">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="41320-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="41320-262">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="41320-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="41320-264">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="41320-265">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41320-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


