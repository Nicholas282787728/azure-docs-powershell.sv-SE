---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580264"
---
# <span data-ttu-id="9e85c-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9e85c-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="9e85c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e85c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e85c-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="9e85c-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e85c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e85c-104">SYNTAX</span></span>

### <span data-ttu-id="9e85c-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9e85c-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e85c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e85c-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e85c-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e85c-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e85c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e85c-108">DESCRIPTION</span></span>
<span data-ttu-id="9e85c-109">Cmdleten **New-AzureRmVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="9e85c-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="9e85c-110">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface och set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="9e85c-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="9e85c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e85c-111">EXAMPLES</span></span>

### <span data-ttu-id="9e85c-112">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="9e85c-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="9e85c-113">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="9e85c-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9e85c-114">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="9e85c-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9e85c-115">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="9e85c-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9e85c-116">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9e85c-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="9e85c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e85c-117">PARAMETERS</span></span>

### <span data-ttu-id="9e85c-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9e85c-118">-AssignIdentity</span></span>
<span data-ttu-id="9e85c-119">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9e85c-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="9e85c-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="9e85c-120">-AvailabilitySetId</span></span>
<span data-ttu-id="9e85c-121">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9e85c-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="9e85c-122">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzureRmAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e85c-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="9e85c-123">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="9e85c-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="9e85c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e85c-124">-DefaultProfile</span></span>
<span data-ttu-id="9e85c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e85c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e85c-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="9e85c-126">-EnableUltraSSD</span></span>
<span data-ttu-id="9e85c-127">Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9e85c-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="9e85c-128">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="9e85c-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="9e85c-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9e85c-129">-IdentityId</span></span>
<span data-ttu-id="9e85c-130">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9e85c-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9e85c-131">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="9e85c-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="9e85c-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9e85c-132">-IdentityType</span></span>
<span data-ttu-id="9e85c-133">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="9e85c-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="9e85c-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9e85c-134">-LicenseType</span></span>
<span data-ttu-id="9e85c-135">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="9e85c-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="9e85c-136">-Taggar</span><span class="sxs-lookup"><span data-stu-id="9e85c-136">-Tags</span></span>
<span data-ttu-id="9e85c-137">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="9e85c-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="9e85c-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e85c-138">-VMName</span></span>
<span data-ttu-id="9e85c-139">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9e85c-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="9e85c-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="9e85c-140">-VMSize</span></span>
<span data-ttu-id="9e85c-141">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9e85c-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="9e85c-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e85c-142">-Zone</span></span>
<span data-ttu-id="9e85c-143">Anger zon listan för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9e85c-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="9e85c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e85c-144">CommonParameters</span></span>
<span data-ttu-id="9e85c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e85c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e85c-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e85c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e85c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e85c-147">INPUTS</span></span>

### <span data-ttu-id="9e85c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9e85c-148">System.String</span></span>

### <span data-ttu-id="9e85c-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="9e85c-149">System.String[]</span></span>

### <span data-ttu-id="9e85c-150">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9e85c-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e85c-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e85c-151">OUTPUTS</span></span>

### <span data-ttu-id="9e85c-152">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e85c-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9e85c-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e85c-153">NOTES</span></span>

## <span data-ttu-id="9e85c-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e85c-154">RELATED LINKS</span></span>

[<span data-ttu-id="9e85c-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9e85c-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="9e85c-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9e85c-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="9e85c-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9e85c-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="9e85c-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9e85c-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


