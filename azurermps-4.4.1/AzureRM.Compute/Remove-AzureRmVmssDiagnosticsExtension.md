---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4f69866d6301bc4efc0c867d35cdc7777e759ed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573694"
---
# <span data-ttu-id="1ac52-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac52-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="1ac52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ac52-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac52-103">Tar bort ett Diagnostics-tillägg från VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ac52-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ac52-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ac52-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac52-106">Cmdleten **Remove-AzureRmVmssDiagnosticsExtension** tar bort ett diagnostiktest från den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1ac52-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1ac52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ac52-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac52-108">Exempel 1: ta bort ett diagnostikverktyg från VMSS</span><span class="sxs-lookup"><span data-stu-id="1ac52-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="1ac52-109">Det här kommandot tar bort diagnostikprogrammet från VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ac52-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="1ac52-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ac52-110">PARAMETERS</span></span>

### <span data-ttu-id="1ac52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac52-111">-DefaultProfile</span></span>
<span data-ttu-id="1ac52-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac52-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ac52-113">-Name</span></span>
<span data-ttu-id="1ac52-114">Anger namnet på tillägget som tas bort från VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ac52-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac52-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ac52-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1ac52-116">Anger den VMSS varifrån tillägget ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1ac52-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac52-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ac52-117">-Confirm</span></span>
<span data-ttu-id="1ac52-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ac52-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac52-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac52-119">-WhatIf</span></span>
<span data-ttu-id="1ac52-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ac52-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ac52-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ac52-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac52-122">CommonParameters</span></span>
<span data-ttu-id="1ac52-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac52-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac52-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac52-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ac52-125">INPUTS</span></span>

## <span data-ttu-id="1ac52-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ac52-126">OUTPUTS</span></span>

###  
<span data-ttu-id="1ac52-127">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1ac52-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1ac52-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ac52-128">NOTES</span></span>

## <span data-ttu-id="1ac52-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ac52-129">RELATED LINKS</span></span>

[<span data-ttu-id="1ac52-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac52-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="1ac52-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac52-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1ac52-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1ac52-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


