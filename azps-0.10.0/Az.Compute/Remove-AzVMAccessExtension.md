---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924981"
---
# <span data-ttu-id="9c334-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9c334-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="9c334-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c334-102">SYNOPSIS</span></span>
<span data-ttu-id="9c334-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9c334-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="9c334-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c334-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c334-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c334-105">DESCRIPTION</span></span>
<span data-ttu-id="9c334-106">Cmdleten **Remove-AzVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9c334-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="9c334-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c334-107">EXAMPLES</span></span>

## <span data-ttu-id="9c334-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c334-108">PARAMETERS</span></span>

### <span data-ttu-id="9c334-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c334-109">-DefaultProfile</span></span>
<span data-ttu-id="9c334-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c334-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c334-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9c334-111">-Force</span></span>
<span data-ttu-id="9c334-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9c334-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c334-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c334-113">-Name</span></span>
<span data-ttu-id="9c334-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c334-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c334-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c334-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c334-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9c334-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9c334-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c334-117">-VMName</span></span>
<span data-ttu-id="9c334-118">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9c334-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9c334-119">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9c334-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c334-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c334-120">-Confirm</span></span>
<span data-ttu-id="9c334-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c334-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c334-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c334-122">-WhatIf</span></span>
<span data-ttu-id="9c334-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c334-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9c334-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c334-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c334-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c334-125">CommonParameters</span></span>
<span data-ttu-id="9c334-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c334-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c334-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c334-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c334-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c334-128">INPUTS</span></span>

### <span data-ttu-id="9c334-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="9c334-129">None</span></span>
<span data-ttu-id="9c334-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9c334-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c334-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c334-131">OUTPUTS</span></span>

### <span data-ttu-id="9c334-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c334-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c334-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c334-133">NOTES</span></span>

## <span data-ttu-id="9c334-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c334-134">RELATED LINKS</span></span>

[<span data-ttu-id="9c334-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9c334-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="9c334-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9c334-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="9c334-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9c334-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
