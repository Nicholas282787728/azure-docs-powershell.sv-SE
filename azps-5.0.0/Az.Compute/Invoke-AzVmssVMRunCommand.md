---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270023"
---
# <span data-ttu-id="eac4c-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="eac4c-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="eac4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eac4c-102">SYNOPSIS</span></span>
<span data-ttu-id="eac4c-103">Kommandot kör på den virtuella datorns skala ange virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eac4c-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="eac4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eac4c-104">SYNTAX</span></span>

### <span data-ttu-id="eac4c-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="eac4c-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac4c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="eac4c-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eac4c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="eac4c-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac4c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eac4c-108">DESCRIPTION</span></span>
<span data-ttu-id="eac4c-109">Aktivera kommandot kör på den virtuella datorns skala ange virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eac4c-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="eac4c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eac4c-110">EXAMPLES</span></span>

### <span data-ttu-id="eac4c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eac4c-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="eac4c-112">Anropa ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna för ID: t ' 0 ' för VM i den virtuella datorns skal uppsättning i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="eac4c-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="eac4c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="eac4c-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="eac4c-114">Anropa ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna för ID: t ' 0 ' för VM i den virtuella datorns skal uppsättning i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="eac4c-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="eac4c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eac4c-115">PARAMETERS</span></span>

### <span data-ttu-id="eac4c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eac4c-116">-AsJob</span></span>
<span data-ttu-id="eac4c-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eac4c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eac4c-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="eac4c-118">-CommandId</span></span>
<span data-ttu-id="eac4c-119">Kommando-ID för kör.</span><span class="sxs-lookup"><span data-stu-id="eac4c-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac4c-120">-DefaultProfile</span></span>
<span data-ttu-id="eac4c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eac4c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac4c-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eac4c-122">-InstanceId</span></span>
<span data-ttu-id="eac4c-123">Instans-ID för virtuell dator skalförändra angiven virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eac4c-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="eac4c-124">-Parameter</span></span>
<span data-ttu-id="eac4c-125">Parametrarna för kör.</span><span class="sxs-lookup"><span data-stu-id="eac4c-125">The run command parameters.</span></span>

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

### <span data-ttu-id="eac4c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac4c-126">-ResourceGroupName</span></span>
<span data-ttu-id="eac4c-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eac4c-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac4c-128">-ResourceId</span></span>
<span data-ttu-id="eac4c-129">Resurs-ID för virtuell dator skalförändra angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="eac4c-129">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="eac4c-130">-ScriptPath</span></span>
<span data-ttu-id="eac4c-131">Sökvägen till det skript som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="eac4c-131">Path of the script to be executed.</span></span>  <span data-ttu-id="eac4c-132">När det här värdet anges åsidosätter det angivna skriptet standard skriptet för kommandot.</span><span class="sxs-lookup"><span data-stu-id="eac4c-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="eac4c-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eac4c-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="eac4c-134">Skalan för den virtuella datorns utbyggbara objekt.</span><span class="sxs-lookup"><span data-stu-id="eac4c-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eac4c-135">-VMScaleSetName</span></span>
<span data-ttu-id="eac4c-136">Namnet på den virtuella datorns skala ange virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eac4c-136">The name of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac4c-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eac4c-137">-Confirm</span></span>
<span data-ttu-id="eac4c-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eac4c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac4c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac4c-139">-WhatIf</span></span>
<span data-ttu-id="eac4c-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eac4c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac4c-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eac4c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac4c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac4c-142">CommonParameters</span></span>
<span data-ttu-id="eac4c-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac4c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac4c-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eac4c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac4c-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eac4c-145">INPUTS</span></span>

### <span data-ttu-id="eac4c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="eac4c-146">System.String</span></span>

### <span data-ttu-id="eac4c-147">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eac4c-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="eac4c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eac4c-148">OUTPUTS</span></span>

### <span data-ttu-id="eac4c-149">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="eac4c-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="eac4c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eac4c-150">NOTES</span></span>

## <span data-ttu-id="eac4c-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eac4c-151">RELATED LINKS</span></span>
