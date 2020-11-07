---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757126"
---
# <span data-ttu-id="3be24-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3be24-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="3be24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3be24-102">SYNOPSIS</span></span>
<span data-ttu-id="3be24-103">Tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3be24-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3be24-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3be24-105">DESCRIPTION</span></span>
<span data-ttu-id="3be24-106">Cmdleten **Remove-AzureRmVMNetworkInterface** tar bort ett nätverks gränssnitt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3be24-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="3be24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3be24-107">EXAMPLES</span></span>

## <span data-ttu-id="3be24-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3be24-108">PARAMETERS</span></span>

### <span data-ttu-id="3be24-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be24-109">-DefaultProfile</span></span>
<span data-ttu-id="3be24-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3be24-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be24-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="3be24-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="3be24-112">Anger en matris med nätverkskort-ID: n som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3be24-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3be24-113">-VM</span><span class="sxs-lookup"><span data-stu-id="3be24-113">-VM</span></span>
<span data-ttu-id="3be24-114">Anger den virtuella dator från vilken denna cmdlet tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3be24-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="3be24-115">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="3be24-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="3be24-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3be24-116">-Confirm</span></span>
<span data-ttu-id="3be24-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3be24-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be24-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be24-118">-WhatIf</span></span>
<span data-ttu-id="3be24-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3be24-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3be24-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3be24-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be24-121">CommonParameters</span></span>
<span data-ttu-id="3be24-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be24-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be24-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be24-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3be24-124">INPUTS</span></span>

### <span data-ttu-id="3be24-125">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3be24-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3be24-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3be24-126">OUTPUTS</span></span>

### <span data-ttu-id="3be24-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3be24-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3be24-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3be24-128">NOTES</span></span>

## <span data-ttu-id="3be24-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3be24-129">RELATED LINKS</span></span>

[<span data-ttu-id="3be24-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3be24-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


