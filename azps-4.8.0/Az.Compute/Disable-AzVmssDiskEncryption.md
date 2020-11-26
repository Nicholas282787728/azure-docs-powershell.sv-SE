---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 2cfdfdfdc662c59f4d9814a6b68d7577b486c550
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260613"
---
# <span data-ttu-id="30177-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="30177-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="30177-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30177-102">SYNOPSIS</span></span>
<span data-ttu-id="30177-103">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="30177-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="30177-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30177-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30177-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30177-105">DESCRIPTION</span></span>
<span data-ttu-id="30177-106">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="30177-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="30177-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30177-107">EXAMPLES</span></span>

### <span data-ttu-id="30177-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30177-108">Example 1</span></span>
```powershell
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="30177-109">Inaktiverar disk kryptering på den virtuella datorns skal uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="30177-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="30177-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30177-110">Example 2</span></span>

<span data-ttu-id="30177-111">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="30177-111">Disables disk encryption on a VM scale set.</span></span> <span data-ttu-id="30177-112">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="30177-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzVmssDiskEncryption -ResourceGroupName 'Group001' -VMScaleSetName 'VMSS001' -VolumeType OS
```

## <span data-ttu-id="30177-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30177-113">PARAMETERS</span></span>

### <span data-ttu-id="30177-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30177-114">-AsJob</span></span>
<span data-ttu-id="30177-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="30177-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30177-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30177-116">-DefaultProfile</span></span>
<span data-ttu-id="30177-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30177-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30177-118">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="30177-118">-ExtensionName</span></span>
<span data-ttu-id="30177-119">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="30177-119">The extension name.</span></span>
<span data-ttu-id="30177-120">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="30177-120">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="30177-121">-Force</span><span class="sxs-lookup"><span data-stu-id="30177-121">-Force</span></span>
<span data-ttu-id="30177-122">För att framtvinga borttagning av tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="30177-122">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="30177-123">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="30177-123">-ForceUpdate</span></span>
<span data-ttu-id="30177-124">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="30177-124">Generate a tag for force update.</span></span>  <span data-ttu-id="30177-125">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="30177-125">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="30177-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30177-126">-ResourceGroupName</span></span>
<span data-ttu-id="30177-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="30177-127">The resource group name.</span></span>

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

### <span data-ttu-id="30177-128">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="30177-128">-VMScaleSetName</span></span>
<span data-ttu-id="30177-129">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="30177-129">The virtual machine name.</span></span>

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

### <span data-ttu-id="30177-130">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="30177-130">-VolumeType</span></span>
<span data-ttu-id="30177-131">Typ av volym (OS eller data) för att utföra krypterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="30177-131">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="30177-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30177-132">-Confirm</span></span>
<span data-ttu-id="30177-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30177-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30177-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30177-134">-WhatIf</span></span>
<span data-ttu-id="30177-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30177-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30177-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30177-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30177-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30177-137">CommonParameters</span></span>
<span data-ttu-id="30177-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30177-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30177-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30177-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30177-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30177-140">INPUTS</span></span>

### <span data-ttu-id="30177-141">System. String</span><span class="sxs-lookup"><span data-stu-id="30177-141">System.String</span></span>

### <span data-ttu-id="30177-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30177-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30177-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30177-143">OUTPUTS</span></span>

### <span data-ttu-id="30177-144">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30177-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="30177-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30177-145">NOTES</span></span>

## <span data-ttu-id="30177-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30177-146">RELATED LINKS</span></span>