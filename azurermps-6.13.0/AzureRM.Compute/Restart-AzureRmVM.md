---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575267"
---
# <span data-ttu-id="48b44-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="48b44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48b44-102">SYNOPSIS</span></span>
<span data-ttu-id="48b44-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="48b44-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48b44-104">SYNTAX</span></span>

### <span data-ttu-id="48b44-105">RestartResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="48b44-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b44-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="48b44-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b44-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="48b44-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b44-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="48b44-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b44-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48b44-109">DESCRIPTION</span></span>
<span data-ttu-id="48b44-110">Cmdleten **restart-AzureRmVM** startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="48b44-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="48b44-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48b44-111">EXAMPLES</span></span>

### <span data-ttu-id="48b44-112">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="48b44-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="48b44-113">Det här kommandot startar om den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="48b44-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="48b44-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48b44-114">PARAMETERS</span></span>

### <span data-ttu-id="48b44-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48b44-115">-AsJob</span></span>
<span data-ttu-id="48b44-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="48b44-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="48b44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b44-117">-DefaultProfile</span></span>
<span data-ttu-id="48b44-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48b44-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b44-119">-ID</span><span class="sxs-lookup"><span data-stu-id="48b44-119">-Id</span></span>
<span data-ttu-id="48b44-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="48b44-120">The resource group name.</span></span>

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

### <span data-ttu-id="48b44-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="48b44-121">-Name</span></span>
<span data-ttu-id="48b44-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="48b44-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="48b44-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="48b44-123">-PerformMaintenance</span></span>
<span data-ttu-id="48b44-124">För att utföra underhåll av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="48b44-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="48b44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b44-125">-ResourceGroupName</span></span>
<span data-ttu-id="48b44-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="48b44-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="48b44-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48b44-127">-Confirm</span></span>
<span data-ttu-id="48b44-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48b44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b44-129">-WhatIf</span></span>
<span data-ttu-id="48b44-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48b44-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48b44-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48b44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b44-132">CommonParameters</span></span>
<span data-ttu-id="48b44-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b44-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b44-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b44-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48b44-135">INPUTS</span></span>

### <span data-ttu-id="48b44-136">System. String</span><span class="sxs-lookup"><span data-stu-id="48b44-136">System.String</span></span>

### <span data-ttu-id="48b44-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48b44-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48b44-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48b44-138">OUTPUTS</span></span>

### <span data-ttu-id="48b44-139">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="48b44-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="48b44-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48b44-140">NOTES</span></span>

## <span data-ttu-id="48b44-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48b44-141">RELATED LINKS</span></span>

[<span data-ttu-id="48b44-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="48b44-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="48b44-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="48b44-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="48b44-146">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="48b44-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b44-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


