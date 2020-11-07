---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 3036b26c4f3ebe6fc6f039f1754acdb3b50977f6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925098"
---
# <span data-ttu-id="64f1d-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="64f1d-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="64f1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="64f1d-103">Kör kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64f1d-103">Run command on the VM.</span></span>

## <span data-ttu-id="64f1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64f1d-104">SYNTAX</span></span>

### <span data-ttu-id="64f1d-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="64f1d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f1d-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="64f1d-106">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64f1d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64f1d-107">DESCRIPTION</span></span>
<span data-ttu-id="64f1d-108">Starta ett Kör-kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64f1d-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="64f1d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="64f1d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64f1d-110">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="64f1d-111">Starta ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna på VM för ' VMname ' i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="64f1d-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="64f1d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64f1d-112">PARAMETERS</span></span>

### <span data-ttu-id="64f1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64f1d-113">-AsJob</span></span>
<span data-ttu-id="64f1d-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="64f1d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="64f1d-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="64f1d-115">-CommandId</span></span>
<span data-ttu-id="64f1d-116">Kommando-ID för kör.</span><span class="sxs-lookup"><span data-stu-id="64f1d-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f1d-117">-DefaultProfile</span></span>
<span data-ttu-id="64f1d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64f1d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f1d-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="64f1d-119">-Parameter</span></span>
<span data-ttu-id="64f1d-120">Parametrarna för kör.</span><span class="sxs-lookup"><span data-stu-id="64f1d-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="64f1d-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64f1d-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="64f1d-123">-ScriptPath</span></span>
<span data-ttu-id="64f1d-124">Sökvägen till det skript som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="64f1d-124">Path of the script to be executed.</span></span>  <span data-ttu-id="64f1d-125">När det här värdet anges åsidosätter det angivna skriptet standard skriptet för kommandot.</span><span class="sxs-lookup"><span data-stu-id="64f1d-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="64f1d-126">-VM</span></span>
<span data-ttu-id="64f1d-127">Den virtuella PS-datorobjektet.</span><span class="sxs-lookup"><span data-stu-id="64f1d-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="64f1d-128">-VMName</span></span>
<span data-ttu-id="64f1d-129">Namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64f1d-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64f1d-130">-Confirm</span></span>
<span data-ttu-id="64f1d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64f1d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f1d-132">-WhatIf</span></span>
<span data-ttu-id="64f1d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64f1d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f1d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64f1d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f1d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f1d-135">CommonParameters</span></span>
<span data-ttu-id="64f1d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f1d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f1d-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f1d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f1d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64f1d-138">INPUTS</span></span>

### <span data-ttu-id="64f1d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="64f1d-139">System.String</span></span>
<span data-ttu-id="64f1d-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64f1d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="64f1d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64f1d-141">OUTPUTS</span></span>

### <span data-ttu-id="64f1d-142">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="64f1d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="64f1d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64f1d-143">NOTES</span></span>

## <span data-ttu-id="64f1d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64f1d-144">RELATED LINKS</span></span>

