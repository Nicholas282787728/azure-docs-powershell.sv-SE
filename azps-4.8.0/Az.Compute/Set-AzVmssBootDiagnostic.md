---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260808"
---
# <span data-ttu-id="4abe5-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4abe5-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="4abe5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4abe5-102">SYNOPSIS</span></span>
<span data-ttu-id="4abe5-103">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="4abe5-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="4abe5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4abe5-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abe5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4abe5-105">DESCRIPTION</span></span>
<span data-ttu-id="4abe5-106">Anger den virtuella datorns skalnings profil för Autostart.</span><span class="sxs-lookup"><span data-stu-id="4abe5-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="4abe5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4abe5-107">EXAMPLES</span></span>

### <span data-ttu-id="4abe5-108">Exempel 1: Ange profil egenskapen för start Diagnostics för en VMSS</span><span class="sxs-lookup"><span data-stu-id="4abe5-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="4abe5-109">Det här kommandot anger start Diagnostics-egenskapen för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="4abe5-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4abe5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4abe5-110">PARAMETERS</span></span>

### <span data-ttu-id="4abe5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abe5-111">-DefaultProfile</span></span>
<span data-ttu-id="4abe5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4abe5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4abe5-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="4abe5-113">-Enabled</span></span>
<span data-ttu-id="4abe5-114">Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4abe5-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abe5-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4abe5-115">-StorageUri</span></span>
<span data-ttu-id="4abe5-116">URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.</span><span class="sxs-lookup"><span data-stu-id="4abe5-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abe5-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4abe5-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4abe5-118">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="4abe5-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="4abe5-119">Du kan använda New-AzVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="4abe5-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4abe5-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4abe5-120">-Confirm</span></span>
<span data-ttu-id="4abe5-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4abe5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abe5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abe5-122">-WhatIf</span></span>
<span data-ttu-id="4abe5-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4abe5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4abe5-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4abe5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abe5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abe5-125">CommonParameters</span></span>
<span data-ttu-id="4abe5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abe5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abe5-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4abe5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abe5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4abe5-128">INPUTS</span></span>

### <span data-ttu-id="4abe5-129">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4abe5-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4abe5-130">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4abe5-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4abe5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4abe5-131">System.String</span></span>

## <span data-ttu-id="4abe5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4abe5-132">OUTPUTS</span></span>

### <span data-ttu-id="4abe5-133">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4abe5-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4abe5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4abe5-134">NOTES</span></span>

## <span data-ttu-id="4abe5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4abe5-135">RELATED LINKS</span></span>
