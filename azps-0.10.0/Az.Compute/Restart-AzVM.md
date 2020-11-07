---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924913"
---
# <span data-ttu-id="e4298-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-101">Restart-AzVM</span></span>

## <span data-ttu-id="e4298-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4298-102">SYNOPSIS</span></span>
<span data-ttu-id="e4298-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e4298-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e4298-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4298-104">SYNTAX</span></span>

### <span data-ttu-id="e4298-105">RestartResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="e4298-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4298-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e4298-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4298-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e4298-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4298-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e4298-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4298-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4298-109">DESCRIPTION</span></span>
<span data-ttu-id="e4298-110">Cmdleten **restart-AzVM** startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e4298-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e4298-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4298-111">EXAMPLES</span></span>

### <span data-ttu-id="e4298-112">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e4298-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e4298-113">Det här kommandot startar om den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4298-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e4298-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4298-114">PARAMETERS</span></span>

### <span data-ttu-id="e4298-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4298-115">-AsJob</span></span>
<span data-ttu-id="e4298-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="e4298-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e4298-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4298-117">-DefaultProfile</span></span>
<span data-ttu-id="e4298-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4298-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4298-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e4298-119">-Id</span></span>
<span data-ttu-id="e4298-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e4298-120">The resource group name.</span></span>

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

### <span data-ttu-id="e4298-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4298-121">-Name</span></span>
<span data-ttu-id="e4298-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="e4298-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="e4298-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e4298-123">-PerformMaintenance</span></span>
<span data-ttu-id="e4298-124">För att utföra underhåll av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e4298-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="e4298-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4298-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4298-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e4298-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e4298-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4298-127">-Confirm</span></span>
<span data-ttu-id="e4298-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4298-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4298-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4298-129">-WhatIf</span></span>
<span data-ttu-id="e4298-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4298-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4298-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4298-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4298-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4298-132">CommonParameters</span></span>
<span data-ttu-id="e4298-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4298-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4298-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4298-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4298-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4298-135">INPUTS</span></span>

### <span data-ttu-id="e4298-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4298-136">None</span></span>
<span data-ttu-id="e4298-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e4298-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4298-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4298-138">OUTPUTS</span></span>

### <span data-ttu-id="e4298-139">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e4298-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e4298-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4298-140">NOTES</span></span>

## <span data-ttu-id="e4298-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4298-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4298-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e4298-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e4298-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e4298-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e4298-146">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e4298-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4298-147">Update-AzVM</span></span>](./Update-AzVM.md)


