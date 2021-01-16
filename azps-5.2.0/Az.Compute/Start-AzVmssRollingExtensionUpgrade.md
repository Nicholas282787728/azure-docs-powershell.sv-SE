---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402616"
---
# <span data-ttu-id="f6ee1-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="f6ee1-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="f6ee1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ee1-103">Denna cmdlet startar en rullande uppgradering för alla tillägg på den angivna virtuella datorns skala till den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="f6ee1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6ee1-104">SYNTAX</span></span>

### <span data-ttu-id="f6ee1-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="f6ee1-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6ee1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6ee1-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6ee1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ee1-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ee1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="f6ee1-109">Startar en rullande uppgradering för att flytta alla tillägg på den här skalan för den virtuella datorn till den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="f6ee1-110">Tillägg som redan kör den senaste versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="f6ee1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6ee1-111">EXAMPLES</span></span>

### <span data-ttu-id="f6ee1-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6ee1-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="f6ee1-113">I det här exemplet får du den befintliga virtuella dator skalan "MyVmssName" och lägger till en anknytning till den.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="f6ee1-114">Det sista kommandot kör den rullande uppgraderings processen för fil tillägget.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="f6ee1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6ee1-115">PARAMETERS</span></span>

### <span data-ttu-id="f6ee1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6ee1-116">-AsJob</span></span>
<span data-ttu-id="f6ee1-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f6ee1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6ee1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ee1-118">-DefaultProfile</span></span>
<span data-ttu-id="f6ee1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6ee1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ee1-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6ee1-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6ee1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ee1-122">-ResourceId</span></span>
<span data-ttu-id="f6ee1-123">Resurs-ID för den virtuella datorns skalnings objekt.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="f6ee1-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f6ee1-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f6ee1-125">Objekt för skalförändrad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="f6ee1-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f6ee1-126">-VMScaleSetName</span></span>
<span data-ttu-id="f6ee1-127">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="f6ee1-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6ee1-128">-Confirm</span></span>
<span data-ttu-id="f6ee1-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ee1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ee1-130">-WhatIf</span></span>
<span data-ttu-id="f6ee1-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ee1-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ee1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ee1-133">CommonParameters</span></span>
<span data-ttu-id="f6ee1-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ee1-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6ee1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ee1-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6ee1-136">INPUTS</span></span>

### <span data-ttu-id="f6ee1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ee1-137">System.String</span></span>

### <span data-ttu-id="f6ee1-138">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f6ee1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f6ee1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6ee1-139">OUTPUTS</span></span>

### <span data-ttu-id="f6ee1-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f6ee1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f6ee1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6ee1-141">NOTES</span></span>

## <span data-ttu-id="f6ee1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6ee1-142">RELATED LINKS</span></span>
