---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924906"
---
# <span data-ttu-id="fd585-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fd585-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="fd585-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd585-102">SYNOPSIS</span></span>
<span data-ttu-id="fd585-103">Tar bort ett tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd585-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="fd585-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd585-104">SYNTAX</span></span>

### <span data-ttu-id="fd585-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd585-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd585-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd585-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd585-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd585-107">DESCRIPTION</span></span>
<span data-ttu-id="fd585-108">Cmdleten **Remove-AzVmssExtension** tar bort ett tillägg från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fd585-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fd585-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd585-109">EXAMPLES</span></span>

### <span data-ttu-id="fd585-110">Exempel 1: ta bort tillägget från VMSS</span><span class="sxs-lookup"><span data-stu-id="fd585-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="fd585-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd585-111">PARAMETERS</span></span>

### <span data-ttu-id="fd585-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd585-112">-DefaultProfile</span></span>
<span data-ttu-id="fd585-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd585-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd585-114">-ID</span><span class="sxs-lookup"><span data-stu-id="fd585-114">-Id</span></span>
<span data-ttu-id="fd585-115">Anger ID för tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd585-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd585-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd585-116">-Name</span></span>
<span data-ttu-id="fd585-117">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd585-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd585-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd585-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd585-119">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fd585-119">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd585-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd585-120">-Confirm</span></span>
<span data-ttu-id="fd585-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd585-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd585-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd585-122">-WhatIf</span></span>
<span data-ttu-id="fd585-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd585-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd585-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd585-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd585-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd585-125">CommonParameters</span></span>
<span data-ttu-id="fd585-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd585-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd585-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd585-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd585-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd585-128">INPUTS</span></span>

### <span data-ttu-id="fd585-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd585-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd585-130">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fd585-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="fd585-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd585-131">OUTPUTS</span></span>

### <span data-ttu-id="fd585-132">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fd585-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fd585-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd585-133">NOTES</span></span>

## <span data-ttu-id="fd585-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd585-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd585-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fd585-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
