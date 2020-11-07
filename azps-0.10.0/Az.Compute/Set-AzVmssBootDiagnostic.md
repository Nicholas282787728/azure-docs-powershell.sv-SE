---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 482398d3ba0934f17b1381edc5dac08fb22bd75a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924761"
---
# <span data-ttu-id="20eb3-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20eb3-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="20eb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="20eb3-103">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="20eb3-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="20eb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20eb3-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20eb3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="20eb3-106">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="20eb3-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="20eb3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="20eb3-108">Exempel 1: Ange profil egenskapen för start Diagnostics för en VMSS</span><span class="sxs-lookup"><span data-stu-id="20eb3-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="20eb3-109">Det här kommandot anger start Diagnostics-egenskapen för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="20eb3-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="20eb3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20eb3-110">PARAMETERS</span></span>

### <span data-ttu-id="20eb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20eb3-111">-DefaultProfile</span></span>
<span data-ttu-id="20eb3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20eb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20eb3-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="20eb3-113">-Enabled</span></span>
<span data-ttu-id="20eb3-114">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20eb3-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="20eb3-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="20eb3-115">-StorageUri</span></span>
<span data-ttu-id="20eb3-116">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="20eb3-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="20eb3-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="20eb3-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="20eb3-118">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="20eb3-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="20eb3-119">Du kan använda New-AzVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="20eb3-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="20eb3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20eb3-120">-Confirm</span></span>
<span data-ttu-id="20eb3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20eb3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20eb3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20eb3-122">-WhatIf</span></span>
<span data-ttu-id="20eb3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20eb3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20eb3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20eb3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20eb3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20eb3-125">CommonParameters</span></span>
<span data-ttu-id="20eb3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20eb3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20eb3-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20eb3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20eb3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20eb3-128">INPUTS</span></span>

### <span data-ttu-id="20eb3-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="20eb3-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="20eb3-130">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="20eb3-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="20eb3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20eb3-131">OUTPUTS</span></span>

### <span data-ttu-id="20eb3-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="20eb3-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="20eb3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20eb3-133">NOTES</span></span>

## <span data-ttu-id="20eb3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20eb3-134">RELATED LINKS</span></span>

