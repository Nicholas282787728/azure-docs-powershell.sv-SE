---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930638"
---
# <span data-ttu-id="5b457-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b457-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5b457-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b457-102">SYNOPSIS</span></span>
<span data-ttu-id="5b457-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5b457-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b457-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b457-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b457-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b457-105">DESCRIPTION</span></span>
<span data-ttu-id="5b457-106">Cmdleten **Remove-AzureRmVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5b457-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="5b457-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b457-107">EXAMPLES</span></span>

## <span data-ttu-id="5b457-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b457-108">PARAMETERS</span></span>

### <span data-ttu-id="5b457-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b457-109">-DefaultProfile</span></span>
<span data-ttu-id="5b457-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b457-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b457-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5b457-111">-Force</span></span>
<span data-ttu-id="5b457-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5b457-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b457-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5b457-113">-Name</span></span>
<span data-ttu-id="5b457-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b457-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b457-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b457-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b457-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5b457-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b457-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b457-117">-VMName</span></span>
<span data-ttu-id="5b457-118">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5b457-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5b457-119">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5b457-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b457-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b457-120">-Confirm</span></span>
<span data-ttu-id="5b457-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b457-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b457-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b457-122">-WhatIf</span></span>
<span data-ttu-id="5b457-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b457-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5b457-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b457-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b457-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b457-125">CommonParameters</span></span>
<span data-ttu-id="5b457-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b457-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b457-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b457-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b457-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b457-128">INPUTS</span></span>

### <span data-ttu-id="5b457-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="5b457-129">None</span></span>
<span data-ttu-id="5b457-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5b457-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b457-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b457-131">OUTPUTS</span></span>

### <span data-ttu-id="5b457-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5b457-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5b457-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b457-133">NOTES</span></span>

## <span data-ttu-id="5b457-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b457-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b457-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b457-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b457-136">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b457-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b457-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b457-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
