---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092443"
---
# <span data-ttu-id="d4712-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="d4712-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="d4712-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4712-102">SYNOPSIS</span></span>
<span data-ttu-id="d4712-103">Anger tillstånd för Orchestration-tjänsten för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4712-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="d4712-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4712-104">SYNTAX</span></span>

### <span data-ttu-id="d4712-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="d4712-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4712-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d4712-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4712-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d4712-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4712-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4712-108">DESCRIPTION</span></span>
<span data-ttu-id="d4712-109">Anger tillstånd för Orchestration-tjänsten för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4712-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="d4712-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4712-110">EXAMPLES</span></span>

### <span data-ttu-id="d4712-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4712-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="d4712-112">Det här kommandot gör om tjänsten för automatisk reparation på VMSS "vmss1" i resurs gruppen "RG".</span><span class="sxs-lookup"><span data-stu-id="d4712-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="d4712-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d4712-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="d4712-114">Det här kommandot återupptar tjänsten för automatisk reparation på VMSS "vmss1" i resurs gruppen "RG".</span><span class="sxs-lookup"><span data-stu-id="d4712-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="d4712-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4712-115">PARAMETERS</span></span>

### <span data-ttu-id="d4712-116">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="d4712-116">-Action</span></span>
<span data-ttu-id="d4712-117">Den åtgärd som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="d4712-117">The action to be performed.</span></span>  <span data-ttu-id="d4712-118">Möjliga värden är: Resume, Suspend.</span><span class="sxs-lookup"><span data-stu-id="d4712-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4712-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4712-119">-AsJob</span></span>
<span data-ttu-id="d4712-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d4712-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4712-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4712-121">-DefaultProfile</span></span>
<span data-ttu-id="d4712-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4712-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4712-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4712-123">-InputObject</span></span>
<span data-ttu-id="d4712-124">Det lokala objektet för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d4712-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4712-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4712-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4712-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d4712-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4712-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4712-127">-ResourceId</span></span>
<span data-ttu-id="d4712-128">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="d4712-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="d4712-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d4712-129">-ServiceName</span></span>
<span data-ttu-id="d4712-130">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d4712-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4712-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4712-131">-VMScaleSetName</span></span>
<span data-ttu-id="d4712-132">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d4712-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d4712-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4712-133">-Confirm</span></span>
<span data-ttu-id="d4712-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4712-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4712-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4712-135">-WhatIf</span></span>
<span data-ttu-id="d4712-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4712-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4712-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4712-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4712-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4712-138">CommonParameters</span></span>
<span data-ttu-id="d4712-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4712-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4712-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4712-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4712-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4712-141">INPUTS</span></span>

### <span data-ttu-id="d4712-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d4712-142">System.String</span></span>

### <span data-ttu-id="d4712-143">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4712-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d4712-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4712-144">OUTPUTS</span></span>

### <span data-ttu-id="d4712-145">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d4712-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d4712-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4712-146">NOTES</span></span>

## <span data-ttu-id="d4712-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4712-147">RELATED LINKS</span></span>
