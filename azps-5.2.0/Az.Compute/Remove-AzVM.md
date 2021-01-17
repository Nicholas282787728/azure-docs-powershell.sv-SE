---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402000"
---
# <span data-ttu-id="d58bd-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-101">Remove-AzVM</span></span>

## <span data-ttu-id="d58bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d58bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d58bd-103">Tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="d58bd-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="d58bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d58bd-104">SYNTAX</span></span>

### <span data-ttu-id="d58bd-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="d58bd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58bd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d58bd-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d58bd-107">DESCRIPTION</span></span>
<span data-ttu-id="d58bd-108">Cmdleten **Remove-AzVM** tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="d58bd-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="d58bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d58bd-109">EXAMPLES</span></span>

### <span data-ttu-id="d58bd-110">Exempel 1: ta bort en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d58bd-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d58bd-111">Det här kommandot tar bort den virtuella datorn med namnet VirtualMachine07 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d58bd-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d58bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d58bd-112">PARAMETERS</span></span>

### <span data-ttu-id="d58bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d58bd-113">-AsJob</span></span>
<span data-ttu-id="d58bd-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d58bd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d58bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58bd-115">-DefaultProfile</span></span>
<span data-ttu-id="d58bd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d58bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d58bd-117">-Force</span></span>
<span data-ttu-id="d58bd-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d58bd-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58bd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d58bd-119">-Id</span></span>
<span data-ttu-id="d58bd-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d58bd-120">The resource group name.</span></span>

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

### <span data-ttu-id="d58bd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d58bd-121">-Name</span></span>
<span data-ttu-id="d58bd-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d58bd-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58bd-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d58bd-123">-NoWait</span></span>
<span data-ttu-id="d58bd-124">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="d58bd-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d58bd-125">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="d58bd-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d58bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="d58bd-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d58bd-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d58bd-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d58bd-128">-Confirm</span></span>
<span data-ttu-id="d58bd-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d58bd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58bd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58bd-130">-WhatIf</span></span>
<span data-ttu-id="d58bd-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d58bd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58bd-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d58bd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58bd-133">CommonParameters</span></span>
<span data-ttu-id="d58bd-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58bd-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d58bd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58bd-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d58bd-136">INPUTS</span></span>

### <span data-ttu-id="d58bd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d58bd-137">System.String</span></span>

## <span data-ttu-id="d58bd-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d58bd-138">OUTPUTS</span></span>

### <span data-ttu-id="d58bd-139">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d58bd-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="d58bd-140">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d58bd-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d58bd-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d58bd-141">NOTES</span></span>

## <span data-ttu-id="d58bd-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d58bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="d58bd-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d58bd-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d58bd-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d58bd-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d58bd-147">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d58bd-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d58bd-148">Update-AzVM</span></span>](./Update-AzVM.md)


