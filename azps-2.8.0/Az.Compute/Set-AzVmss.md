---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: ce71ad0e82e7082c199d4823c3a3a59be972ec60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744922"
---
# <span data-ttu-id="7566b-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-101">Set-AzVmss</span></span>

## <span data-ttu-id="7566b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7566b-102">SYNOPSIS</span></span>
<span data-ttu-id="7566b-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="7566b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7566b-104">SYNTAX</span></span>

### <span data-ttu-id="7566b-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="7566b-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7566b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7566b-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7566b-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7566b-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7566b-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7566b-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7566b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7566b-109">DESCRIPTION</span></span>
<span data-ttu-id="7566b-110">Cmdleten **set-AzVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7566b-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="7566b-111">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="7566b-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="7566b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7566b-112">EXAMPLES</span></span>

### <span data-ttu-id="7566b-113">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="7566b-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="7566b-114">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="7566b-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="7566b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7566b-115">PARAMETERS</span></span>

### <span data-ttu-id="7566b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7566b-116">-AsJob</span></span>
<span data-ttu-id="7566b-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="7566b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7566b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7566b-118">-DefaultProfile</span></span>
<span data-ttu-id="7566b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7566b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7566b-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7566b-120">-InstanceId</span></span>
<span data-ttu-id="7566b-121">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7566b-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7566b-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7566b-122">-PerformMaintenance</span></span>
<span data-ttu-id="7566b-123">Anger att denna cmdlet utför underhåll på en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="7566b-124">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="7566b-124">-Redeploy</span></span>
<span data-ttu-id="7566b-125">Anger att cmdleten återdistribuerar en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="7566b-126">-Ombild</span><span class="sxs-lookup"><span data-stu-id="7566b-126">-Reimage</span></span>
<span data-ttu-id="7566b-127">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="7566b-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="7566b-128">-ReimageAll</span></span>
<span data-ttu-id="7566b-129">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="7566b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7566b-130">-ResourceGroupName</span></span>
<span data-ttu-id="7566b-131">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="7566b-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="7566b-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="7566b-132">-TempDisk</span></span>
<span data-ttu-id="7566b-133">Anger om du vill att bilden ska visas igen.</span><span class="sxs-lookup"><span data-stu-id="7566b-133">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="7566b-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7566b-134">-VMScaleSetName</span></span>
<span data-ttu-id="7566b-135">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="7566b-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="7566b-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7566b-136">-Confirm</span></span>
<span data-ttu-id="7566b-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7566b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7566b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7566b-138">-WhatIf</span></span>
<span data-ttu-id="7566b-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7566b-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7566b-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7566b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7566b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7566b-141">CommonParameters</span></span>
<span data-ttu-id="7566b-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7566b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7566b-143">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7566b-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7566b-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7566b-144">INPUTS</span></span>

### <span data-ttu-id="7566b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7566b-145">System.String</span></span>

### <span data-ttu-id="7566b-146">System. string []</span><span class="sxs-lookup"><span data-stu-id="7566b-146">System.String[]</span></span>

## <span data-ttu-id="7566b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7566b-147">OUTPUTS</span></span>

### <span data-ttu-id="7566b-148">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7566b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7566b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7566b-149">NOTES</span></span>

## <span data-ttu-id="7566b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7566b-150">RELATED LINKS</span></span>

[<span data-ttu-id="7566b-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7566b-152">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7566b-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7566b-154">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7566b-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7566b-156">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="7566b-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7566b-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


