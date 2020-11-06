---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577103"
---
# <span data-ttu-id="7da37-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="7da37-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="7da37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7da37-102">SYNOPSIS</span></span>
<span data-ttu-id="7da37-103">Kör kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7da37-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7da37-104">SYNTAX</span></span>

### <span data-ttu-id="7da37-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="7da37-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da37-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7da37-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da37-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="7da37-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7da37-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7da37-108">DESCRIPTION</span></span>
<span data-ttu-id="7da37-109">Starta ett Kör-kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7da37-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="7da37-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7da37-110">EXAMPLES</span></span>

### <span data-ttu-id="7da37-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7da37-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="7da37-112">Starta ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna på VM för ' VMname ' i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="7da37-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="7da37-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7da37-113">PARAMETERS</span></span>

### <span data-ttu-id="7da37-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7da37-114">-AsJob</span></span>
<span data-ttu-id="7da37-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="7da37-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7da37-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="7da37-116">-CommandId</span></span>
<span data-ttu-id="7da37-117">Kommando-ID för kör.</span><span class="sxs-lookup"><span data-stu-id="7da37-117">The run command id.</span></span>

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

### <span data-ttu-id="7da37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da37-118">-DefaultProfile</span></span>
<span data-ttu-id="7da37-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7da37-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da37-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7da37-120">-Parameter</span></span>
<span data-ttu-id="7da37-121">Parametrarna för kör.</span><span class="sxs-lookup"><span data-stu-id="7da37-121">The run command parameters.</span></span>

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

### <span data-ttu-id="7da37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da37-122">-ResourceGroupName</span></span>
<span data-ttu-id="7da37-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7da37-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da37-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7da37-124">-ResourceId</span></span>
<span data-ttu-id="7da37-125">Resurs-ID för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7da37-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="7da37-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="7da37-126">-ScriptPath</span></span>
<span data-ttu-id="7da37-127">Sökvägen till det skript som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="7da37-127">Path of the script to be executed.</span></span>  <span data-ttu-id="7da37-128">När det här värdet anges åsidosätter det angivna skriptet standard skriptet för kommandot.</span><span class="sxs-lookup"><span data-stu-id="7da37-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="7da37-129">-VM</span><span class="sxs-lookup"><span data-stu-id="7da37-129">-VM</span></span>
<span data-ttu-id="7da37-130">Den virtuella PS-datorobjektet.</span><span class="sxs-lookup"><span data-stu-id="7da37-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="7da37-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="7da37-131">-VMName</span></span>
<span data-ttu-id="7da37-132">Namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7da37-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da37-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7da37-133">-Confirm</span></span>
<span data-ttu-id="7da37-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7da37-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da37-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da37-135">-WhatIf</span></span>
<span data-ttu-id="7da37-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7da37-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da37-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7da37-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da37-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da37-138">CommonParameters</span></span>
<span data-ttu-id="7da37-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da37-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da37-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da37-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da37-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7da37-141">INPUTS</span></span>

### <span data-ttu-id="7da37-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7da37-142">System.String</span></span>

### <span data-ttu-id="7da37-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7da37-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7da37-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7da37-144">OUTPUTS</span></span>

### <span data-ttu-id="7da37-145">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="7da37-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="7da37-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7da37-146">NOTES</span></span>

## <span data-ttu-id="7da37-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7da37-147">RELATED LINKS</span></span>
