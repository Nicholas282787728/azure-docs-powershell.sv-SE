---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 206ce916e1a170bbcdf11f791a4610dd5d2172af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757901"
---
# <span data-ttu-id="bb9dc-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="bb9dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9dc-103">Stoppar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb9dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb9dc-104">SYNTAX</span></span>

### <span data-ttu-id="bb9dc-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="bb9dc-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb9dc-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="bb9dc-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb9dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb9dc-107">DESCRIPTION</span></span>
<span data-ttu-id="bb9dc-108">Cmdleten **Stop-AzureRmVmss** stoppar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="bb9dc-109">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="bb9dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb9dc-110">EXAMPLES</span></span>

### <span data-ttu-id="bb9dc-111">Exempel 1: stoppa alla virtuella datorer i VMSS</span><span class="sxs-lookup"><span data-stu-id="bb9dc-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="bb9dc-112">Det här kommandot stoppar alla virtuella datorer som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="bb9dc-113">Exempel 2: stoppa en viss uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="bb9dc-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="bb9dc-114">Det här kommandot stoppar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bb9dc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb9dc-115">PARAMETERS</span></span>

### <span data-ttu-id="bb9dc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb9dc-116">-AsJob</span></span>
<span data-ttu-id="bb9dc-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9dc-118">-DefaultProfile</span></span>
<span data-ttu-id="bb9dc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb9dc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb9dc-120">-Force</span></span>
<span data-ttu-id="bb9dc-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bb9dc-122">-InstanceId</span></span>
<span data-ttu-id="bb9dc-123">Anger, som en sträng mat ris, ID: t för de virtuella dator instanserna som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="bb9dc-124">Till exempel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="bb9dc-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb9dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb9dc-126">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="bb9dc-127">-StayProvisioned</span></span>
<span data-ttu-id="bb9dc-128">Om det här alternativet anges kommer den virtuella datorn att ange stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="bb9dc-129">Om det inte anges kommer den virtuella datorn att ange stoppat-avdelat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="bb9dc-130">Användaren debiteras fortfarande för virtuella datorer i stoppat tillstånd men inte för virtuella datorer i stoppat-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bb9dc-131">-VMScaleSetName</span></span>
<span data-ttu-id="bb9dc-132">Anger namnet på den VMSS som denna cmdlet stoppar de virtuella datorerna för.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9dc-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb9dc-133">-Confirm</span></span>
<span data-ttu-id="bb9dc-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb9dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb9dc-135">-WhatIf</span></span>
<span data-ttu-id="bb9dc-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb9dc-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb9dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9dc-138">CommonParameters</span></span>
<span data-ttu-id="bb9dc-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb9dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9dc-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9dc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9dc-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb9dc-141">INPUTS</span></span>

### <span data-ttu-id="bb9dc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bb9dc-142">System.String</span></span>

### <span data-ttu-id="bb9dc-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="bb9dc-143">System.String[]</span></span>

## <span data-ttu-id="bb9dc-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb9dc-144">OUTPUTS</span></span>

### <span data-ttu-id="bb9dc-145">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bb9dc-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bb9dc-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb9dc-146">NOTES</span></span>

## <span data-ttu-id="bb9dc-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb9dc-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb9dc-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-149">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-151">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="bb9dc-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb9dc-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


