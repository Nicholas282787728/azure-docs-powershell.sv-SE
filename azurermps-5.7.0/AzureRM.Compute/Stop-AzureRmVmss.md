---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584407"
---
# <span data-ttu-id="84b33-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="84b33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84b33-102">SYNOPSIS</span></span>
<span data-ttu-id="84b33-103">Stoppar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="84b33-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84b33-104">SYNTAX</span></span>

### <span data-ttu-id="84b33-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="84b33-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b33-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="84b33-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b33-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84b33-107">DESCRIPTION</span></span>
<span data-ttu-id="84b33-108">Cmdleten **Stop-AzureRmVmss** stoppar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="84b33-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="84b33-109">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="84b33-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="84b33-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84b33-110">EXAMPLES</span></span>

### <span data-ttu-id="84b33-111">Exempel 1: stoppa alla virtuella datorer i VMSS</span><span class="sxs-lookup"><span data-stu-id="84b33-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="84b33-112">Det här kommandot stoppar alla virtuella datorer som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="84b33-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="84b33-113">Exempel 2: stoppa en viss uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="84b33-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="84b33-114">Det här kommandot stoppar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="84b33-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="84b33-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84b33-115">PARAMETERS</span></span>

### <span data-ttu-id="84b33-116">-Force</span><span class="sxs-lookup"><span data-stu-id="84b33-116">-Force</span></span>
<span data-ttu-id="84b33-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="84b33-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b33-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="84b33-118">-InstanceId</span></span>
<span data-ttu-id="84b33-119">Anger, som en sträng mat ris, ID: t för de virtuella dator instanserna som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="84b33-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="84b33-120">Till exempel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="84b33-120">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b33-121">-ResourceGroupName</span></span>
<span data-ttu-id="84b33-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="84b33-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="84b33-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="84b33-123">-StayProvisioned</span></span>
<span data-ttu-id="84b33-124">Om det här alternativet anges kommer den virtuella datorn att ange stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="84b33-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="84b33-125">Om det inte anges kommer den virtuella datorn att ange stoppat-avdelat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="84b33-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="84b33-126">Användaren debiteras fortfarande för virtuella datorer i stoppat tillstånd men inte för virtuella datorer i stoppat-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="84b33-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b33-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="84b33-127">-VMScaleSetName</span></span>
<span data-ttu-id="84b33-128">Anger namnet på den VMSS som denna cmdlet stoppar de virtuella datorerna för.</span><span class="sxs-lookup"><span data-stu-id="84b33-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b33-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84b33-129">-Confirm</span></span>
<span data-ttu-id="84b33-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84b33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b33-131">-WhatIf</span></span>
<span data-ttu-id="84b33-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84b33-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84b33-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84b33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b33-134">CommonParameters</span></span>
<span data-ttu-id="84b33-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b33-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b33-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b33-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84b33-137">INPUTS</span></span>

### <span data-ttu-id="84b33-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="84b33-138">None</span></span>
<span data-ttu-id="84b33-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="84b33-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84b33-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84b33-140">OUTPUTS</span></span>

## <span data-ttu-id="84b33-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84b33-141">NOTES</span></span>

## <span data-ttu-id="84b33-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84b33-142">RELATED LINKS</span></span>

[<span data-ttu-id="84b33-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="84b33-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="84b33-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="84b33-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="84b33-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="84b33-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="84b33-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="84b33-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


