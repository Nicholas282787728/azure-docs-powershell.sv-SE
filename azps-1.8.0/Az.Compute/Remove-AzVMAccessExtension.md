---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: a409d4f6d09279aed6a22b9212894a1aca9cae1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917310"
---
# <span data-ttu-id="9ac6a-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9ac6a-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="9ac6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac6a-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="9ac6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ac6a-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ac6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ac6a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac6a-106">Cmdleten **Remove-AzVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="9ac6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ac6a-107">EXAMPLES</span></span>

## <span data-ttu-id="9ac6a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ac6a-108">PARAMETERS</span></span>

### <span data-ttu-id="9ac6a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac6a-109">-DefaultProfile</span></span>
<span data-ttu-id="9ac6a-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac6a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9ac6a-111">-Force</span></span>
<span data-ttu-id="9ac6a-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac6a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ac6a-113">-Name</span></span>
<span data-ttu-id="9ac6a-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ac6a-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac6a-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-117">-VMName</span></span>
<span data-ttu-id="9ac6a-118">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9ac6a-119">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac6a-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ac6a-120">-Confirm</span></span>
<span data-ttu-id="9ac6a-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ac6a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ac6a-122">-WhatIf</span></span>
<span data-ttu-id="9ac6a-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ac6a-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ac6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac6a-125">CommonParameters</span></span>
<span data-ttu-id="9ac6a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac6a-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac6a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac6a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ac6a-128">INPUTS</span></span>

### <span data-ttu-id="9ac6a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac6a-129">System.String</span></span>

## <span data-ttu-id="9ac6a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ac6a-130">OUTPUTS</span></span>

### <span data-ttu-id="9ac6a-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ac6a-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9ac6a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ac6a-132">NOTES</span></span>

## <span data-ttu-id="9ac6a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ac6a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9ac6a-134">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9ac6a-134">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="9ac6a-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9ac6a-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="9ac6a-136">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9ac6a-136">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
