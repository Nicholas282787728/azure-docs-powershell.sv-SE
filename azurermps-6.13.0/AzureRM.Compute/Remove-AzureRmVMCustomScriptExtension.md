---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757911"
---
# <span data-ttu-id="72cca-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72cca-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="72cca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72cca-102">SYNOPSIS</span></span>
<span data-ttu-id="72cca-103">Tar bort ett anpassat skript tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="72cca-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72cca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72cca-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72cca-105">DESCRIPTION</span></span>
<span data-ttu-id="72cca-106">Cmdleten **Remove-AzureRmVMCustomScriptExtension** tar bort ett anpassat tillägg för virtuella skript från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="72cca-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="72cca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72cca-107">EXAMPLES</span></span>

## <span data-ttu-id="72cca-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72cca-108">PARAMETERS</span></span>

### <span data-ttu-id="72cca-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cca-109">-DefaultProfile</span></span>
<span data-ttu-id="72cca-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72cca-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cca-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72cca-111">-Force</span></span>
<span data-ttu-id="72cca-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="72cca-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72cca-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="72cca-113">-Name</span></span>
<span data-ttu-id="72cca-114">Anger namnet på det anpassade skript tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cca-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72cca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72cca-115">-ResourceGroupName</span></span>
<span data-ttu-id="72cca-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="72cca-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="72cca-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="72cca-117">-VMName</span></span>
<span data-ttu-id="72cca-118">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="72cca-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="72cca-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72cca-119">-Confirm</span></span>
<span data-ttu-id="72cca-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72cca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cca-121">-WhatIf</span></span>
<span data-ttu-id="72cca-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72cca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cca-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72cca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cca-124">CommonParameters</span></span>
<span data-ttu-id="72cca-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cca-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cca-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72cca-127">INPUTS</span></span>

### <span data-ttu-id="72cca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="72cca-128">System.String</span></span>

## <span data-ttu-id="72cca-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72cca-129">OUTPUTS</span></span>

### <span data-ttu-id="72cca-130">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72cca-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72cca-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72cca-131">NOTES</span></span>

## <span data-ttu-id="72cca-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72cca-132">RELATED LINKS</span></span>

[<span data-ttu-id="72cca-133">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72cca-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="72cca-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72cca-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
