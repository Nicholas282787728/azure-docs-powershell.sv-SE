---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923010"
---
# <span data-ttu-id="43ed2-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-101">Update-AzVM</span></span>

## <span data-ttu-id="43ed2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="43ed2-103">Uppdaterar tillståndet för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="43ed2-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="43ed2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43ed2-104">SYNTAX</span></span>

### <span data-ttu-id="43ed2-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="43ed2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43ed2-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="43ed2-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43ed2-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="43ed2-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ed2-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="43ed2-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ed2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43ed2-109">DESCRIPTION</span></span>
<span data-ttu-id="43ed2-110">Cmdleten **Update-AzVM** uppdaterar tillståndet för en virtuell Azure-dator till tillståndet för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="43ed2-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="43ed2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43ed2-111">EXAMPLES</span></span>

### <span data-ttu-id="43ed2-112">Exempel 1: uppdatera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="43ed2-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="43ed2-113">Det här kommandot uppdaterar den virtuella datorn $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="43ed2-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="43ed2-114">Kommandot uppdaterar det med hjälp av det virtuella dator objekt som lagras i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="43ed2-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="43ed2-115">Använd cmdleten **Get-AzVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="43ed2-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="43ed2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43ed2-116">PARAMETERS</span></span>

### <span data-ttu-id="43ed2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43ed2-117">-AsJob</span></span>
<span data-ttu-id="43ed2-118">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="43ed2-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="43ed2-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="43ed2-119">-AssignIdentity</span></span>
<span data-ttu-id="43ed2-120">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="43ed2-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="43ed2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ed2-121">-DefaultProfile</span></span>
<span data-ttu-id="43ed2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43ed2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ed2-123">-ID</span><span class="sxs-lookup"><span data-stu-id="43ed2-123">-Id</span></span>
<span data-ttu-id="43ed2-124">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43ed2-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="43ed2-125">-IdentityId</span></span>
<span data-ttu-id="43ed2-126">Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="43ed2-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="43ed2-127">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="43ed2-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="43ed2-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="43ed2-128">-IdentityType</span></span>
<span data-ttu-id="43ed2-129">Den typ av identitet som används för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="43ed2-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="43ed2-130">För närvarande är den enda typ som stöds ' SystemAssigned ', vilket implicit skapar en identitet.</span><span class="sxs-lookup"><span data-stu-id="43ed2-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="43ed2-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="43ed2-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="43ed2-132">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="43ed2-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="43ed2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ed2-133">-ResourceGroupName</span></span>
<span data-ttu-id="43ed2-134">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="43ed2-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="43ed2-135">-Tag</span></span>
<span data-ttu-id="43ed2-136">Anger resurser och resurs grupper med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="43ed2-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="43ed2-137">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="43ed2-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="43ed2-138">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="43ed2-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-139">-VM</span><span class="sxs-lookup"><span data-stu-id="43ed2-139">-VM</span></span>
<span data-ttu-id="43ed2-140">Anger ett lokalt virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="43ed2-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="43ed2-141">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="43ed2-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="43ed2-142">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="43ed2-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43ed2-143">-Confirm</span></span>
<span data-ttu-id="43ed2-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43ed2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ed2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ed2-145">-WhatIf</span></span>
<span data-ttu-id="43ed2-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43ed2-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="43ed2-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43ed2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ed2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ed2-148">CommonParameters</span></span>
<span data-ttu-id="43ed2-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ed2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ed2-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ed2-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ed2-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43ed2-151">INPUTS</span></span>

### <span data-ttu-id="43ed2-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="43ed2-152">PSVirtualMachine</span></span>
<span data-ttu-id="43ed2-153">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="43ed2-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="43ed2-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43ed2-154">OUTPUTS</span></span>

### <span data-ttu-id="43ed2-155">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="43ed2-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="43ed2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43ed2-156">NOTES</span></span>

## <span data-ttu-id="43ed2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43ed2-157">RELATED LINKS</span></span>

[<span data-ttu-id="43ed2-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="43ed2-159">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="43ed2-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="43ed2-161">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="43ed2-162">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="43ed2-163">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="43ed2-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="43ed2-164">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="43ed2-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


