---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757702"
---
# <span data-ttu-id="32f8a-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="32f8a-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="32f8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="32f8a-103">Kör kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="32f8a-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32f8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32f8a-104">SYNTAX</span></span>

### <span data-ttu-id="32f8a-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="32f8a-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f8a-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="32f8a-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32f8a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32f8a-107">DESCRIPTION</span></span>
<span data-ttu-id="32f8a-108">Starta ett Kör-kommando på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="32f8a-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="32f8a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="32f8a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="32f8a-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="32f8a-111">Starta ett Kör-kommando i RunPowerShellScript med åsidosättning av skriptet ' sample.ps1 ' och parametrarna på VM för ' VMname ' i resurs gruppen ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="32f8a-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="32f8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32f8a-112">PARAMETERS</span></span>

### <span data-ttu-id="32f8a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f8a-113">-AsJob</span></span>
<span data-ttu-id="32f8a-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="32f8a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="32f8a-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="32f8a-115">-CommandId</span></span>
<span data-ttu-id="32f8a-116">Kommando-ID för kör.</span><span class="sxs-lookup"><span data-stu-id="32f8a-116">The run command id.</span></span>

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

### <span data-ttu-id="32f8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f8a-117">-DefaultProfile</span></span>
<span data-ttu-id="32f8a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32f8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f8a-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="32f8a-119">-Parameter</span></span>
<span data-ttu-id="32f8a-120">Parametrarna för kör.</span><span class="sxs-lookup"><span data-stu-id="32f8a-120">The run command parameters.</span></span>

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

### <span data-ttu-id="32f8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="32f8a-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="32f8a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="32f8a-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="32f8a-123">-ScriptPath</span></span>
<span data-ttu-id="32f8a-124">Sökvägen till det skript som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="32f8a-124">Path of the script to be executed.</span></span>  <span data-ttu-id="32f8a-125">När det här värdet anges åsidosätter det angivna skriptet standard skriptet för kommandot.</span><span class="sxs-lookup"><span data-stu-id="32f8a-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="32f8a-126">-VM</span><span class="sxs-lookup"><span data-stu-id="32f8a-126">-VM</span></span>
<span data-ttu-id="32f8a-127">Den virtuella PS-datorobjektet.</span><span class="sxs-lookup"><span data-stu-id="32f8a-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="32f8a-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="32f8a-128">-VMName</span></span>
<span data-ttu-id="32f8a-129">Namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="32f8a-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="32f8a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32f8a-130">-Confirm</span></span>
<span data-ttu-id="32f8a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32f8a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f8a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f8a-132">-WhatIf</span></span>
<span data-ttu-id="32f8a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32f8a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f8a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32f8a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f8a-135">CommonParameters</span></span>
<span data-ttu-id="32f8a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f8a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f8a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f8a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32f8a-138">INPUTS</span></span>

### <span data-ttu-id="32f8a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="32f8a-139">System.String</span></span>
<span data-ttu-id="32f8a-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32f8a-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="32f8a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32f8a-141">OUTPUTS</span></span>

### <span data-ttu-id="32f8a-142">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="32f8a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="32f8a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32f8a-143">NOTES</span></span>

## <span data-ttu-id="32f8a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32f8a-144">RELATED LINKS</span></span>
