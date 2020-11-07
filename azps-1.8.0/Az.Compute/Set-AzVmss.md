---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 99f022f539ff5db9bb99537bb87fce8a8567947c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917221"
---
# <span data-ttu-id="2569e-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-101">Set-AzVmss</span></span>

## <span data-ttu-id="2569e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2569e-102">SYNOPSIS</span></span>
<span data-ttu-id="2569e-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="2569e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2569e-104">SYNTAX</span></span>

### <span data-ttu-id="2569e-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="2569e-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2569e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2569e-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2569e-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="2569e-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2569e-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="2569e-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2569e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2569e-109">DESCRIPTION</span></span>
<span data-ttu-id="2569e-110">Cmdleten **set-AzVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2569e-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="2569e-111">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="2569e-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="2569e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2569e-112">EXAMPLES</span></span>

### <span data-ttu-id="2569e-113">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="2569e-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="2569e-114">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="2569e-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="2569e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2569e-115">PARAMETERS</span></span>

### <span data-ttu-id="2569e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2569e-116">-AsJob</span></span>
<span data-ttu-id="2569e-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="2569e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2569e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2569e-118">-DefaultProfile</span></span>
<span data-ttu-id="2569e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2569e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2569e-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2569e-120">-InstanceId</span></span>
<span data-ttu-id="2569e-121">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2569e-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="2569e-122">-PerformMaintenance</span></span>
<span data-ttu-id="2569e-123">Anger att denna cmdlet utför underhåll på en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-124">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="2569e-124">-Redeploy</span></span>
<span data-ttu-id="2569e-125">Anger att cmdleten återdistribuerar en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-126">-Ombild</span><span class="sxs-lookup"><span data-stu-id="2569e-126">-Reimage</span></span>
<span data-ttu-id="2569e-127">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="2569e-128">-ReimageAll</span></span>
<span data-ttu-id="2569e-129">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="2569e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2569e-130">-ResourceGroupName</span></span>
<span data-ttu-id="2569e-131">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="2569e-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="2569e-132">-TempDisk</span></span>
<span data-ttu-id="2569e-133">Anger om du vill att bilden ska visas igen.</span><span class="sxs-lookup"><span data-stu-id="2569e-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2569e-134">-VMScaleSetName</span></span>
<span data-ttu-id="2569e-135">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="2569e-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2569e-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2569e-136">-Confirm</span></span>
<span data-ttu-id="2569e-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2569e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2569e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2569e-138">-WhatIf</span></span>
<span data-ttu-id="2569e-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2569e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2569e-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2569e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2569e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2569e-141">CommonParameters</span></span>
<span data-ttu-id="2569e-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2569e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2569e-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2569e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2569e-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2569e-144">INPUTS</span></span>

### <span data-ttu-id="2569e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2569e-145">System.String</span></span>

### <span data-ttu-id="2569e-146">System. string []</span><span class="sxs-lookup"><span data-stu-id="2569e-146">System.String[]</span></span>

## <span data-ttu-id="2569e-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2569e-147">OUTPUTS</span></span>

### <span data-ttu-id="2569e-148">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2569e-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2569e-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2569e-149">NOTES</span></span>

## <span data-ttu-id="2569e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2569e-150">RELATED LINKS</span></span>

[<span data-ttu-id="2569e-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="2569e-152">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="2569e-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="2569e-154">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="2569e-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="2569e-156">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="2569e-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2569e-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


