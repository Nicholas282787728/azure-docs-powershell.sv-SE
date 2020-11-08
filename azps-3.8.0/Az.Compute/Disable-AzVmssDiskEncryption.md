---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 14f29bb7097f584c89fa1bf92bf816cf4ca3d511
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092378"
---
# <span data-ttu-id="2a154-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2a154-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="2a154-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a154-102">SYNOPSIS</span></span>
<span data-ttu-id="2a154-103">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="2a154-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="2a154-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a154-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a154-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a154-105">DESCRIPTION</span></span>
<span data-ttu-id="2a154-106">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="2a154-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="2a154-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a154-107">EXAMPLES</span></span>

### <span data-ttu-id="2a154-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a154-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="2a154-109">Inaktiverar disk kryptering på den virtuella datorns skal uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="2a154-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="2a154-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a154-110">PARAMETERS</span></span>

### <span data-ttu-id="2a154-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a154-111">-AsJob</span></span>
<span data-ttu-id="2a154-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2a154-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a154-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a154-113">-DefaultProfile</span></span>
<span data-ttu-id="2a154-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a154-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a154-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="2a154-115">-ExtensionName</span></span>
<span data-ttu-id="2a154-116">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="2a154-116">The extension name.</span></span>
<span data-ttu-id="2a154-117">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2a154-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a154-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2a154-118">-Force</span></span>
<span data-ttu-id="2a154-119">För att framtvinga borttagning av tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2a154-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="2a154-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2a154-120">-ForceUpdate</span></span>
<span data-ttu-id="2a154-121">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="2a154-121">Generate a tag for force update.</span></span>  <span data-ttu-id="2a154-122">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="2a154-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a154-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a154-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a154-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2a154-124">The resource group name.</span></span>

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

### <span data-ttu-id="2a154-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a154-125">-VMScaleSetName</span></span>
<span data-ttu-id="2a154-126">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="2a154-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="2a154-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="2a154-127">-VolumeType</span></span>
<span data-ttu-id="2a154-128">Typ av volym (OS eller data) för att utföra krypterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="2a154-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a154-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a154-129">-Confirm</span></span>
<span data-ttu-id="2a154-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a154-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a154-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a154-131">-WhatIf</span></span>
<span data-ttu-id="2a154-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a154-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a154-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a154-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a154-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a154-134">CommonParameters</span></span>
<span data-ttu-id="2a154-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a154-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a154-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a154-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a154-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a154-137">INPUTS</span></span>

### <span data-ttu-id="2a154-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2a154-138">System.String</span></span>

### <span data-ttu-id="2a154-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a154-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a154-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a154-140">OUTPUTS</span></span>

### <span data-ttu-id="2a154-141">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a154-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2a154-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a154-142">NOTES</span></span>

## <span data-ttu-id="2a154-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a154-143">RELATED LINKS</span></span>
