---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573497"
---
# <span data-ttu-id="9e2d2-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="9e2d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e2d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2d2-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e2d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e2d2-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e2d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e2d2-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2d2-106">Cmdleten **Update-AzureRmVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="9e2d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e2d2-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2d2-108">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="9e2d2-109">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till statusen för ett lokalt VMSS-objekt med namnet LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="9e2d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e2d2-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2d2-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2d2-111">-ResourceGroupName</span></span>
<span data-ttu-id="9e2d2-112">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2d2-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9e2d2-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9e2d2-114">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="9e2d2-115">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="9e2d2-116">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2d2-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9e2d2-117">-VMScaleSetName</span></span>
<span data-ttu-id="9e2d2-118">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2d2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e2d2-119">-Confirm</span></span>
<span data-ttu-id="9e2d2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2d2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2d2-121">-WhatIf</span></span>
<span data-ttu-id="9e2d2-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9e2d2-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2d2-124">CommonParameters</span></span>
<span data-ttu-id="9e2d2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2d2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2d2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2d2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e2d2-127">INPUTS</span></span>

### <span data-ttu-id="9e2d2-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e2d2-128">None</span></span>
<span data-ttu-id="9e2d2-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9e2d2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e2d2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e2d2-130">OUTPUTS</span></span>

## <span data-ttu-id="9e2d2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e2d2-131">NOTES</span></span>

## <span data-ttu-id="9e2d2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e2d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e2d2-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9e2d2-139">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e2d2-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


