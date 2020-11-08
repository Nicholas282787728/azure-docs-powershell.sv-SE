---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270025"
---
# <span data-ttu-id="6a6f3-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6a6f3-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="6a6f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6f3-103">Kör ett kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-103">Run a command on the VM.</span></span>

## <span data-ttu-id="6a6f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a6f3-104">SYNTAX</span></span>

### <span data-ttu-id="6a6f3-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="6a6f3-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6f3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6a6f3-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a6f3-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="6a6f3-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a6f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a6f3-108">DESCRIPTION</span></span>
<span data-ttu-id="6a6f3-109">Starta ett Kör-kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="6a6f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="6a6f3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a6f3-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="6a6f3-112">Starta ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna på VM för ' VMname ' i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="6a6f3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a6f3-113">PARAMETERS</span></span>

### <span data-ttu-id="6a6f3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a6f3-114">-AsJob</span></span>
<span data-ttu-id="6a6f3-115">Kör cmdleten i bakgrunden och returnera ett Job-objekt för att spåra status.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="6a6f3-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="6a6f3-116">-CommandId</span></span>
<span data-ttu-id="6a6f3-117">Kommando-ID för kör.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-117">The run command ID.</span></span>

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

### <span data-ttu-id="6a6f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6f3-118">-DefaultProfile</span></span>
<span data-ttu-id="6a6f3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6f3-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6a6f3-120">-Parameter</span></span>
<span data-ttu-id="6a6f3-121">Parametrarna för kör.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-121">The run command parameters.</span></span>

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

### <span data-ttu-id="6a6f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a6f3-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a6f3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a6f3-124">-ResourceId</span></span>
<span data-ttu-id="6a6f3-125">Resurs-ID för VM.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="6a6f3-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="6a6f3-126">-ScriptPath</span></span>
<span data-ttu-id="6a6f3-127">Sökvägen till det skript som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-127">Path of the script to be executed.</span></span>  <span data-ttu-id="6a6f3-128">När det här värdet anges åsidosätter det angivna skriptet standard skriptet för kommandot.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="6a6f3-129">-VM</span><span class="sxs-lookup"><span data-stu-id="6a6f3-129">-VM</span></span>
<span data-ttu-id="6a6f3-130">Den virtuella PS-datorobjektet.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a6f3-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a6f3-131">-VMName</span></span>
<span data-ttu-id="6a6f3-132">Namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="6a6f3-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a6f3-133">-Confirm</span></span>
<span data-ttu-id="6a6f3-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a6f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a6f3-135">-WhatIf</span></span>
<span data-ttu-id="6a6f3-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a6f3-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a6f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6f3-138">CommonParameters</span></span>
<span data-ttu-id="6a6f3-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6f3-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a6f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6f3-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a6f3-141">INPUTS</span></span>

### <span data-ttu-id="6a6f3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6a6f3-142">System.String</span></span>

### <span data-ttu-id="6a6f3-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a6f3-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a6f3-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a6f3-144">OUTPUTS</span></span>

### <span data-ttu-id="6a6f3-145">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="6a6f3-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="6a6f3-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a6f3-146">NOTES</span></span>

## <span data-ttu-id="6a6f3-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a6f3-147">RELATED LINKS</span></span>
