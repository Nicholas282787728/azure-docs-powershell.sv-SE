---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579756"
---
# <span data-ttu-id="39dd0-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="39dd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="39dd0-103">Uppdaterar tillståndet för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="39dd0-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39dd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39dd0-104">SYNTAX</span></span>

### <span data-ttu-id="39dd0-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="39dd0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39dd0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="39dd0-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39dd0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39dd0-107">DESCRIPTION</span></span>
<span data-ttu-id="39dd0-108">Cmdleten **Update-AzureRmVM** uppdaterar tillståndet för en virtuell Azure-dator till tillståndet för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="39dd0-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="39dd0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39dd0-109">EXAMPLES</span></span>

### <span data-ttu-id="39dd0-110">Exempel 1: uppdatera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="39dd0-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="39dd0-111">Det här kommandot uppdaterar den virtuella datorn $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="39dd0-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="39dd0-112">Kommandot uppdaterar det med hjälp av det virtuella dator objekt som lagras i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="39dd0-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="39dd0-113">Använd cmdleten **Get-AzureRmVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="39dd0-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="39dd0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39dd0-114">PARAMETERS</span></span>

### <span data-ttu-id="39dd0-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="39dd0-115">-AssignIdentity</span></span>
<span data-ttu-id="39dd0-116">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="39dd0-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="39dd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dd0-117">-DefaultProfile</span></span>
<span data-ttu-id="39dd0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39dd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39dd0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="39dd0-119">-Id</span></span>
<span data-ttu-id="39dd0-120">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="39dd0-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="39dd0-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="39dd0-121">-IdentityType</span></span>
<span data-ttu-id="39dd0-122">Den typ av identitet som används för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="39dd0-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="39dd0-123">För närvarande är den enda typ som stöds ' SystemAssigned ', vilket implicit skapar en identitet.</span><span class="sxs-lookup"><span data-stu-id="39dd0-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39dd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39dd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="39dd0-125">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="39dd0-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dd0-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="39dd0-126">-Tags</span></span>
<span data-ttu-id="39dd0-127">Anger resurser och resurs grupper med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="39dd0-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="39dd0-128">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="39dd0-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="39dd0-129">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="39dd0-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="39dd0-130">-VM</span><span class="sxs-lookup"><span data-stu-id="39dd0-130">-VM</span></span>
<span data-ttu-id="39dd0-131">Anger ett lokalt virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="39dd0-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="39dd0-132">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="39dd0-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="39dd0-133">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="39dd0-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="39dd0-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39dd0-134">-Confirm</span></span>
<span data-ttu-id="39dd0-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39dd0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39dd0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39dd0-136">-WhatIf</span></span>
<span data-ttu-id="39dd0-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39dd0-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="39dd0-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39dd0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39dd0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dd0-139">CommonParameters</span></span>
<span data-ttu-id="39dd0-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39dd0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dd0-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39dd0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dd0-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39dd0-142">INPUTS</span></span>

## <span data-ttu-id="39dd0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39dd0-143">OUTPUTS</span></span>

## <span data-ttu-id="39dd0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39dd0-144">NOTES</span></span>

## <span data-ttu-id="39dd0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39dd0-145">RELATED LINKS</span></span>

[<span data-ttu-id="39dd0-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="39dd0-147">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="39dd0-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="39dd0-149">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="39dd0-150">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="39dd0-151">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39dd0-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="39dd0-152">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="39dd0-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


