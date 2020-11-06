---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573529"
---
# <span data-ttu-id="86e3a-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="86e3a-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="86e3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="86e3a-103">Tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="86e3a-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86e3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86e3a-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="86e3a-106">Cmdleten **Remove-AzureRmVMNetworkInterface** tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="86e3a-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="86e3a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86e3a-107">EXAMPLES</span></span>

## <span data-ttu-id="86e3a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86e3a-108">PARAMETERS</span></span>

### <span data-ttu-id="86e3a-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="86e3a-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="86e3a-110">Anger en matris med nätverkskort-ID: n som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="86e3a-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e3a-111">-VM</span><span class="sxs-lookup"><span data-stu-id="86e3a-111">-VM</span></span>
<span data-ttu-id="86e3a-112">Anger den virtuella dator från vilken denna cmdlet tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="86e3a-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="86e3a-113">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="86e3a-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86e3a-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86e3a-114">-Confirm</span></span>
<span data-ttu-id="86e3a-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86e3a-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="86e3a-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e3a-116">-WhatIf</span></span>
<span data-ttu-id="86e3a-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86e3a-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86e3a-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86e3a-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="86e3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e3a-119">CommonParameters</span></span>
<span data-ttu-id="86e3a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e3a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e3a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e3a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86e3a-122">INPUTS</span></span>

### <span data-ttu-id="86e3a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="86e3a-123">None</span></span>
<span data-ttu-id="86e3a-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="86e3a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86e3a-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86e3a-125">OUTPUTS</span></span>

## <span data-ttu-id="86e3a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86e3a-126">NOTES</span></span>

## <span data-ttu-id="86e3a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86e3a-127">RELATED LINKS</span></span>

[<span data-ttu-id="86e3a-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="86e3a-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


