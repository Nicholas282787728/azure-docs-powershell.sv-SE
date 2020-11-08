---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260144"
---
# <span data-ttu-id="97461-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="97461-101">New-AzVMConfig</span></span>

## <span data-ttu-id="97461-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97461-102">SYNOPSIS</span></span>
<span data-ttu-id="97461-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="97461-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="97461-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97461-104">SYNTAX</span></span>

### <span data-ttu-id="97461-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="97461-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97461-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="97461-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97461-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97461-107">DESCRIPTION</span></span>
<span data-ttu-id="97461-108">Cmdleten **New-AzVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="97461-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="97461-109">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface och set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="97461-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="97461-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97461-110">EXAMPLES</span></span>

### <span data-ttu-id="97461-111">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="97461-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="97461-112">Det första kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="97461-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="97461-113">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="97461-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="97461-114">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="97461-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="97461-115">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="97461-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="97461-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97461-116">PARAMETERS</span></span>

### <span data-ttu-id="97461-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="97461-117">-AvailabilitySetId</span></span>
<span data-ttu-id="97461-118">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="97461-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="97461-119">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97461-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="97461-120">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="97461-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="97461-121">Virtuella datorer som anges i samma tillgänglighets uppsättning tilldelas olika noder för att maximera tillgängligheten.</span><span class="sxs-lookup"><span data-stu-id="97461-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="97461-122">Mer information om tillgänglighets uppsättningar finns i [Hantera tillgänglighet för virtuella datorer](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="97461-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="97461-123">För mer information om planerat underhåll av Azure, se [planerat underhåll för virtuella datorer i Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="97461-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="97461-124">För närvarande kan en virtuell dator bara läggas till i tillgänglighets uppsättningen när den skapas.</span><span class="sxs-lookup"><span data-stu-id="97461-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="97461-125">Den tillgänglighets uppsättning som den virtuella datorn läggs till ska vara under samma resurs grupp som tillgänglighets uppsättnings resursen.</span><span class="sxs-lookup"><span data-stu-id="97461-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="97461-126">Det går inte att lägga till en befintlig virtuell dator i en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="97461-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="97461-127">Den här egenskapen får inte finnas tillsammans med en egenskap som inte är null. virtualMachineScaleSet reference.</span><span class="sxs-lookup"><span data-stu-id="97461-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97461-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97461-128">-DefaultProfile</span></span>
<span data-ttu-id="97461-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97461-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97461-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="97461-130">-EnableUltraSSD</span></span>
<span data-ttu-id="97461-131">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="97461-132">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="97461-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="97461-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="97461-133">-EvictionPolicy</span></span>
<span data-ttu-id="97461-134">Borttagnings princip för den virtuella Azure-datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="97461-135">Värden som stöds är "frigör" och "ta bort".</span><span class="sxs-lookup"><span data-stu-id="97461-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="97461-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="97461-136">-HostId</span></span>
<span data-ttu-id="97461-137">ID för värden</span><span class="sxs-lookup"><span data-stu-id="97461-137">The Id of Host</span></span>

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

### <span data-ttu-id="97461-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="97461-138">-IdentityId</span></span>
<span data-ttu-id="97461-139">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="97461-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="97461-140">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="97461-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="97461-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="97461-141">-IdentityType</span></span>
<span data-ttu-id="97461-142">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="97461-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97461-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="97461-143">-LicenseType</span></span>
<span data-ttu-id="97461-144">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="97461-144">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97461-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="97461-145">-MaxPrice</span></span>
<span data-ttu-id="97461-146">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="97461-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="97461-147">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="97461-147">This price is in US Dollars.</span></span> <span data-ttu-id="97461-148">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="97461-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="97461-149">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="97461-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="97461-150">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="97461-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="97461-151">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="97461-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="97461-152">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="97461-152">Example: 0.01538.</span></span>  <span data-ttu-id="97461-153">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="97461-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="97461-154">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="97461-154">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97461-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="97461-155">-EncryptionAtHost</span></span>
<span data-ttu-id="97461-156">Egenskapen EncryptionAtHost kan användas av användaren i begäran för att aktivera eller inaktivera värd krypteringen för den virtuella datorn eller skalan för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97461-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="97461-157">Detta aktiverar kryptering för alla diskar inklusive resurs/Temp-disk på själva värden.</span><span class="sxs-lookup"><span data-stu-id="97461-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="97461-158">Standard: krypteringen på värden kommer att inaktive ras såvida den inte är inställd på True för resursen.</span><span class="sxs-lookup"><span data-stu-id="97461-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="97461-159">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="97461-159">-Priority</span></span>
<span data-ttu-id="97461-160">Prioriteten för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="97461-161">Endast värden som stöds är "regular", "dekor" och "Low".</span><span class="sxs-lookup"><span data-stu-id="97461-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="97461-162">' Regular ' är för vanlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97461-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="97461-163">"Plats" gäller för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97461-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="97461-164">"Low" är också för en virtuell dator, men ersätts med ' dekor ".</span><span class="sxs-lookup"><span data-stu-id="97461-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="97461-165">Använd "plats" istället för "Low".</span><span class="sxs-lookup"><span data-stu-id="97461-165">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="97461-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="97461-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="97461-167">Resurs-ID för närhets gruppen som ska användas med den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="97461-168">-Taggar</span><span class="sxs-lookup"><span data-stu-id="97461-168">-Tags</span></span>
<span data-ttu-id="97461-169">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="97461-169">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97461-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="97461-170">-VMName</span></span>
<span data-ttu-id="97461-171">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-171">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97461-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="97461-172">-VMSize</span></span>
<span data-ttu-id="97461-173">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="97461-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="97461-174">-VmssId</span></span>
<span data-ttu-id="97461-175">ID för den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="97461-175">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="97461-176">-Zone</span><span class="sxs-lookup"><span data-stu-id="97461-176">-Zone</span></span>
<span data-ttu-id="97461-177">Anger listan över tillgänglighets zoner för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97461-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="97461-178">De tillåtna värdena beror på regionens funktioner.</span><span class="sxs-lookup"><span data-stu-id="97461-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="97461-179">Tillåtna värden är normalt 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="97461-179">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="97461-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97461-180">CommonParameters</span></span>
<span data-ttu-id="97461-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97461-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97461-182">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97461-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97461-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97461-183">INPUTS</span></span>

### <span data-ttu-id="97461-184">System. String</span><span class="sxs-lookup"><span data-stu-id="97461-184">System.String</span></span>

### <span data-ttu-id="97461-185">System. string []</span><span class="sxs-lookup"><span data-stu-id="97461-185">System.String[]</span></span>

### <span data-ttu-id="97461-186">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="97461-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="97461-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97461-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97461-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97461-188">OUTPUTS</span></span>

### <span data-ttu-id="97461-189">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97461-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="97461-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97461-190">NOTES</span></span>

## <span data-ttu-id="97461-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97461-191">RELATED LINKS</span></span>

[<span data-ttu-id="97461-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="97461-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="97461-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="97461-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="97461-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="97461-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="97461-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="97461-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


