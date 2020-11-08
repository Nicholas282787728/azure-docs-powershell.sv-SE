---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089827"
---
# <span data-ttu-id="7d470-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="7d470-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="7d470-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d470-102">SYNOPSIS</span></span>
<span data-ttu-id="7d470-103">Manuell uppdatering av plattforms uppdateringar för att uppdatera virtuella datorer i en skala för virtuell dator med en tjänst infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="7d470-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="7d470-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d470-104">SYNTAX</span></span>

### <span data-ttu-id="7d470-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="7d470-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d470-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7d470-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d470-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7d470-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d470-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d470-108">DESCRIPTION</span></span>
<span data-ttu-id="7d470-109">Tvinga manuell plattforms uppdaterings domän att få uppdatera virtuella datorer i en skal uppsättning för en virtuell dator med en tjänst infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="7d470-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="7d470-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d470-110">EXAMPLES</span></span>

### <span data-ttu-id="7d470-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d470-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="7d470-112">Det här kommandot tvingar Service Fabric-uppdateringen att gå på UD 0 för den virtuella datorns skalnings uppsättning angiven med resurs gruppens namn och skal uppsättnings namn.</span><span class="sxs-lookup"><span data-stu-id="7d470-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="7d470-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7d470-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="7d470-114">Det här kommandot tvingar Service Fabric-uppdateringen att gå in på UD 1 för den virtuella datorns skal uppsättning som anges av objekt skalnings gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d470-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="7d470-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7d470-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="7d470-116">Det här kommandot tvingar Service Fabric-uppdateringen att gå på UD 2 för den virtuella datorns skalnings uppsättning enligt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7d470-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="7d470-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d470-117">PARAMETERS</span></span>

### <span data-ttu-id="7d470-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d470-118">-AsJob</span></span>
<span data-ttu-id="7d470-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7d470-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d470-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d470-120">-DefaultProfile</span></span>
<span data-ttu-id="7d470-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d470-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d470-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="7d470-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="7d470-123">Platform Update-domänen där en manuell återställning efter frågas.</span><span class="sxs-lookup"><span data-stu-id="7d470-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d470-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d470-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d470-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d470-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d470-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d470-126">-ResourceId</span></span>
<span data-ttu-id="7d470-127">Resurs-ID för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="7d470-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d470-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7d470-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7d470-129">Objekt med skal uppsättning för lokal virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7d470-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d470-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7d470-130">-VMScaleSetName</span></span>
<span data-ttu-id="7d470-131">Namnet på den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="7d470-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d470-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d470-132">-Confirm</span></span>
<span data-ttu-id="7d470-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d470-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d470-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d470-134">-WhatIf</span></span>
<span data-ttu-id="7d470-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d470-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d470-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d470-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d470-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d470-137">CommonParameters</span></span>
<span data-ttu-id="7d470-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d470-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d470-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d470-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d470-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d470-140">INPUTS</span></span>

### <span data-ttu-id="7d470-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7d470-141">System.String</span></span>

### <span data-ttu-id="7d470-142">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7d470-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7d470-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d470-143">OUTPUTS</span></span>

### <span data-ttu-id="7d470-144">Microsoft. Azure. commands. Compute. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="7d470-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="7d470-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d470-145">NOTES</span></span>

## <span data-ttu-id="7d470-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d470-146">RELATED LINKS</span></span>
