---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089170"
---
# <span data-ttu-id="db4f2-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="db4f2-101">New-AzVMConfig</span></span>

## <span data-ttu-id="db4f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="db4f2-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="db4f2-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="db4f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db4f2-104">SYNTAX</span></span>

### <span data-ttu-id="db4f2-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db4f2-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4f2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="db4f2-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4f2-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="db4f2-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db4f2-108">DESCRIPTION</span></span>
<span data-ttu-id="db4f2-109">Cmdleten **New-AzVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="db4f2-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="db4f2-110">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface och set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="db4f2-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="db4f2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db4f2-111">EXAMPLES</span></span>

### <span data-ttu-id="db4f2-112">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="db4f2-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="db4f2-113">Det första kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="db4f2-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="db4f2-114">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="db4f2-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db4f2-115">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="db4f2-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="db4f2-116">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="db4f2-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="db4f2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db4f2-117">PARAMETERS</span></span>

### <span data-ttu-id="db4f2-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="db4f2-118">-AssignIdentity</span></span>
<span data-ttu-id="db4f2-119">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="db4f2-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="db4f2-120">-AvailabilitySetId</span></span>
<span data-ttu-id="db4f2-121">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db4f2-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="db4f2-122">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db4f2-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="db4f2-123">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="db4f2-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="db4f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4f2-124">-DefaultProfile</span></span>
<span data-ttu-id="db4f2-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db4f2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4f2-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="db4f2-126">-EnableUltraSSD</span></span>
<span data-ttu-id="db4f2-127">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="db4f2-128">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="db4f2-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="db4f2-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="db4f2-129">-EvictionPolicy</span></span>
<span data-ttu-id="db4f2-130">Borttagnings principen för den virtuella datorn med den högsta prioriteten.</span><span class="sxs-lookup"><span data-stu-id="db4f2-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="db4f2-131">Det enda värdet som stöds är "frigör".</span><span class="sxs-lookup"><span data-stu-id="db4f2-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="db4f2-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="db4f2-132">-HostId</span></span>
<span data-ttu-id="db4f2-133">ID för värden</span><span class="sxs-lookup"><span data-stu-id="db4f2-133">The Id of Host</span></span>

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

### <span data-ttu-id="db4f2-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="db4f2-134">-IdentityId</span></span>
<span data-ttu-id="db4f2-135">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db4f2-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="db4f2-136">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="db4f2-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="db4f2-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="db4f2-137">-IdentityType</span></span>
<span data-ttu-id="db4f2-138">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="db4f2-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="db4f2-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="db4f2-139">-LicenseType</span></span>
<span data-ttu-id="db4f2-140">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="db4f2-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="db4f2-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="db4f2-141">-MaxPrice</span></span>
<span data-ttu-id="db4f2-142">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="db4f2-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="db4f2-143">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="db4f2-143">This price is in US Dollars.</span></span> <span data-ttu-id="db4f2-144">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="db4f2-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="db4f2-145">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="db4f2-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="db4f2-146">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="db4f2-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="db4f2-147">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="db4f2-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="db4f2-148">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="db4f2-148">Example: 0.01538.</span></span>  <span data-ttu-id="db4f2-149">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="db4f2-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="db4f2-150">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="db4f2-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="db4f2-151">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="db4f2-151">-Priority</span></span>
<span data-ttu-id="db4f2-152">Prioriteten för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="db4f2-153">Endast värden som stöds är "regular", "dekor" och "Low".</span><span class="sxs-lookup"><span data-stu-id="db4f2-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="db4f2-154">' Regular ' är för vanlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="db4f2-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="db4f2-155">"Plats" gäller för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="db4f2-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="db4f2-156">"Low" är också för en virtuell dator, men ersätts med ' dekor ".</span><span class="sxs-lookup"><span data-stu-id="db4f2-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="db4f2-157">Använd "plats" istället för "Low".</span><span class="sxs-lookup"><span data-stu-id="db4f2-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="db4f2-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="db4f2-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="db4f2-159">Resurs-ID för närhets gruppen som ska användas med den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="db4f2-160">-Taggar</span><span class="sxs-lookup"><span data-stu-id="db4f2-160">-Tags</span></span>
<span data-ttu-id="db4f2-161">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="db4f2-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="db4f2-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="db4f2-162">-VMName</span></span>
<span data-ttu-id="db4f2-163">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="db4f2-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="db4f2-164">-VMSize</span></span>
<span data-ttu-id="db4f2-165">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="db4f2-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="db4f2-166">-VmssId</span></span>
<span data-ttu-id="db4f2-167">ID för den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="db4f2-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="db4f2-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="db4f2-168">-Zone</span></span>
<span data-ttu-id="db4f2-169">Anger listan över tillgänglighets zoner för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="db4f2-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="db4f2-170">De tillåtna värdena beror på regionens funktioner.</span><span class="sxs-lookup"><span data-stu-id="db4f2-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="db4f2-171">Tillåtna värden är normalt 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="db4f2-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="db4f2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4f2-172">CommonParameters</span></span>
<span data-ttu-id="db4f2-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4f2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4f2-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db4f2-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4f2-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db4f2-175">INPUTS</span></span>

### <span data-ttu-id="db4f2-176">System. String</span><span class="sxs-lookup"><span data-stu-id="db4f2-176">System.String</span></span>

### <span data-ttu-id="db4f2-177">System. string []</span><span class="sxs-lookup"><span data-stu-id="db4f2-177">System.String[]</span></span>

### <span data-ttu-id="db4f2-178">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="db4f2-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="db4f2-179">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db4f2-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db4f2-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db4f2-180">OUTPUTS</span></span>

### <span data-ttu-id="db4f2-181">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db4f2-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="db4f2-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db4f2-182">NOTES</span></span>

## <span data-ttu-id="db4f2-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db4f2-183">RELATED LINKS</span></span>

[<span data-ttu-id="db4f2-184">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="db4f2-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="db4f2-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="db4f2-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="db4f2-186">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="db4f2-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="db4f2-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="db4f2-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


