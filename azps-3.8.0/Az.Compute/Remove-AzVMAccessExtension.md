---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 6c02a8381ca1cda4fec6fb52ea3d798884b45bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089838"
---
# <span data-ttu-id="c4ef2-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c4ef2-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="c4ef2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ef2-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="c4ef2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4ef2-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4ef2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4ef2-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ef2-106">Cmdleten **Remove-AzVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="c4ef2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4ef2-107">EXAMPLES</span></span>

## <span data-ttu-id="c4ef2-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4ef2-108">PARAMETERS</span></span>

### <span data-ttu-id="c4ef2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ef2-109">-DefaultProfile</span></span>
<span data-ttu-id="c4ef2-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4ef2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c4ef2-111">-Force</span></span>
<span data-ttu-id="c4ef2-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4ef2-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4ef2-113">-Name</span></span>
<span data-ttu-id="c4ef2-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4ef2-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c4ef2-115">-NoWait</span></span>
<span data-ttu-id="c4ef2-116">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c4ef2-117">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c4ef2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ef2-118">-ResourceGroupName</span></span>
<span data-ttu-id="c4ef2-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c4ef2-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c4ef2-120">-VMName</span></span>
<span data-ttu-id="c4ef2-121">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c4ef2-122">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4ef2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4ef2-123">-Confirm</span></span>
<span data-ttu-id="c4ef2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ef2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ef2-125">-WhatIf</span></span>
<span data-ttu-id="c4ef2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ef2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ef2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ef2-128">CommonParameters</span></span>
<span data-ttu-id="c4ef2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ef2-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4ef2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ef2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4ef2-131">INPUTS</span></span>

### <span data-ttu-id="c4ef2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ef2-132">System.String</span></span>

## <span data-ttu-id="c4ef2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4ef2-133">OUTPUTS</span></span>

### <span data-ttu-id="c4ef2-134">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c4ef2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c4ef2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4ef2-135">NOTES</span></span>

## <span data-ttu-id="c4ef2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4ef2-136">RELATED LINKS</span></span>

[<span data-ttu-id="c4ef2-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c4ef2-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="c4ef2-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c4ef2-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="c4ef2-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c4ef2-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)