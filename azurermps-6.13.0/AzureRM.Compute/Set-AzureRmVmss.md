---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575260"
---
# <span data-ttu-id="6a69c-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="6a69c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a69c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a69c-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a69c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a69c-104">SYNTAX</span></span>

### <span data-ttu-id="6a69c-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="6a69c-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a69c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6a69c-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a69c-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="6a69c-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a69c-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="6a69c-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a69c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a69c-109">DESCRIPTION</span></span>
<span data-ttu-id="6a69c-110">Cmdleten **set-AzureRmVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6a69c-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6a69c-111">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="6a69c-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="6a69c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a69c-112">EXAMPLES</span></span>

### <span data-ttu-id="6a69c-113">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="6a69c-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="6a69c-114">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="6a69c-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="6a69c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a69c-115">PARAMETERS</span></span>

### <span data-ttu-id="6a69c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a69c-116">-AsJob</span></span>
<span data-ttu-id="6a69c-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="6a69c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6a69c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a69c-118">-DefaultProfile</span></span>
<span data-ttu-id="6a69c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a69c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a69c-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6a69c-120">-InstanceId</span></span>
<span data-ttu-id="6a69c-121">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6a69c-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="6a69c-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="6a69c-122">-PerformMaintenance</span></span>
<span data-ttu-id="6a69c-123">Anger att denna cmdlet utför underhåll på en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="6a69c-124">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="6a69c-124">-Redeploy</span></span>
<span data-ttu-id="6a69c-125">Anger att cmdleten återdistribuerar en eller flera virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="6a69c-126">-Ombild</span><span class="sxs-lookup"><span data-stu-id="6a69c-126">-Reimage</span></span>
<span data-ttu-id="6a69c-127">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="6a69c-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="6a69c-128">-ReimageAll</span></span>
<span data-ttu-id="6a69c-129">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="6a69c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a69c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6a69c-131">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a69c-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6a69c-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6a69c-132">-VMScaleSetName</span></span>
<span data-ttu-id="6a69c-133">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="6a69c-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="6a69c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a69c-134">-Confirm</span></span>
<span data-ttu-id="6a69c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a69c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a69c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a69c-136">-WhatIf</span></span>
<span data-ttu-id="6a69c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a69c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a69c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a69c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a69c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a69c-139">CommonParameters</span></span>
<span data-ttu-id="6a69c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a69c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a69c-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a69c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a69c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a69c-142">INPUTS</span></span>

### <span data-ttu-id="6a69c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6a69c-143">System.String</span></span>

### <span data-ttu-id="6a69c-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="6a69c-144">System.String[]</span></span>

## <span data-ttu-id="6a69c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a69c-145">OUTPUTS</span></span>

### <span data-ttu-id="6a69c-146">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6a69c-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6a69c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a69c-147">NOTES</span></span>

## <span data-ttu-id="6a69c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a69c-148">RELATED LINKS</span></span>

[<span data-ttu-id="6a69c-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="6a69c-150">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="6a69c-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="6a69c-152">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="6a69c-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="6a69c-154">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="6a69c-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a69c-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


