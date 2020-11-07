---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924745"
---
# <span data-ttu-id="afd1f-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-101">Update-AzVmss</span></span>

## <span data-ttu-id="afd1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="afd1f-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="afd1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afd1f-104">SYNTAX</span></span>

### <span data-ttu-id="afd1f-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="afd1f-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd1f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="afd1f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afd1f-107">DESCRIPTION</span></span>
<span data-ttu-id="afd1f-108">Cmdleten **Update-AzVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="afd1f-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="afd1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afd1f-109">EXAMPLES</span></span>

### <span data-ttu-id="afd1f-110">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="afd1f-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="afd1f-111">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till tillståndet för ett lokalt VMSS-objekt, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="afd1f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afd1f-112">PARAMETERS</span></span>

### <span data-ttu-id="afd1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afd1f-113">-AsJob</span></span>
<span data-ttu-id="afd1f-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="afd1f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="afd1f-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="afd1f-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="afd1f-116">Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="afd1f-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="afd1f-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="afd1f-118">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="afd1f-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="afd1f-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="afd1f-120">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="afd1f-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="afd1f-121">-CustomData</span></span>
<span data-ttu-id="afd1f-122">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="afd1f-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="afd1f-123">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="afd1f-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="afd1f-124">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="afd1f-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd1f-125">-DefaultProfile</span></span>
<span data-ttu-id="afd1f-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afd1f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd1f-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="afd1f-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="afd1f-128">Anger att denna cmdlet inaktiverar lösenordsautentisering för Linux OS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="afd1f-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="afd1f-130">Anger om de virtuella Windows-datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="afd1f-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="afd1f-131">-IdentityId</span></span>
<span data-ttu-id="afd1f-132">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="afd1f-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="afd1f-133">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="afd1f-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="afd1f-134">-IdentityType</span></span>
<span data-ttu-id="afd1f-135">Anger den typ av identitet som används för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="afd1f-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="afd1f-136">Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="afd1f-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="afd1f-137">Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="afd1f-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="afd1f-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afd1f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afd1f-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="afd1f-139">SystemAssigned</span></span>
- <span data-ttu-id="afd1f-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="afd1f-140">UserAssigned</span></span>
- <span data-ttu-id="afd1f-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="afd1f-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="afd1f-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="afd1f-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="afd1f-143">-ImageReferenceId</span></span>
<span data-ttu-id="afd1f-144">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="afd1f-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="afd1f-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="afd1f-146">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="afd1f-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="afd1f-147">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="afd1f-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="afd1f-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="afd1f-149">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="afd1f-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="afd1f-150">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="afd1f-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="afd1f-151">-ImageReferenceSku</span></span>
<span data-ttu-id="afd1f-152">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="afd1f-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="afd1f-153">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd1f-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="afd1f-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="afd1f-155">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="afd1f-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="afd1f-156">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="afd1f-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="afd1f-157">-ImageUri</span></span>
<span data-ttu-id="afd1f-158">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="afd1f-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="afd1f-159">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="afd1f-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="afd1f-160">-LicenseType</span></span>
<span data-ttu-id="afd1f-161">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="afd1f-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="afd1f-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="afd1f-163">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="afd1f-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="afd1f-164">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afd1f-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afd1f-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="afd1f-165">StandardLRS</span></span>
- <span data-ttu-id="afd1f-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="afd1f-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="afd1f-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="afd1f-168">Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.</span><span class="sxs-lookup"><span data-stu-id="afd1f-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="afd1f-169">Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="afd1f-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="afd1f-170">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="afd1f-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="afd1f-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="afd1f-172">Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.</span><span class="sxs-lookup"><span data-stu-id="afd1f-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="afd1f-173">Det här villkoret kontrol leras innan en batch startas.</span><span class="sxs-lookup"><span data-stu-id="afd1f-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="afd1f-174">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="afd1f-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="afd1f-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="afd1f-176">Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.</span><span class="sxs-lookup"><span data-stu-id="afd1f-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="afd1f-177">Denna kontroll sker efter att varje kommando har uppgraderats.</span><span class="sxs-lookup"><span data-stu-id="afd1f-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="afd1f-178">Om denna procents ATS överskrids avbryts den rullande uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="afd1f-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="afd1f-179">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="afd1f-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="afd1f-180">-OsDiskCaching</span></span>
<span data-ttu-id="afd1f-181">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="afd1f-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="afd1f-182">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afd1f-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afd1f-183">Ingen</span><span class="sxs-lookup"><span data-stu-id="afd1f-183">None</span></span>
- <span data-ttu-id="afd1f-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="afd1f-184">ReadOnly</span></span>
- <span data-ttu-id="afd1f-185">Läs</span><span class="sxs-lookup"><span data-stu-id="afd1f-185">ReadWrite</span></span>

<span data-ttu-id="afd1f-186">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="afd1f-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="afd1f-187">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="afd1f-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="afd1f-188">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="afd1f-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="afd1f-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="afd1f-190">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="afd1f-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-191">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="afd1f-191">-Overprovision</span></span>
<span data-ttu-id="afd1f-192">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="afd1f-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="afd1f-194">Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.</span><span class="sxs-lookup"><span data-stu-id="afd1f-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="afd1f-195">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="afd1f-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="afd1f-196">Standardvärdet är 0 sekunder (PT0S).</span><span class="sxs-lookup"><span data-stu-id="afd1f-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="afd1f-197">-PlanName</span></span>
<span data-ttu-id="afd1f-198">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="afd1f-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="afd1f-199">-PlanProduct</span></span>
<span data-ttu-id="afd1f-200">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="afd1f-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="afd1f-201">-PlanPromotionCode</span></span>
<span data-ttu-id="afd1f-202">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="afd1f-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="afd1f-203">-PlanPublisher</span></span>
<span data-ttu-id="afd1f-204">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="afd1f-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="afd1f-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="afd1f-206">Anger om virtuell dator agent ska etableras på de virtuella Windows-datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd1f-207">-ResourceGroupName</span></span>
<span data-ttu-id="afd1f-208">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="afd1f-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="afd1f-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="afd1f-210">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="afd1f-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="afd1f-211">-SkuCapacity</span></span>
<span data-ttu-id="afd1f-212">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="afd1f-213">-SkuName</span></span>
<span data-ttu-id="afd1f-214">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="afd1f-215">-SkuTier</span></span>
<span data-ttu-id="afd1f-216">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="afd1f-217">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afd1f-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afd1f-218">Standar</span><span class="sxs-lookup"><span data-stu-id="afd1f-218">Standard</span></span>
- <span data-ttu-id="afd1f-219">Basisk</span><span class="sxs-lookup"><span data-stu-id="afd1f-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-220">-Tagg</span><span class="sxs-lookup"><span data-stu-id="afd1f-220">-Tag</span></span>
<span data-ttu-id="afd1f-221">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="afd1f-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="afd1f-222">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="afd1f-222">For example:</span></span>

<span data-ttu-id="afd1f-223">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="afd1f-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="afd1f-224">-TimeZone</span></span>
<span data-ttu-id="afd1f-225">Anger tids zonen för Windows OS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="afd1f-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="afd1f-227">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="afd1f-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="afd1f-228">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afd1f-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afd1f-229">Versal</span><span class="sxs-lookup"><span data-stu-id="afd1f-229">Automatic</span></span>
- <span data-ttu-id="afd1f-230">Manövrer</span><span class="sxs-lookup"><span data-stu-id="afd1f-230">Manual</span></span>
- <span data-ttu-id="afd1f-231">Rullar</span><span class="sxs-lookup"><span data-stu-id="afd1f-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="afd1f-232">-VhdContainer</span></span>
<span data-ttu-id="afd1f-233">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afd1f-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="afd1f-235">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="afd1f-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="afd1f-236">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="afd1f-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="afd1f-237">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="afd1f-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="afd1f-238">-VMScaleSetName</span></span>
<span data-ttu-id="afd1f-239">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="afd1f-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-240">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afd1f-240">-Confirm</span></span>
<span data-ttu-id="afd1f-241">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afd1f-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd1f-242">-WhatIf</span></span>
<span data-ttu-id="afd1f-243">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afd1f-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="afd1f-244">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afd1f-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd1f-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd1f-245">CommonParameters</span></span>
<span data-ttu-id="afd1f-246">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd1f-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd1f-247">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd1f-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd1f-248">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afd1f-248">INPUTS</span></span>

### <span data-ttu-id="afd1f-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afd1f-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="afd1f-250">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="afd1f-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="afd1f-251">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afd1f-251">OUTPUTS</span></span>

### <span data-ttu-id="afd1f-252">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afd1f-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="afd1f-253">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afd1f-253">NOTES</span></span>

## <span data-ttu-id="afd1f-254">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afd1f-254">RELATED LINKS</span></span>

[<span data-ttu-id="afd1f-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="afd1f-256">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="afd1f-257">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="afd1f-258">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="afd1f-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="afd1f-260">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="afd1f-261">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="afd1f-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


