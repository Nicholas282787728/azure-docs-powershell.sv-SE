---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924942"
---
# <span data-ttu-id="14cd2-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="14cd2-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="14cd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="14cd2-103">Tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="14cd2-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="14cd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14cd2-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14cd2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="14cd2-106">Cmdleten **Remove-AzVMNetworkInterface** tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="14cd2-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="14cd2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="14cd2-108">9.1</span><span class="sxs-lookup"><span data-stu-id="14cd2-108">1:</span></span>
```

```

## <span data-ttu-id="14cd2-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14cd2-109">PARAMETERS</span></span>

### <span data-ttu-id="14cd2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cd2-110">-DefaultProfile</span></span>
<span data-ttu-id="14cd2-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14cd2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14cd2-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="14cd2-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="14cd2-113">Anger en matris med nätverkskort-ID: n som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="14cd2-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="14cd2-114">-VM</span><span class="sxs-lookup"><span data-stu-id="14cd2-114">-VM</span></span>
<span data-ttu-id="14cd2-115">Anger den virtuella dator från vilken denna cmdlet tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="14cd2-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="14cd2-116">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="14cd2-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="14cd2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14cd2-117">-Confirm</span></span>
<span data-ttu-id="14cd2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14cd2-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="14cd2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14cd2-119">-WhatIf</span></span>
<span data-ttu-id="14cd2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14cd2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14cd2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14cd2-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="14cd2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cd2-122">CommonParameters</span></span>
<span data-ttu-id="14cd2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cd2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cd2-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14cd2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cd2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14cd2-125">INPUTS</span></span>

### <span data-ttu-id="14cd2-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="14cd2-126">PSVirtualMachine</span></span>
<span data-ttu-id="14cd2-127">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="14cd2-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="14cd2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14cd2-128">OUTPUTS</span></span>

### <span data-ttu-id="14cd2-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="14cd2-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="14cd2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14cd2-130">NOTES</span></span>

## <span data-ttu-id="14cd2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14cd2-131">RELATED LINKS</span></span>

[<span data-ttu-id="14cd2-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="14cd2-132">Get-AzVM</span></span>](./Get-AzVM.md)


