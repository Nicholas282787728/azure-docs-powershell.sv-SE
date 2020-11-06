---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576596"
---
# <span data-ttu-id="3debc-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3debc-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3debc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3debc-102">SYNOPSIS</span></span>
<span data-ttu-id="3debc-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3debc-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3debc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3debc-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3debc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3debc-105">DESCRIPTION</span></span>
<span data-ttu-id="3debc-106">Cmdleten **Remove-AzureRmVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3debc-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="3debc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3debc-107">EXAMPLES</span></span>

## <span data-ttu-id="3debc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3debc-108">PARAMETERS</span></span>

### <span data-ttu-id="3debc-109">-Force</span><span class="sxs-lookup"><span data-stu-id="3debc-109">-Force</span></span>
<span data-ttu-id="3debc-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3debc-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3debc-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="3debc-111">-Name</span></span>
<span data-ttu-id="3debc-112">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3debc-112">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3debc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3debc-113">-ResourceGroupName</span></span>
<span data-ttu-id="3debc-114">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3debc-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3debc-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="3debc-115">-VMName</span></span>
<span data-ttu-id="3debc-116">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3debc-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3debc-117">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3debc-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3debc-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3debc-118">-Confirm</span></span>
<span data-ttu-id="3debc-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3debc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3debc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3debc-120">-WhatIf</span></span>
<span data-ttu-id="3debc-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3debc-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3debc-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3debc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3debc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3debc-123">CommonParameters</span></span>
<span data-ttu-id="3debc-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3debc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3debc-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3debc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3debc-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3debc-126">INPUTS</span></span>

### <span data-ttu-id="3debc-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="3debc-127">None</span></span>
<span data-ttu-id="3debc-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3debc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3debc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3debc-129">OUTPUTS</span></span>

## <span data-ttu-id="3debc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3debc-130">NOTES</span></span>

## <span data-ttu-id="3debc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3debc-131">RELATED LINKS</span></span>

[<span data-ttu-id="3debc-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3debc-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3debc-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3debc-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3debc-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3debc-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
