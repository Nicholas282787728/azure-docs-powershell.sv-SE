---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270002"
---
# <span data-ttu-id="8f1a0-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-101">Stop-AzVM</span></span>

## <span data-ttu-id="8f1a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1a0-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8f1a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f1a0-104">SYNTAX</span></span>

### <span data-ttu-id="8f1a0-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="8f1a0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1a0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8f1a0-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f1a0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f1a0-107">DESCRIPTION</span></span>
<span data-ttu-id="8f1a0-108">Cmdleten **Stop-AzVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8f1a0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f1a0-109">EXAMPLES</span></span>

### <span data-ttu-id="8f1a0-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8f1a0-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8f1a0-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8f1a0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f1a0-112">PARAMETERS</span></span>

### <span data-ttu-id="8f1a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f1a0-113">-AsJob</span></span>
<span data-ttu-id="8f1a0-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8f1a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1a0-115">-DefaultProfile</span></span>
<span data-ttu-id="8f1a0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f1a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8f1a0-117">-Force</span></span>
<span data-ttu-id="8f1a0-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f1a0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8f1a0-119">-Id</span></span>
<span data-ttu-id="8f1a0-120">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="8f1a0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f1a0-121">-Name</span></span>
<span data-ttu-id="8f1a0-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="8f1a0-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8f1a0-123">-NoWait</span></span>
<span data-ttu-id="8f1a0-124">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8f1a0-125">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8f1a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f1a0-127">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8f1a0-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="8f1a0-128">-SkipShutdown</span></span>
<span data-ttu-id="8f1a0-129">Så här efterfrågar du icke-städade VM-avstängning när VM-etableringen behålls.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="8f1a0-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8f1a0-130">-StayProvisioned</span></span>
<span data-ttu-id="8f1a0-131">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8f1a0-132">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="8f1a0-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f1a0-133">-Confirm</span></span>
<span data-ttu-id="8f1a0-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f1a0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f1a0-135">-WhatIf</span></span>
<span data-ttu-id="8f1a0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f1a0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f1a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1a0-138">CommonParameters</span></span>
<span data-ttu-id="8f1a0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f1a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1a0-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f1a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1a0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f1a0-141">INPUTS</span></span>

### <span data-ttu-id="8f1a0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8f1a0-142">System.String</span></span>

## <span data-ttu-id="8f1a0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f1a0-143">OUTPUTS</span></span>

### <span data-ttu-id="8f1a0-144">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8f1a0-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="8f1a0-145">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8f1a0-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8f1a0-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f1a0-146">NOTES</span></span>

## <span data-ttu-id="8f1a0-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f1a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="8f1a0-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8f1a0-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8f1a0-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8f1a0-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8f1a0-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8f1a0-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8f1a0-153">Update-AzVM</span></span>](./Update-AzVM.md)


