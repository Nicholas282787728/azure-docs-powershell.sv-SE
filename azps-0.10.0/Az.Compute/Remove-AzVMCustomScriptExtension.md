---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924966"
---
# <span data-ttu-id="1cdf1-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1cdf1-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="1cdf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdf1-103">Tar bort ett anpassat skript tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="1cdf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cdf1-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cdf1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cdf1-105">DESCRIPTION</span></span>
<span data-ttu-id="1cdf1-106">Cmdleten **Remove-AzVMCustomScriptExtension** tar bort ett anpassat tillägg för virtuella skript från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="1cdf1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cdf1-107">EXAMPLES</span></span>

## <span data-ttu-id="1cdf1-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cdf1-108">PARAMETERS</span></span>

### <span data-ttu-id="1cdf1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdf1-109">-DefaultProfile</span></span>
<span data-ttu-id="1cdf1-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cdf1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1cdf1-111">-Force</span></span>
<span data-ttu-id="1cdf1-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1cdf1-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1cdf1-113">-Name</span></span>
<span data-ttu-id="1cdf1-114">Anger namnet på det anpassade skript tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cdf1-115">-ResourceGroupName</span></span>
<span data-ttu-id="1cdf1-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf1-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="1cdf1-117">-VMName</span></span>
<span data-ttu-id="1cdf1-118">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1cdf1-119">-Confirm</span></span>
<span data-ttu-id="1cdf1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cdf1-121">-WhatIf</span></span>
<span data-ttu-id="1cdf1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1cdf1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdf1-124">CommonParameters</span></span>
<span data-ttu-id="1cdf1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdf1-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cdf1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdf1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cdf1-127">INPUTS</span></span>

### <span data-ttu-id="1cdf1-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="1cdf1-128">None</span></span>
<span data-ttu-id="1cdf1-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1cdf1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1cdf1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cdf1-130">OUTPUTS</span></span>

### <span data-ttu-id="1cdf1-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1cdf1-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1cdf1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cdf1-132">NOTES</span></span>

## <span data-ttu-id="1cdf1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cdf1-133">RELATED LINKS</span></span>

[<span data-ttu-id="1cdf1-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1cdf1-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="1cdf1-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1cdf1-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
