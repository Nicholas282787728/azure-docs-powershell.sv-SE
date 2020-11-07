---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917177"
---
# <span data-ttu-id="b8c8b-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-101">Update-AzVM</span></span>

## <span data-ttu-id="b8c8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c8b-103">Uppdaterar tillståndet för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="b8c8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8c8b-104">SYNTAX</span></span>

### <span data-ttu-id="b8c8b-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8c8b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c8b-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8c8b-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c8b-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8c8b-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c8b-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b8c8b-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c8b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8c8b-109">DESCRIPTION</span></span>
<span data-ttu-id="b8c8b-110">Cmdleten **Update-AzVM** uppdaterar tillståndet för en virtuell Azure-dator till tillståndet för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="b8c8b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8c8b-111">EXAMPLES</span></span>

### <span data-ttu-id="b8c8b-112">Exempel 1: uppdatera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b8c8b-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b8c8b-113">Det här kommandot uppdaterar den virtuella datorn $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="b8c8b-114">Kommandot uppdaterar det med hjälp av det virtuella dator objekt som lagras i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b8c8b-115">Använd cmdleten **Get-AzVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="b8c8b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8c8b-116">PARAMETERS</span></span>

### <span data-ttu-id="b8c8b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c8b-117">-AsJob</span></span>
<span data-ttu-id="b8c8b-118">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b8c8b-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c8b-119">-AssignIdentity</span></span>
<span data-ttu-id="b8c8b-120">Ange den systemtilldelade identiteten för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="b8c8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c8b-121">-DefaultProfile</span></span>
<span data-ttu-id="b8c8b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c8b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b8c8b-123">-Id</span></span>
<span data-ttu-id="b8c8b-124">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b8c8b-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="b8c8b-125">-IdentityId</span></span>
<span data-ttu-id="b8c8b-126">Anger listan över användar identiteter som är associerade med den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="b8c8b-127">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="b8c8b-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b8c8b-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b8c8b-128">-IdentityType</span></span>
<span data-ttu-id="b8c8b-129">Den typ av identitet som används för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="b8c8b-130">Giltiga värden är SystemAssigned, UserAssigned, SystemAssignedUserAssigned och none.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="b8c8b-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b8c8b-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="b8c8b-132">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="b8c8b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c8b-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8c8b-134">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c8b-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b8c8b-135">-Tag</span></span>
<span data-ttu-id="b8c8b-136">Anger resurser och resurs grupper med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b8c8b-137">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b8c8b-138">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="b8c8b-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="b8c8b-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="b8c8b-140">Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="b8c8b-141">Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till på en virtuell dator om den här egenskapen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="b8c8b-142">-VM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-142">-VM</span></span>
<span data-ttu-id="b8c8b-143">Anger ett lokalt virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="b8c8b-144">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b8c8b-145">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="b8c8b-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8c8b-146">-Confirm</span></span>
<span data-ttu-id="b8c8b-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c8b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c8b-148">-WhatIf</span></span>
<span data-ttu-id="b8c8b-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c8b-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c8b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c8b-151">CommonParameters</span></span>
<span data-ttu-id="b8c8b-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c8b-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c8b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c8b-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8c8b-154">INPUTS</span></span>

### <span data-ttu-id="b8c8b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b8c8b-155">System.String</span></span>

### <span data-ttu-id="b8c8b-156">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b8c8b-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b8c8b-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8c8b-157">System.Boolean</span></span>

## <span data-ttu-id="b8c8b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8c8b-158">OUTPUTS</span></span>

### <span data-ttu-id="b8c8b-159">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b8c8b-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b8c8b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8c8b-160">NOTES</span></span>

## <span data-ttu-id="b8c8b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8c8b-161">RELATED LINKS</span></span>

[<span data-ttu-id="b8c8b-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b8c8b-163">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b8c8b-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b8c8b-165">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b8c8b-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b8c8b-167">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8c8b-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b8c8b-168">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b8c8b-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


