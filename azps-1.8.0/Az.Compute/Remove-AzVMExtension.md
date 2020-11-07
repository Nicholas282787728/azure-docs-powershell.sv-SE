---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: ce16c011d07d47dcbbfd0a957323955904751c82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917293"
---
# <span data-ttu-id="75c63-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="75c63-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="75c63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75c63-102">SYNOPSIS</span></span>
<span data-ttu-id="75c63-103">Tar bort ett tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="75c63-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="75c63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75c63-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c63-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75c63-105">DESCRIPTION</span></span>
<span data-ttu-id="75c63-106">Cmdleten **Remove-AzVMExtension** tar bort ett tillägg från virtuella dator tillägg på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="75c63-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="75c63-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75c63-107">EXAMPLES</span></span>

### <span data-ttu-id="75c63-108">Exempel 1: ta bort ett tillägg från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="75c63-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="75c63-109">Det här kommandot tar bort tillägget med namnet ContosoTest från den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="75c63-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="75c63-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75c63-110">PARAMETERS</span></span>

### <span data-ttu-id="75c63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c63-111">-DefaultProfile</span></span>
<span data-ttu-id="75c63-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75c63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c63-113">-Force</span><span class="sxs-lookup"><span data-stu-id="75c63-113">-Force</span></span>
<span data-ttu-id="75c63-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="75c63-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75c63-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="75c63-115">-Name</span></span>
<span data-ttu-id="75c63-116">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c63-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="75c63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c63-117">-ResourceGroupName</span></span>
<span data-ttu-id="75c63-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="75c63-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="75c63-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="75c63-119">-VMName</span></span>
<span data-ttu-id="75c63-120">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort tillägget.</span><span class="sxs-lookup"><span data-stu-id="75c63-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="75c63-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75c63-121">-Confirm</span></span>
<span data-ttu-id="75c63-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75c63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c63-123">-WhatIf</span></span>
<span data-ttu-id="75c63-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75c63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c63-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75c63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c63-126">CommonParameters</span></span>
<span data-ttu-id="75c63-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c63-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c63-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c63-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75c63-129">INPUTS</span></span>

### <span data-ttu-id="75c63-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75c63-130">System.String</span></span>

## <span data-ttu-id="75c63-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75c63-131">OUTPUTS</span></span>

### <span data-ttu-id="75c63-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="75c63-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="75c63-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75c63-133">NOTES</span></span>

## <span data-ttu-id="75c63-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75c63-134">RELATED LINKS</span></span>

[<span data-ttu-id="75c63-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="75c63-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="75c63-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="75c63-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


