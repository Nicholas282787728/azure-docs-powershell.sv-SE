---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745024"
---
# <span data-ttu-id="8e562-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8e562-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="8e562-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e562-102">SYNOPSIS</span></span>
<span data-ttu-id="8e562-103">Tar bort ett anpassat skript tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8e562-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="8e562-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e562-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e562-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e562-105">DESCRIPTION</span></span>
<span data-ttu-id="8e562-106">Cmdleten **Remove-AzVMCustomScriptExtension** tar bort ett anpassat tillägg för virtuella skript från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8e562-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8e562-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e562-107">EXAMPLES</span></span>

## <span data-ttu-id="8e562-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e562-108">PARAMETERS</span></span>

### <span data-ttu-id="8e562-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e562-109">-DefaultProfile</span></span>
<span data-ttu-id="8e562-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e562-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e562-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8e562-111">-Force</span></span>
<span data-ttu-id="8e562-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8e562-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e562-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e562-113">-Name</span></span>
<span data-ttu-id="8e562-114">Anger namnet på det anpassade skript tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e562-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8e562-115">-NoWait</span></span>
<span data-ttu-id="8e562-116">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="8e562-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8e562-117">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="8e562-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8e562-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e562-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e562-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8e562-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="8e562-120">-VMName</span></span>
<span data-ttu-id="8e562-121">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="8e562-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e562-122">-Confirm</span></span>
<span data-ttu-id="8e562-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e562-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e562-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e562-124">-WhatIf</span></span>
<span data-ttu-id="8e562-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e562-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e562-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e562-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e562-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e562-127">CommonParameters</span></span>
<span data-ttu-id="8e562-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e562-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e562-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e562-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e562-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e562-130">INPUTS</span></span>

### <span data-ttu-id="8e562-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8e562-131">System.String</span></span>

## <span data-ttu-id="8e562-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e562-132">OUTPUTS</span></span>

### <span data-ttu-id="8e562-133">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8e562-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8e562-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e562-134">NOTES</span></span>

## <span data-ttu-id="8e562-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e562-135">RELATED LINKS</span></span>

[<span data-ttu-id="8e562-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8e562-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="8e562-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8e562-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
