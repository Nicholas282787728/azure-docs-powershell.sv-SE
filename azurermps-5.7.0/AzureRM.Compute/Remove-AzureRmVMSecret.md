---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755981"
---
# <span data-ttu-id="d1eed-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="d1eed-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="d1eed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1eed-102">SYNOPSIS</span></span>
<span data-ttu-id="d1eed-103">Tar bort (a) hemliga (a) hemligheter från ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="d1eed-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1eed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1eed-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1eed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1eed-105">DESCRIPTION</span></span>
<span data-ttu-id="d1eed-106">Remove-AzureRmVMSecret-cmdleten tar bort (a) hemligheter från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d1eed-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="d1eed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1eed-107">EXAMPLES</span></span>

### <span data-ttu-id="d1eed-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1eed-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="d1eed-109">Tar bort alla hemligheter från en virtuell dator "VM1" i resurs gruppen "RG1" och uppdaterar den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="d1eed-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="d1eed-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1eed-110">PARAMETERS</span></span>

### <span data-ttu-id="d1eed-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d1eed-111">-SourceVaultId</span></span>
<span data-ttu-id="d1eed-112">Anger en matris med käll valv-ID: n som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d1eed-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1eed-113">-VM</span><span class="sxs-lookup"><span data-stu-id="d1eed-113">-VM</span></span>
<span data-ttu-id="d1eed-114">Anger den virtuella dator från vilken denna cmdlet tar bort (a) hemlighet (s).</span><span class="sxs-lookup"><span data-stu-id="d1eed-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="d1eed-115">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d1eed-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="d1eed-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1eed-116">-Confirm</span></span>
<span data-ttu-id="d1eed-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1eed-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1eed-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1eed-118">-WhatIf</span></span>
<span data-ttu-id="d1eed-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1eed-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1eed-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1eed-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1eed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1eed-121">CommonParameters</span></span>
<span data-ttu-id="d1eed-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1eed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1eed-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1eed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1eed-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1eed-124">INPUTS</span></span>

### <span data-ttu-id="d1eed-125">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1eed-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d1eed-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1eed-126">OUTPUTS</span></span>

### <span data-ttu-id="d1eed-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1eed-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d1eed-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1eed-128">NOTES</span></span>

## <span data-ttu-id="d1eed-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1eed-129">RELATED LINKS</span></span>

