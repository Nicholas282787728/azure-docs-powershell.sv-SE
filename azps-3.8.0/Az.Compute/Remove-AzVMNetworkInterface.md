---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091396"
---
# <span data-ttu-id="ce4cc-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ce4cc-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="ce4cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4cc-103">Tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ce4cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce4cc-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce4cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ce4cc-106">Cmdleten **Remove-AzVMNetworkInterface** tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ce4cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce4cc-107">EXAMPLES</span></span>

## <span data-ttu-id="ce4cc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce4cc-108">PARAMETERS</span></span>

### <span data-ttu-id="ce4cc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4cc-109">-DefaultProfile</span></span>
<span data-ttu-id="ce4cc-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce4cc-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="ce4cc-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="ce4cc-112">Anger en matris med nätverkskort-ID: n som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4cc-113">-VM</span><span class="sxs-lookup"><span data-stu-id="ce4cc-113">-VM</span></span>
<span data-ttu-id="ce4cc-114">Anger den virtuella dator från vilken denna cmdlet tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="ce4cc-115">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4cc-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce4cc-116">-Confirm</span></span>
<span data-ttu-id="ce4cc-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce4cc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4cc-118">-WhatIf</span></span>
<span data-ttu-id="ce4cc-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce4cc-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce4cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4cc-121">CommonParameters</span></span>
<span data-ttu-id="ce4cc-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4cc-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce4cc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4cc-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce4cc-124">INPUTS</span></span>

### <span data-ttu-id="ce4cc-125">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ce4cc-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ce4cc-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce4cc-126">OUTPUTS</span></span>

### <span data-ttu-id="ce4cc-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ce4cc-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ce4cc-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce4cc-128">NOTES</span></span>

## <span data-ttu-id="ce4cc-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce4cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce4cc-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ce4cc-130">Get-AzVM</span></span>](./Get-AzVM.md)

