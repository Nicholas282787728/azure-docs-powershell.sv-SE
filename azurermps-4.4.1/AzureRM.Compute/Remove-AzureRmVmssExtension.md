---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573691"
---
# <span data-ttu-id="8e91f-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8e91f-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8e91f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e91f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e91f-103">Tar bort ett tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e91f-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e91f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e91f-104">SYNTAX</span></span>

### <span data-ttu-id="8e91f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e91f-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e91f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e91f-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e91f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e91f-107">DESCRIPTION</span></span>
<span data-ttu-id="8e91f-108">Cmdleten **Remove-AzureRmVmssExtension** tar bort ett tillägg från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8e91f-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8e91f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e91f-109">EXAMPLES</span></span>

## <span data-ttu-id="8e91f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e91f-110">PARAMETERS</span></span>

### <span data-ttu-id="8e91f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e91f-111">-DefaultProfile</span></span>
<span data-ttu-id="8e91f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e91f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e91f-113">-ID</span><span class="sxs-lookup"><span data-stu-id="8e91f-113">-Id</span></span>
<span data-ttu-id="8e91f-114">Anger ID för tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e91f-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e91f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e91f-115">-Name</span></span>
<span data-ttu-id="8e91f-116">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e91f-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e91f-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e91f-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8e91f-118">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8e91f-118">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e91f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e91f-119">-Confirm</span></span>
<span data-ttu-id="8e91f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e91f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e91f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e91f-121">-WhatIf</span></span>
<span data-ttu-id="8e91f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e91f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e91f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e91f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e91f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e91f-124">CommonParameters</span></span>
<span data-ttu-id="8e91f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e91f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e91f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e91f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e91f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e91f-127">INPUTS</span></span>

## <span data-ttu-id="8e91f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e91f-128">OUTPUTS</span></span>

### <span data-ttu-id="8e91f-129">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8e91f-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8e91f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e91f-130">NOTES</span></span>

## <span data-ttu-id="8e91f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e91f-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e91f-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8e91f-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
