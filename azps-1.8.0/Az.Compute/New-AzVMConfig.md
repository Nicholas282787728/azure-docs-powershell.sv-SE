---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754536"
---
# <span data-ttu-id="68ae1-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="68ae1-101">New-AzVMConfig</span></span>

## <span data-ttu-id="68ae1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="68ae1-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="68ae1-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="68ae1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68ae1-104">SYNTAX</span></span>

### <span data-ttu-id="68ae1-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="68ae1-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68ae1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ae1-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ae1-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ae1-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68ae1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68ae1-108">DESCRIPTION</span></span>
<span data-ttu-id="68ae1-109">Cmdleten **New-AzVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="68ae1-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="68ae1-110">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface och set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="68ae1-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="68ae1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68ae1-111">EXAMPLES</span></span>

### <span data-ttu-id="68ae1-112">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="68ae1-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="68ae1-113">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="68ae1-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="68ae1-114">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="68ae1-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="68ae1-115">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="68ae1-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="68ae1-116">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="68ae1-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="68ae1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68ae1-117">PARAMETERS</span></span>

### <span data-ttu-id="68ae1-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="68ae1-118">-AssignIdentity</span></span>
<span data-ttu-id="68ae1-119">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="68ae1-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="68ae1-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="68ae1-120">-AvailabilitySetId</span></span>
<span data-ttu-id="68ae1-121">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="68ae1-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="68ae1-122">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae1-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="68ae1-123">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="68ae1-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="68ae1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ae1-124">-DefaultProfile</span></span>
<span data-ttu-id="68ae1-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68ae1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ae1-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="68ae1-126">-EnableUltraSSD</span></span>
<span data-ttu-id="68ae1-127">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="68ae1-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="68ae1-128">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="68ae1-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="68ae1-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="68ae1-129">-IdentityId</span></span>
<span data-ttu-id="68ae1-130">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="68ae1-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="68ae1-131">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="68ae1-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="68ae1-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="68ae1-132">-IdentityType</span></span>
<span data-ttu-id="68ae1-133">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="68ae1-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="68ae1-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="68ae1-134">-LicenseType</span></span>
<span data-ttu-id="68ae1-135">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="68ae1-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="68ae1-136">-Taggar</span><span class="sxs-lookup"><span data-stu-id="68ae1-136">-Tags</span></span>
<span data-ttu-id="68ae1-137">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="68ae1-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="68ae1-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="68ae1-138">-VMName</span></span>
<span data-ttu-id="68ae1-139">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="68ae1-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="68ae1-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="68ae1-140">-VMSize</span></span>
<span data-ttu-id="68ae1-141">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="68ae1-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="68ae1-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="68ae1-142">-Zone</span></span>
<span data-ttu-id="68ae1-143">Anger listan över tillgänglighets zoner för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="68ae1-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="68ae1-144">De tillåtna värdena beror på regionens funktioner.</span><span class="sxs-lookup"><span data-stu-id="68ae1-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="68ae1-145">Tillåtna värden är normalt 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="68ae1-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="68ae1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ae1-146">CommonParameters</span></span>
<span data-ttu-id="68ae1-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ae1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ae1-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ae1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ae1-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68ae1-149">INPUTS</span></span>

### <span data-ttu-id="68ae1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="68ae1-150">System.String</span></span>

### <span data-ttu-id="68ae1-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="68ae1-151">System.String[]</span></span>

### <span data-ttu-id="68ae1-152">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="68ae1-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="68ae1-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68ae1-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68ae1-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68ae1-154">OUTPUTS</span></span>

### <span data-ttu-id="68ae1-155">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="68ae1-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="68ae1-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68ae1-156">NOTES</span></span>

## <span data-ttu-id="68ae1-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68ae1-157">RELATED LINKS</span></span>

[<span data-ttu-id="68ae1-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ae1-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="68ae1-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="68ae1-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="68ae1-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="68ae1-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="68ae1-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="68ae1-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


