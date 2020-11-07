---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744906"
---
# <span data-ttu-id="79851-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="79851-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="79851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79851-102">SYNOPSIS</span></span>
<span data-ttu-id="79851-103">Ändrar tillstånd för en VMSS-instans.</span><span class="sxs-lookup"><span data-stu-id="79851-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="79851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79851-104">SYNTAX</span></span>

### <span data-ttu-id="79851-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="79851-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79851-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="79851-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79851-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="79851-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79851-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="79851-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79851-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79851-109">DESCRIPTION</span></span>
<span data-ttu-id="79851-110">Cmdleten **set-AzVmssVM** ändrar tillståndet för en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="79851-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="79851-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79851-111">EXAMPLES</span></span>

## <span data-ttu-id="79851-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79851-112">PARAMETERS</span></span>

### <span data-ttu-id="79851-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79851-113">-AsJob</span></span>
<span data-ttu-id="79851-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="79851-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79851-115">-DefaultProfile</span></span>
<span data-ttu-id="79851-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79851-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79851-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="79851-117">-InstanceId</span></span>
<span data-ttu-id="79851-118">Anger ID för den VMSS-instans som denna cmdlet ändrar tillstånd för.</span><span class="sxs-lookup"><span data-stu-id="79851-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79851-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="79851-119">-PerformMaintenance</span></span>
<span data-ttu-id="79851-120">Anger att denna cmdlet utför underhåll på en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="79851-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="79851-121">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="79851-121">-Redeploy</span></span>
<span data-ttu-id="79851-122">Anger att denna cmdlet omdistribuerar en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="79851-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="79851-123">-Ombild</span><span class="sxs-lookup"><span data-stu-id="79851-123">-Reimage</span></span>
<span data-ttu-id="79851-124">Anger att denna cmdlet ombildar VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="79851-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="79851-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="79851-125">-ReimageAll</span></span>
<span data-ttu-id="79851-126">Anger att cmdleten återavbildningar alla diskar i VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="79851-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="79851-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79851-127">-ResourceGroupName</span></span>
<span data-ttu-id="79851-128">Anger namnet på den resurs grupp som innehåller VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="79851-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="79851-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="79851-129">-VMScaleSetName</span></span>
<span data-ttu-id="79851-130">Anger namnet på den VMSS-instans som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="79851-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="79851-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79851-131">-Confirm</span></span>
<span data-ttu-id="79851-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79851-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79851-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79851-133">-WhatIf</span></span>
<span data-ttu-id="79851-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79851-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79851-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79851-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79851-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79851-136">CommonParameters</span></span>
<span data-ttu-id="79851-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79851-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79851-138">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79851-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79851-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79851-139">INPUTS</span></span>

### <span data-ttu-id="79851-140">System. String</span><span class="sxs-lookup"><span data-stu-id="79851-140">System.String</span></span>

## <span data-ttu-id="79851-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79851-141">OUTPUTS</span></span>

### <span data-ttu-id="79851-142">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="79851-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="79851-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79851-143">NOTES</span></span>

## <span data-ttu-id="79851-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79851-144">RELATED LINKS</span></span>

[<span data-ttu-id="79851-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="79851-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)