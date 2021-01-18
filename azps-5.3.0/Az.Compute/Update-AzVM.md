---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526560"
---
# <span data-ttu-id="6ad8b-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-101">Update-AzVM</span></span>

## <span data-ttu-id="6ad8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ad8b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad8b-103">Uppdaterar tillståndet för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="6ad8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ad8b-104">SYNTAX</span></span>

### <span data-ttu-id="6ad8b-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="6ad8b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad8b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad8b-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad8b-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6ad8b-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad8b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ad8b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad8b-109">Cmdleten **Update-AzVM** uppdaterar tillståndet för en virtuell Azure-dator till tillståndet för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="6ad8b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ad8b-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad8b-111">Exempel 1: uppdatera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="6ad8b-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6ad8b-112">Det här kommandot uppdaterar den virtuella datorn $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="6ad8b-113">Kommandot uppdaterar det med hjälp av det virtuella dator objekt som lagras i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6ad8b-114">Använd cmdleten **Get-AzVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="6ad8b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ad8b-115">PARAMETERS</span></span>

### <span data-ttu-id="6ad8b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ad8b-116">-AsJob</span></span>
<span data-ttu-id="6ad8b-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6ad8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad8b-118">-DefaultProfile</span></span>
<span data-ttu-id="6ad8b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad8b-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="6ad8b-120">-HostId</span></span>
<span data-ttu-id="6ad8b-121">ID för värden</span><span class="sxs-lookup"><span data-stu-id="6ad8b-121">The Id of Host</span></span>

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

### <span data-ttu-id="6ad8b-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="6ad8b-122">-EncryptionAtHost</span></span>
<span data-ttu-id="6ad8b-123">Egenskapen EncryptionAtHost kan användas av användaren i begäran för att aktivera eller inaktivera värd krypteringen för den virtuella datorn eller skalan för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="6ad8b-124">Detta aktiverar kryptering för alla diskar inklusive resurs/Temp-disk på själva värden.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="6ad8b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="6ad8b-125">-Id</span></span>
<span data-ttu-id="6ad8b-126">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad8b-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6ad8b-127">-IdentityId</span></span>
<span data-ttu-id="6ad8b-128">Anger listan över användar identiteter som är associerade med den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="6ad8b-129">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="6ad8b-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6ad8b-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6ad8b-130">-IdentityType</span></span>
<span data-ttu-id="6ad8b-131">Den typ av identitet som används för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="6ad8b-132">Giltiga värden är SystemAssigned, UserAssigned, SystemAssignedUserAssigned och none.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="6ad8b-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="6ad8b-133">-MaxPrice</span></span>
<span data-ttu-id="6ad8b-134">Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="6ad8b-135">Priset är i USD.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-135">This price is in US Dollars.</span></span> <span data-ttu-id="6ad8b-136">Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="6ad8b-137">Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="6ad8b-138">MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6ad8b-139">Möjliga värden är: ett decimal tal större än noll.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6ad8b-140">Exempel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-140">Example: 0.01538.</span></span>  <span data-ttu-id="6ad8b-141">-1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6ad8b-142">Standard priset för max är-1 om det inte tillhandahålls av dig.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6ad8b-143">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6ad8b-143">-NoWait</span></span>
<span data-ttu-id="6ad8b-144">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6ad8b-145">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6ad8b-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6ad8b-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="6ad8b-147">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="6ad8b-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6ad8b-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6ad8b-149">Resurs-ID för närhets gruppen som ska användas med den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="6ad8b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad8b-150">-ResourceGroupName</span></span>
<span data-ttu-id="6ad8b-151">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad8b-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6ad8b-152">-Tag</span></span>
<span data-ttu-id="6ad8b-153">Anger resurser och resurs grupper med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="6ad8b-154">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="6ad8b-155">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="6ad8b-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="6ad8b-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="6ad8b-157">Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="6ad8b-158">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="6ad8b-159">-VM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-159">-VM</span></span>
<span data-ttu-id="6ad8b-160">Anger ett lokalt virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="6ad8b-161">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="6ad8b-162">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad8b-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ad8b-163">-Confirm</span></span>
<span data-ttu-id="6ad8b-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad8b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad8b-165">-WhatIf</span></span>
<span data-ttu-id="6ad8b-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad8b-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="6ad8b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad8b-168">CommonParameters</span></span>
<span data-ttu-id="6ad8b-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad8b-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ad8b-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad8b-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ad8b-171">INPUTS</span></span>

### <span data-ttu-id="6ad8b-172">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad8b-172">System.String</span></span>

### <span data-ttu-id="6ad8b-173">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6ad8b-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6ad8b-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ad8b-174">System.Boolean</span></span>

## <span data-ttu-id="6ad8b-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ad8b-175">OUTPUTS</span></span>

### <span data-ttu-id="6ad8b-176">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6ad8b-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6ad8b-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ad8b-177">NOTES</span></span>

## <span data-ttu-id="6ad8b-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ad8b-178">RELATED LINKS</span></span>

[<span data-ttu-id="6ad8b-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6ad8b-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6ad8b-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="6ad8b-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6ad8b-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="6ad8b-184">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ad8b-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6ad8b-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6ad8b-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


