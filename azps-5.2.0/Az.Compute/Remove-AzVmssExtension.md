---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408016"
---
# <span data-ttu-id="ffa2d-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ffa2d-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="ffa2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffa2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa2d-103">Tar bort ett tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="ffa2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffa2d-104">SYNTAX</span></span>

### <span data-ttu-id="ffa2d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa2d-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa2d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa2d-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa2d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffa2d-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa2d-108">Cmdleten **Remove-AzVmssExtension** tar bort ett tillägg från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ffa2d-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ffa2d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffa2d-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa2d-110">Exempel 1: ta bort ett VMSS-tillägg</span><span class="sxs-lookup"><span data-stu-id="ffa2d-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="ffa2d-111">Det här kommandot tar bort tillägget för en VMSS och uppdaterar VMSS efter ändringen.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="ffa2d-112">Exempel 2: ta bort en instans från en VMSS</span><span class="sxs-lookup"><span data-stu-id="ffa2d-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="ffa2d-113">Det här kommandot tar bort ange tilläggs-ID från VMSS som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="ffa2d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffa2d-114">PARAMETERS</span></span>

### <span data-ttu-id="ffa2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa2d-115">-DefaultProfile</span></span>
<span data-ttu-id="ffa2d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffa2d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ffa2d-117">-Id</span></span>
<span data-ttu-id="ffa2d-118">Anger ID för tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ffa2d-119">-Name</span></span>
<span data-ttu-id="ffa2d-120">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2d-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ffa2d-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ffa2d-122">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="ffa2d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ffa2d-123">-Confirm</span></span>
<span data-ttu-id="ffa2d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa2d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa2d-125">-WhatIf</span></span>
<span data-ttu-id="ffa2d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffa2d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa2d-128">CommonParameters</span></span>
<span data-ttu-id="ffa2d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa2d-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa2d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa2d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffa2d-131">INPUTS</span></span>

### <span data-ttu-id="ffa2d-132">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ffa2d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ffa2d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa2d-133">System.String</span></span>

## <span data-ttu-id="ffa2d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffa2d-134">OUTPUTS</span></span>

### <span data-ttu-id="ffa2d-135">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ffa2d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ffa2d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffa2d-136">NOTES</span></span>

## <span data-ttu-id="ffa2d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffa2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="ffa2d-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ffa2d-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
