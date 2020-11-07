---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930709"
---
# <span data-ttu-id="9f7aa-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9f7aa-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="9f7aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7aa-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f7aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f7aa-104">SYNTAX</span></span>

### <span data-ttu-id="9f7aa-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9f7aa-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f7aa-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f7aa-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f7aa-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f7aa-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f7aa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f7aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9f7aa-109">Cmdleten **New-AzureRmVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="9f7aa-110">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface och set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="9f7aa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f7aa-111">EXAMPLES</span></span>

### <span data-ttu-id="9f7aa-112">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="9f7aa-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="9f7aa-113">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="9f7aa-114">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9f7aa-115">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9f7aa-116">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="9f7aa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f7aa-117">PARAMETERS</span></span>

### <span data-ttu-id="9f7aa-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9f7aa-118">-AssignIdentity</span></span>
<span data-ttu-id="9f7aa-119">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="9f7aa-120">-AvailabilitySetId</span></span>
<span data-ttu-id="9f7aa-121">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="9f7aa-122">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzureRmAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="9f7aa-123">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7aa-124">-DefaultProfile</span></span>
<span data-ttu-id="9f7aa-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f7aa-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9f7aa-126">-IdentityId</span></span>
<span data-ttu-id="9f7aa-127">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9f7aa-128">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="9f7aa-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9f7aa-129">-IdentityType</span></span>
<span data-ttu-id="9f7aa-130">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f7aa-131">-LicenseType</span></span>
<span data-ttu-id="9f7aa-132">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-133">-Taggar</span><span class="sxs-lookup"><span data-stu-id="9f7aa-133">-Tags</span></span>
<span data-ttu-id="9f7aa-134">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="9f7aa-135">-VMName</span></span>
<span data-ttu-id="9f7aa-136">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="9f7aa-137">-VMSize</span></span>
<span data-ttu-id="9f7aa-138">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="9f7aa-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="9f7aa-139">-Zone</span></span>
<span data-ttu-id="9f7aa-140">Anger zon listan för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7aa-141">CommonParameters</span></span>
<span data-ttu-id="9f7aa-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7aa-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7aa-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7aa-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f7aa-144">INPUTS</span></span>

### <span data-ttu-id="9f7aa-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f7aa-145">None</span></span>
<span data-ttu-id="9f7aa-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9f7aa-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f7aa-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f7aa-147">OUTPUTS</span></span>

### <span data-ttu-id="9f7aa-148">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f7aa-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9f7aa-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f7aa-149">NOTES</span></span>

## <span data-ttu-id="9f7aa-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f7aa-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f7aa-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f7aa-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="9f7aa-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f7aa-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="9f7aa-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9f7aa-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="9f7aa-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f7aa-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


