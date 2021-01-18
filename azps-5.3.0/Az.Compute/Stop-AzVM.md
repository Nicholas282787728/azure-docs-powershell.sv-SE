---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524434"
---
# <span data-ttu-id="77735-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-101">Stop-AzVM</span></span>

## <span data-ttu-id="77735-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77735-102">SYNOPSIS</span></span>
<span data-ttu-id="77735-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="77735-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="77735-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77735-104">SYNTAX</span></span>

### <span data-ttu-id="77735-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="77735-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77735-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="77735-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77735-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77735-107">DESCRIPTION</span></span>
<span data-ttu-id="77735-108">Cmdleten **Stop-AzVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="77735-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="77735-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77735-109">EXAMPLES</span></span>

### <span data-ttu-id="77735-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="77735-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="77735-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="77735-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="77735-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77735-112">PARAMETERS</span></span>

### <span data-ttu-id="77735-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77735-113">-AsJob</span></span>
<span data-ttu-id="77735-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="77735-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="77735-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77735-115">-DefaultProfile</span></span>
<span data-ttu-id="77735-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77735-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77735-117">-Force</span><span class="sxs-lookup"><span data-stu-id="77735-117">-Force</span></span>
<span data-ttu-id="77735-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="77735-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77735-119">-ID</span><span class="sxs-lookup"><span data-stu-id="77735-119">-Id</span></span>
<span data-ttu-id="77735-120">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="77735-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="77735-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="77735-121">-Name</span></span>
<span data-ttu-id="77735-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="77735-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77735-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="77735-123">-NoWait</span></span>
<span data-ttu-id="77735-124">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="77735-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="77735-125">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="77735-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="77735-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77735-126">-ResourceGroupName</span></span>
<span data-ttu-id="77735-127">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="77735-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="77735-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="77735-128">-SkipShutdown</span></span>
<span data-ttu-id="77735-129">Så här efterfrågar du icke-städade VM-avstängning när VM-etableringen behålls.</span><span class="sxs-lookup"><span data-stu-id="77735-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="77735-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="77735-130">-StayProvisioned</span></span>
<span data-ttu-id="77735-131">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="77735-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="77735-132">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="77735-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="77735-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77735-133">-Confirm</span></span>
<span data-ttu-id="77735-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77735-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77735-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77735-135">-WhatIf</span></span>
<span data-ttu-id="77735-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77735-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77735-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77735-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77735-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77735-138">CommonParameters</span></span>
<span data-ttu-id="77735-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77735-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77735-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77735-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77735-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77735-141">INPUTS</span></span>

### <span data-ttu-id="77735-142">System. String</span><span class="sxs-lookup"><span data-stu-id="77735-142">System.String</span></span>

## <span data-ttu-id="77735-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77735-143">OUTPUTS</span></span>

### <span data-ttu-id="77735-144">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="77735-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="77735-145">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="77735-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="77735-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77735-146">NOTES</span></span>

## <span data-ttu-id="77735-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77735-147">RELATED LINKS</span></span>

[<span data-ttu-id="77735-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="77735-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="77735-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="77735-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="77735-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="77735-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="77735-153">Update-AzVM</span></span>](./Update-AzVM.md)


