---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930630"
---
# <span data-ttu-id="4ebbc-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4ebbc-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="4ebbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ebbc-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebbc-103">Tar bort ett anpassat skript tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ebbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ebbc-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebbc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ebbc-105">DESCRIPTION</span></span>
<span data-ttu-id="4ebbc-106">Cmdleten **Remove-AzureRmVMCustomScriptExtension** tar bort ett anpassat tillägg för virtuella skript från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="4ebbc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ebbc-107">EXAMPLES</span></span>

## <span data-ttu-id="4ebbc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ebbc-108">PARAMETERS</span></span>

### <span data-ttu-id="4ebbc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebbc-109">-DefaultProfile</span></span>
<span data-ttu-id="4ebbc-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ebbc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4ebbc-111">-Force</span></span>
<span data-ttu-id="4ebbc-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ebbc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ebbc-113">-Name</span></span>
<span data-ttu-id="4ebbc-114">Anger namnet på det anpassade skript tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ebbc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebbc-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ebbc-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4ebbc-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="4ebbc-117">-VMName</span></span>
<span data-ttu-id="4ebbc-118">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="4ebbc-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ebbc-119">-Confirm</span></span>
<span data-ttu-id="4ebbc-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebbc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebbc-121">-WhatIf</span></span>
<span data-ttu-id="4ebbc-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4ebbc-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ebbc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebbc-124">CommonParameters</span></span>
<span data-ttu-id="4ebbc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebbc-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebbc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebbc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ebbc-127">INPUTS</span></span>

### <span data-ttu-id="4ebbc-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ebbc-128">None</span></span>
<span data-ttu-id="4ebbc-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ebbc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ebbc-130">OUTPUTS</span></span>

### <span data-ttu-id="4ebbc-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4ebbc-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4ebbc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ebbc-132">NOTES</span></span>

## <span data-ttu-id="4ebbc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ebbc-133">RELATED LINKS</span></span>

[<span data-ttu-id="4ebbc-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4ebbc-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="4ebbc-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4ebbc-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
