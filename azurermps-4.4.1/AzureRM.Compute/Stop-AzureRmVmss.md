---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756355"
---
# <span data-ttu-id="36da1-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="36da1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36da1-102">SYNOPSIS</span></span>
<span data-ttu-id="36da1-103">Stoppar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="36da1-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36da1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36da1-104">SYNTAX</span></span>

### <span data-ttu-id="36da1-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="36da1-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36da1-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="36da1-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36da1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36da1-107">DESCRIPTION</span></span>
<span data-ttu-id="36da1-108">Cmdleten **Stop-AzureRmVmss** stoppar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="36da1-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="36da1-109">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="36da1-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="36da1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36da1-110">EXAMPLES</span></span>

### <span data-ttu-id="36da1-111">Exempel 1: stoppa alla virtuella datorer i VMSS</span><span class="sxs-lookup"><span data-stu-id="36da1-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="36da1-112">Det här kommandot stoppar alla virtuella datorer som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="36da1-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="36da1-113">Exempel 2: stoppa en viss uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="36da1-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="36da1-114">Det här kommandot stoppar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="36da1-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="36da1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36da1-115">PARAMETERS</span></span>

### <span data-ttu-id="36da1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36da1-116">-DefaultProfile</span></span>
<span data-ttu-id="36da1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36da1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36da1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36da1-118">-Force</span></span>
<span data-ttu-id="36da1-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="36da1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36da1-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36da1-120">-InstanceId</span></span>
<span data-ttu-id="36da1-121">Anger, som en sträng mat ris, ID: t för de virtuella dator instanserna som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="36da1-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="36da1-122">Till exempel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="36da1-122">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="36da1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36da1-123">-ResourceGroupName</span></span>
<span data-ttu-id="36da1-124">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="36da1-124">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="36da1-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="36da1-125">-StayProvisioned</span></span>
<span data-ttu-id="36da1-126">Om det här alternativet anges kommer den virtuella datorn att ange stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="36da1-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="36da1-127">Om det inte anges kommer den virtuella datorn att ange stoppat-avdelat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="36da1-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="36da1-128">Användaren debiteras fortfarande för virtuella datorer i stoppat tillstånd men inte för virtuella datorer i stoppat-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="36da1-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="36da1-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36da1-129">-VMScaleSetName</span></span>
<span data-ttu-id="36da1-130">Anger namnet på den VMSS som denna cmdlet stoppar de virtuella datorerna för.</span><span class="sxs-lookup"><span data-stu-id="36da1-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="36da1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36da1-131">-Confirm</span></span>
<span data-ttu-id="36da1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36da1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36da1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36da1-133">-WhatIf</span></span>
<span data-ttu-id="36da1-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36da1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36da1-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36da1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36da1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36da1-136">CommonParameters</span></span>
<span data-ttu-id="36da1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36da1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36da1-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36da1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36da1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36da1-139">INPUTS</span></span>

## <span data-ttu-id="36da1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36da1-140">OUTPUTS</span></span>

## <span data-ttu-id="36da1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36da1-141">NOTES</span></span>

## <span data-ttu-id="36da1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36da1-142">RELATED LINKS</span></span>

[<span data-ttu-id="36da1-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="36da1-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="36da1-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="36da1-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="36da1-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="36da1-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="36da1-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36da1-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


