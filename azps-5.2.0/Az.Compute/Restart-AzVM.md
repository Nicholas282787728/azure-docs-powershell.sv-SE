---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394152"
---
# <span data-ttu-id="0ff87-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-101">Restart-AzVM</span></span>

## <span data-ttu-id="0ff87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ff87-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff87-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="0ff87-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="0ff87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ff87-104">SYNTAX</span></span>

### <span data-ttu-id="0ff87-105">RestartResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="0ff87-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff87-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0ff87-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff87-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0ff87-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ff87-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0ff87-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff87-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ff87-109">DESCRIPTION</span></span>
<span data-ttu-id="0ff87-110">Cmdleten **restart-AzVM** startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="0ff87-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="0ff87-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ff87-111">EXAMPLES</span></span>

### <span data-ttu-id="0ff87-112">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="0ff87-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0ff87-113">Det här kommandot startar om den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0ff87-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0ff87-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ff87-114">PARAMETERS</span></span>

### <span data-ttu-id="0ff87-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ff87-115">-AsJob</span></span>
<span data-ttu-id="0ff87-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="0ff87-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0ff87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff87-117">-DefaultProfile</span></span>
<span data-ttu-id="0ff87-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff87-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0ff87-119">-Id</span></span>
<span data-ttu-id="0ff87-120">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0ff87-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff87-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ff87-121">-Name</span></span>
<span data-ttu-id="0ff87-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="0ff87-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff87-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0ff87-123">-NoWait</span></span>
<span data-ttu-id="0ff87-124">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="0ff87-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0ff87-125">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="0ff87-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0ff87-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="0ff87-126">-PerformMaintenance</span></span>
<span data-ttu-id="0ff87-127">För att utföra underhåll av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0ff87-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff87-128">-ResourceGroupName</span></span>
<span data-ttu-id="0ff87-129">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0ff87-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff87-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ff87-130">-Confirm</span></span>
<span data-ttu-id="0ff87-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ff87-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff87-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff87-132">-WhatIf</span></span>
<span data-ttu-id="0ff87-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ff87-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff87-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ff87-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff87-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff87-135">CommonParameters</span></span>
<span data-ttu-id="0ff87-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff87-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff87-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ff87-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff87-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ff87-138">INPUTS</span></span>

### <span data-ttu-id="0ff87-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff87-139">System.String</span></span>

### <span data-ttu-id="0ff87-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ff87-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ff87-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ff87-141">OUTPUTS</span></span>

### <span data-ttu-id="0ff87-142">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="0ff87-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="0ff87-143">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ff87-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0ff87-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ff87-144">NOTES</span></span>

## <span data-ttu-id="0ff87-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ff87-145">RELATED LINKS</span></span>

[<span data-ttu-id="0ff87-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0ff87-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="0ff87-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0ff87-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="0ff87-150">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0ff87-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ff87-151">Update-AzVM</span></span>](./Update-AzVM.md)


