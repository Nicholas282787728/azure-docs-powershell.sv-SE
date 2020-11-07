---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86fb5997c93aecbaa5aabd07255ae6bde840e91f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931029"
---
# <span data-ttu-id="ab17b-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="ab17b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab17b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab17b-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ab17b-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab17b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab17b-104">SYNTAX</span></span>

### <span data-ttu-id="ab17b-105">RestartResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="ab17b-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab17b-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab17b-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab17b-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab17b-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab17b-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab17b-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab17b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab17b-109">DESCRIPTION</span></span>
<span data-ttu-id="ab17b-110">Cmdleten **restart-AzureRmVM** startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ab17b-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ab17b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab17b-111">EXAMPLES</span></span>

### <span data-ttu-id="ab17b-112">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ab17b-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ab17b-113">Det här kommandot startar om den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ab17b-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ab17b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab17b-114">PARAMETERS</span></span>

### <span data-ttu-id="ab17b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab17b-115">-AsJob</span></span>
<span data-ttu-id="ab17b-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ab17b-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ab17b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab17b-117">-DefaultProfile</span></span>
<span data-ttu-id="ab17b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab17b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab17b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ab17b-119">-Id</span></span>
<span data-ttu-id="ab17b-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ab17b-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab17b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab17b-121">-Name</span></span>
<span data-ttu-id="ab17b-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="ab17b-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="ab17b-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ab17b-123">-PerformMaintenance</span></span>
<span data-ttu-id="ab17b-124">För att utföra underhåll av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ab17b-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab17b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab17b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab17b-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ab17b-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab17b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab17b-127">-Confirm</span></span>
<span data-ttu-id="ab17b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab17b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab17b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab17b-129">-WhatIf</span></span>
<span data-ttu-id="ab17b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab17b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab17b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab17b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab17b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab17b-132">CommonParameters</span></span>
<span data-ttu-id="ab17b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab17b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab17b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab17b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab17b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab17b-135">INPUTS</span></span>

### <span data-ttu-id="ab17b-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="ab17b-136">None</span></span>
<span data-ttu-id="ab17b-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ab17b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab17b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab17b-138">OUTPUTS</span></span>

### <span data-ttu-id="ab17b-139">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ab17b-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ab17b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab17b-140">NOTES</span></span>

## <span data-ttu-id="ab17b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab17b-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab17b-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ab17b-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ab17b-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ab17b-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ab17b-146">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ab17b-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab17b-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


