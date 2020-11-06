---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578276"
---
# <span data-ttu-id="1f778-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1f778-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="1f778-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f778-102">SYNOPSIS</span></span>
<span data-ttu-id="1f778-103">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="1f778-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f778-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f778-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f778-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f778-105">DESCRIPTION</span></span>
<span data-ttu-id="1f778-106">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="1f778-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="1f778-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f778-107">EXAMPLES</span></span>

### <span data-ttu-id="1f778-108">Exempel 1: Ange profil egenskapen för start Diagnostics för en VMSS</span><span class="sxs-lookup"><span data-stu-id="1f778-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="1f778-109">Det här kommandot anger start Diagnostics-egenskapen för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="1f778-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1f778-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f778-110">PARAMETERS</span></span>

### <span data-ttu-id="1f778-111">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="1f778-111">-Enabled</span></span>
<span data-ttu-id="1f778-112">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="1f778-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f778-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1f778-113">-StorageUri</span></span>
<span data-ttu-id="1f778-114">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="1f778-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f778-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f778-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1f778-116">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="1f778-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="1f778-117">Du kan använda New-AzureRmVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="1f778-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f778-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f778-118">-Confirm</span></span>
<span data-ttu-id="1f778-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f778-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f778-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f778-120">-WhatIf</span></span>
<span data-ttu-id="1f778-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f778-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f778-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f778-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f778-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f778-123">CommonParameters</span></span>
<span data-ttu-id="1f778-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f778-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f778-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f778-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f778-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f778-126">INPUTS</span></span>

### <span data-ttu-id="1f778-127">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f778-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="1f778-128">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="1f778-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="1f778-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f778-129">OUTPUTS</span></span>

### <span data-ttu-id="1f778-130">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f778-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="1f778-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f778-131">NOTES</span></span>

## <span data-ttu-id="1f778-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f778-132">RELATED LINKS</span></span>

