---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 50fd6447448968527b942e163f520142f594b7a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929441"
---
# <span data-ttu-id="b4be0-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="b4be0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4be0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4be0-103">Stoppar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be0-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4be0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4be0-104">SYNTAX</span></span>

### <span data-ttu-id="b4be0-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="b4be0-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4be0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b4be0-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4be0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4be0-107">DESCRIPTION</span></span>
<span data-ttu-id="b4be0-108">Cmdleten **Stop-AzureRmVmss** stoppar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="b4be0-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="b4be0-109">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="b4be0-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="b4be0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4be0-110">EXAMPLES</span></span>

### <span data-ttu-id="b4be0-111">Exempel 1: stoppa alla virtuella datorer i VMSS</span><span class="sxs-lookup"><span data-stu-id="b4be0-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b4be0-112">Det här kommandot stoppar alla virtuella datorer som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be0-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="b4be0-113">Exempel 2: stoppa en viss uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="b4be0-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="b4be0-114">Det här kommandot stoppar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be0-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b4be0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4be0-115">PARAMETERS</span></span>

### <span data-ttu-id="b4be0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4be0-116">-AsJob</span></span>
<span data-ttu-id="b4be0-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="b4be0-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b4be0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4be0-118">-DefaultProfile</span></span>
<span data-ttu-id="b4be0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4be0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4be0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b4be0-120">-Force</span></span>
<span data-ttu-id="b4be0-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b4be0-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4be0-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b4be0-122">-InstanceId</span></span>
<span data-ttu-id="b4be0-123">Anger, som en sträng mat ris, ID: t för de virtuella dator instanserna som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="b4be0-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="b4be0-124">Till exempel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="b4be0-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="b4be0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4be0-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4be0-126">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4be0-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b4be0-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b4be0-127">-StayProvisioned</span></span>
<span data-ttu-id="b4be0-128">Om det här alternativet anges kommer den virtuella datorn att ange stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b4be0-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="b4be0-129">Om det inte anges kommer den virtuella datorn att ange stoppat-avdelat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b4be0-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="b4be0-130">Användaren debiteras fortfarande för virtuella datorer i stoppat tillstånd men inte för virtuella datorer i stoppat-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b4be0-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4be0-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b4be0-131">-VMScaleSetName</span></span>
<span data-ttu-id="b4be0-132">Anger namnet på den VMSS som denna cmdlet stoppar de virtuella datorerna för.</span><span class="sxs-lookup"><span data-stu-id="b4be0-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="b4be0-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4be0-133">-Confirm</span></span>
<span data-ttu-id="b4be0-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4be0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4be0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4be0-135">-WhatIf</span></span>
<span data-ttu-id="b4be0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4be0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4be0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4be0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4be0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4be0-138">CommonParameters</span></span>
<span data-ttu-id="b4be0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4be0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4be0-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4be0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4be0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4be0-141">INPUTS</span></span>

### <span data-ttu-id="b4be0-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4be0-142">None</span></span>
<span data-ttu-id="b4be0-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b4be0-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4be0-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4be0-144">OUTPUTS</span></span>

### <span data-ttu-id="b4be0-145">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b4be0-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b4be0-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4be0-146">NOTES</span></span>

## <span data-ttu-id="b4be0-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4be0-147">RELATED LINKS</span></span>

[<span data-ttu-id="b4be0-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b4be0-149">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b4be0-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b4be0-151">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b4be0-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b4be0-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b4be0-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4be0-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


