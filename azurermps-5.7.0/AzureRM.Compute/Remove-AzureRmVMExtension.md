---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573530"
---
# <span data-ttu-id="897ed-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="897ed-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="897ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="897ed-102">SYNOPSIS</span></span>
<span data-ttu-id="897ed-103">Tar bort ett tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="897ed-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="897ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="897ed-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="897ed-105">DESCRIPTION</span></span>
<span data-ttu-id="897ed-106">Cmdleten **Remove-AzureRmVMExtension** tar bort ett tillägg från virtuella dator tillägg på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="897ed-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="897ed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="897ed-107">EXAMPLES</span></span>

### <span data-ttu-id="897ed-108">Exempel 1: ta bort ett tillägg från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="897ed-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="897ed-109">Det här kommandot tar bort tillägget med namnet ContosoTest från den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="897ed-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="897ed-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="897ed-110">PARAMETERS</span></span>

### <span data-ttu-id="897ed-111">-Force</span><span class="sxs-lookup"><span data-stu-id="897ed-111">-Force</span></span>
<span data-ttu-id="897ed-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="897ed-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="897ed-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="897ed-113">-Name</span></span>
<span data-ttu-id="897ed-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897ed-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="897ed-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897ed-115">-ResourceGroupName</span></span>
<span data-ttu-id="897ed-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="897ed-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="897ed-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="897ed-117">-VMName</span></span>
<span data-ttu-id="897ed-118">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="897ed-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="897ed-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="897ed-119">-Confirm</span></span>
<span data-ttu-id="897ed-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="897ed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897ed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897ed-121">-WhatIf</span></span>
<span data-ttu-id="897ed-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="897ed-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="897ed-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="897ed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897ed-124">CommonParameters</span></span>
<span data-ttu-id="897ed-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897ed-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="897ed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897ed-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="897ed-127">INPUTS</span></span>

### <span data-ttu-id="897ed-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="897ed-128">None</span></span>
<span data-ttu-id="897ed-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="897ed-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="897ed-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="897ed-130">OUTPUTS</span></span>

## <span data-ttu-id="897ed-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="897ed-131">NOTES</span></span>

## <span data-ttu-id="897ed-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="897ed-132">RELATED LINKS</span></span>

[<span data-ttu-id="897ed-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="897ed-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="897ed-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="897ed-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


