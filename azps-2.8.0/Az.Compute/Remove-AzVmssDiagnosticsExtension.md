---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 06b2a0d72d2195cfd73beb44bbfc8f61e5b87fa9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745003"
---
# <span data-ttu-id="a39c6-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a39c6-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="a39c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a39c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a39c6-103">Tar bort ett Diagnostics-tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="a39c6-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="a39c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a39c6-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a39c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a39c6-106">Cmdleten **Remove-AzVmssDiagnosticsExtension** tar bort ett diagnostiktest från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a39c6-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a39c6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a39c6-107">EXAMPLES</span></span>

### <span data-ttu-id="a39c6-108">Exempel 1: ta bort ett diagnostikverktyg från VMSS</span><span class="sxs-lookup"><span data-stu-id="a39c6-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="a39c6-109">Det här kommandot tar bort diagnostikprogrammet från VMSS.</span><span class="sxs-lookup"><span data-stu-id="a39c6-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="a39c6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a39c6-110">PARAMETERS</span></span>

### <span data-ttu-id="a39c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39c6-111">-DefaultProfile</span></span>
<span data-ttu-id="a39c6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a39c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a39c6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="a39c6-113">-Name</span></span>
<span data-ttu-id="a39c6-114">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="a39c6-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39c6-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a39c6-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a39c6-116">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a39c6-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a39c6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a39c6-117">-Confirm</span></span>
<span data-ttu-id="a39c6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a39c6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39c6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39c6-119">-WhatIf</span></span>
<span data-ttu-id="a39c6-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a39c6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39c6-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a39c6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39c6-122">CommonParameters</span></span>
<span data-ttu-id="a39c6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39c6-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a39c6-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39c6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a39c6-125">INPUTS</span></span>

### <span data-ttu-id="a39c6-126">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a39c6-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a39c6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a39c6-127">System.String</span></span>

## <span data-ttu-id="a39c6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a39c6-128">OUTPUTS</span></span>

### <span data-ttu-id="a39c6-129">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a39c6-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a39c6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a39c6-130">NOTES</span></span>

## <span data-ttu-id="a39c6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a39c6-131">RELATED LINKS</span></span>

[<span data-ttu-id="a39c6-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a39c6-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="a39c6-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a39c6-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a39c6-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a39c6-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


