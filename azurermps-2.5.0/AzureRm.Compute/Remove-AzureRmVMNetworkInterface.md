---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930318"
---
# <span data-ttu-id="c8f9b-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c8f9b-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="c8f9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f9b-103">Tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8f9b-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f9b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f9b-106">Cmdleten **Remove-AzureRmVMNetworkInterface** tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c8f9b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f9b-108">9.1</span><span class="sxs-lookup"><span data-stu-id="c8f9b-108">1:</span></span>
```

```

## <span data-ttu-id="c8f9b-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8f9b-109">PARAMETERS</span></span>

### <span data-ttu-id="c8f9b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f9b-110">-DefaultProfile</span></span>
<span data-ttu-id="c8f9b-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f9b-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="c8f9b-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="c8f9b-113">Anger en matris med nätverkskort-ID: n som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8f9b-114">-VM</span><span class="sxs-lookup"><span data-stu-id="c8f9b-114">-VM</span></span>
<span data-ttu-id="c8f9b-115">Anger den virtuella dator från vilken denna cmdlet tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="c8f9b-116">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="c8f9b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8f9b-117">-Confirm</span></span>
<span data-ttu-id="c8f9b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c8f9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f9b-119">-WhatIf</span></span>
<span data-ttu-id="c8f9b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8f9b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c8f9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f9b-122">CommonParameters</span></span>
<span data-ttu-id="c8f9b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f9b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f9b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8f9b-125">INPUTS</span></span>

### <span data-ttu-id="c8f9b-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8f9b-126">PSVirtualMachine</span></span>
<span data-ttu-id="c8f9b-127">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c8f9b-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c8f9b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8f9b-128">OUTPUTS</span></span>

### <span data-ttu-id="c8f9b-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8f9b-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c8f9b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8f9b-130">NOTES</span></span>

## <span data-ttu-id="c8f9b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8f9b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8f9b-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c8f9b-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


