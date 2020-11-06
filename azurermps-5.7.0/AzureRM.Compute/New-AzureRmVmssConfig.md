---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575711"
---
# <span data-ttu-id="ae7bf-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ae7bf-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="ae7bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7bf-103">Skapar ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae7bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae7bf-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae7bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae7bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7bf-106">Cmdleten **New-AzureRmVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="ae7bf-107">Andra cmdletar behövs för att konfigurera VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="ae7bf-108">Dessa cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="ae7bf-108">These cmdlets are:</span></span>

- <span data-ttu-id="ae7bf-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="ae7bf-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="ae7bf-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae7bf-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ae7bf-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ae7bf-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="ae7bf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae7bf-113">EXAMPLES</span></span>

### <span data-ttu-id="ae7bf-114">Exempel 1: skapa ett VMSS-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="ae7bf-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="ae7bf-115">I det här exemplet skapas ett VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="ae7bf-116">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="ae7bf-117">I det andra kommandot används cmdleten **New-AzureRmVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="ae7bf-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae7bf-118">PARAMETERS</span></span>

### <span data-ttu-id="ae7bf-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ae7bf-119">-BootDiagnostic</span></span>
<span data-ttu-id="ae7bf-120">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ae7bf-121">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="ae7bf-121">-Extension</span></span>
<span data-ttu-id="ae7bf-122">Anger VMSS för tillägget.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="ae7bf-123">Du kan använda cmdleten **Add-AzureRmVmssExtension** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ae7bf-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ae7bf-124">-IdentityType</span></span>
<span data-ttu-id="ae7bf-125">Ange identiteten för den virtuella datorns skal uppsättning om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bf-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ae7bf-126">-LicenseType</span></span>
<span data-ttu-id="ae7bf-127">Ange licens typ, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ae7bf-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="ae7bf-128">-Location</span></span>
<span data-ttu-id="ae7bf-129">Anger den Azure-plats där VMSS skapas.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ae7bf-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae7bf-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ae7bf-131">Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ae7bf-132">Du kan använda cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ae7bf-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-133">-OsProfile</span></span>
<span data-ttu-id="ae7bf-134">Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ae7bf-135">Du kan använda cmdleten **set-AzureRmVmssOsProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ae7bf-136">-Överleverans</span><span class="sxs-lookup"><span data-stu-id="ae7bf-136">-Overprovision</span></span>
<span data-ttu-id="ae7bf-137">Anger om cmdleten ska VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ae7bf-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ae7bf-138">-PlanName</span></span>
<span data-ttu-id="ae7bf-139">Anger plan namnet.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ae7bf-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ae7bf-140">-PlanProduct</span></span>
<span data-ttu-id="ae7bf-141">Anger plan produkten.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ae7bf-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ae7bf-142">-PlanPromotionCode</span></span>
<span data-ttu-id="ae7bf-143">Anger abonnemangs kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ae7bf-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ae7bf-144">-PlanPublisher</span></span>
<span data-ttu-id="ae7bf-145">Anger plan utgivaren.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ae7bf-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="ae7bf-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="ae7bf-147">Ange återställnings princip.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bf-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ae7bf-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="ae7bf-149">Anger gruppen enskild placering.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ae7bf-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ae7bf-150">-SkuCapacity</span></span>
<span data-ttu-id="ae7bf-151">Anger antalet instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bf-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ae7bf-152">-SkuName</span></span>
<span data-ttu-id="ae7bf-153">Anger storleken på alla instanser av VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ae7bf-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ae7bf-154">-SkuTier</span></span>
<span data-ttu-id="ae7bf-155">Anger nivån för VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="ae7bf-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ae7bf-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae7bf-157">Standar</span><span class="sxs-lookup"><span data-stu-id="ae7bf-157">Standard</span></span>
- <span data-ttu-id="ae7bf-158">Basisk</span><span class="sxs-lookup"><span data-stu-id="ae7bf-158">Basic</span></span>

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

### <span data-ttu-id="ae7bf-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-159">-StorageProfile</span></span>
<span data-ttu-id="ae7bf-160">Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ae7bf-161">Du kan använda cmdleten **set-AzureRmVmssStorageProfile** för att ange detta objekt.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ae7bf-162">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ae7bf-162">-Tag</span></span>
<span data-ttu-id="ae7bf-163">Anger de taggar som ska kopplas till VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="ae7bf-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ae7bf-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="ae7bf-165">Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="ae7bf-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ae7bf-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae7bf-167">Versal</span><span class="sxs-lookup"><span data-stu-id="ae7bf-167">Automatic</span></span>
- <span data-ttu-id="ae7bf-168">Manövrer</span><span class="sxs-lookup"><span data-stu-id="ae7bf-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bf-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae7bf-169">-Confirm</span></span>
<span data-ttu-id="ae7bf-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7bf-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7bf-171">-WhatIf</span></span>
<span data-ttu-id="ae7bf-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae7bf-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7bf-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7bf-174">CommonParameters</span></span>
<span data-ttu-id="ae7bf-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7bf-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7bf-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7bf-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae7bf-177">INPUTS</span></span>

### <span data-ttu-id="ae7bf-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae7bf-178">None</span></span>
<span data-ttu-id="ae7bf-179">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae7bf-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae7bf-180">OUTPUTS</span></span>

### <span data-ttu-id="ae7bf-181">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ae7bf-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ae7bf-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae7bf-182">NOTES</span></span>

## <span data-ttu-id="ae7bf-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae7bf-183">RELATED LINKS</span></span>

[<span data-ttu-id="ae7bf-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="ae7bf-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bf-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="ae7bf-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae7bf-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ae7bf-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ae7bf-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="ae7bf-188">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ae7bf-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


