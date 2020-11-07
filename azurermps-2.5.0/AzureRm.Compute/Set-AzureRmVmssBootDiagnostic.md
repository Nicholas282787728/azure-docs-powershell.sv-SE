---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928902"
---
# <span data-ttu-id="70970-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="70970-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="70970-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70970-102">SYNOPSIS</span></span>
<span data-ttu-id="70970-103">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="70970-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70970-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70970-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70970-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70970-105">DESCRIPTION</span></span>
<span data-ttu-id="70970-106">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="70970-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="70970-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70970-107">EXAMPLES</span></span>

### <span data-ttu-id="70970-108">Exempel 1: Ange profil egenskapen för start Diagnostics för en VMSS</span><span class="sxs-lookup"><span data-stu-id="70970-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="70970-109">Det här kommandot anger start Diagnostics-egenskapen för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="70970-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="70970-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70970-110">PARAMETERS</span></span>

### <span data-ttu-id="70970-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70970-111">-DefaultProfile</span></span>
<span data-ttu-id="70970-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70970-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70970-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="70970-113">-Enabled</span></span>
<span data-ttu-id="70970-114">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="70970-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="70970-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="70970-115">-StorageUri</span></span>
<span data-ttu-id="70970-116">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="70970-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="70970-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70970-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="70970-118">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="70970-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="70970-119">Du kan använda New-AzureRmVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="70970-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="70970-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70970-120">-Confirm</span></span>
<span data-ttu-id="70970-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70970-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70970-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70970-122">-WhatIf</span></span>
<span data-ttu-id="70970-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70970-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70970-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70970-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70970-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70970-125">CommonParameters</span></span>
<span data-ttu-id="70970-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70970-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70970-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70970-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70970-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70970-128">INPUTS</span></span>

### <span data-ttu-id="70970-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70970-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="70970-130">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="70970-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="70970-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70970-131">OUTPUTS</span></span>

### <span data-ttu-id="70970-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70970-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="70970-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70970-133">NOTES</span></span>

## <span data-ttu-id="70970-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70970-134">RELATED LINKS</span></span>

