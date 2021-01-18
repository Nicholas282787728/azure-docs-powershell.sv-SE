---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524437"
---
# <span data-ttu-id="5a997-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a997-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="5a997-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a997-102">SYNOPSIS</span></span>
<span data-ttu-id="5a997-103">Denna cmdlet startar en rullande uppgradering för alla tillägg på den angivna virtuella datorns skala till den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="5a997-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="5a997-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a997-104">SYNTAX</span></span>

### <span data-ttu-id="5a997-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="5a997-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a997-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a997-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a997-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a997-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a997-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a997-108">DESCRIPTION</span></span>
<span data-ttu-id="5a997-109">Startar en rullande uppgradering för att flytta alla tillägg på den här skalan för den virtuella datorn till den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="5a997-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="5a997-110">Tillägg som redan kör den senaste versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="5a997-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="5a997-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a997-111">EXAMPLES</span></span>

### <span data-ttu-id="5a997-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a997-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="5a997-113">I det här exemplet får du den befintliga virtuella dator skalan "MyVmssName" och lägger till en anknytning till den.</span><span class="sxs-lookup"><span data-stu-id="5a997-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="5a997-114">Det sista kommandot kör den rullande uppgraderings processen för fil tillägget.</span><span class="sxs-lookup"><span data-stu-id="5a997-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="5a997-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a997-115">PARAMETERS</span></span>

### <span data-ttu-id="5a997-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a997-116">-AsJob</span></span>
<span data-ttu-id="5a997-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5a997-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a997-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a997-118">-DefaultProfile</span></span>
<span data-ttu-id="5a997-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a997-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a997-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a997-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a997-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a997-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a997-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a997-122">-ResourceId</span></span>
<span data-ttu-id="5a997-123">Resurs-ID för den virtuella datorns skalnings objekt.</span><span class="sxs-lookup"><span data-stu-id="5a997-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a997-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a997-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5a997-125">Objekt för skalförändrad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5a997-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a997-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5a997-126">-VMScaleSetName</span></span>
<span data-ttu-id="5a997-127">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="5a997-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a997-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a997-128">-Confirm</span></span>
<span data-ttu-id="5a997-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a997-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a997-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a997-130">-WhatIf</span></span>
<span data-ttu-id="5a997-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a997-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a997-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a997-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a997-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a997-133">CommonParameters</span></span>
<span data-ttu-id="5a997-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a997-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a997-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a997-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a997-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a997-136">INPUTS</span></span>

### <span data-ttu-id="5a997-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5a997-137">System.String</span></span>

### <span data-ttu-id="5a997-138">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a997-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5a997-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a997-139">OUTPUTS</span></span>

### <span data-ttu-id="5a997-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5a997-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5a997-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a997-141">NOTES</span></span>

## <span data-ttu-id="5a997-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a997-142">RELATED LINKS</span></span>
