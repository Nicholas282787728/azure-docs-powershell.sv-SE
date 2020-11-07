---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930745"
---
# <span data-ttu-id="ddf3d-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ddf3d-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="ddf3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddf3d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf3d-103">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddf3d-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddf3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddf3d-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf3d-106">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="ddf3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddf3d-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf3d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddf3d-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ddf3d-109">Inaktiverar disk kryptering på den virtuella datorns skal uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="ddf3d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddf3d-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf3d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddf3d-111">-AsJob</span></span>
<span data-ttu-id="ddf3d-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ddf3d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddf3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf3d-113">-DefaultProfile</span></span>
<span data-ttu-id="ddf3d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddf3d-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ddf3d-115">-ExtensionName</span></span>
<span data-ttu-id="ddf3d-116">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-116">The extension name.</span></span>
<span data-ttu-id="ddf3d-117">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf3d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ddf3d-118">-Force</span></span>
<span data-ttu-id="ddf3d-119">För att framtvinga borttagning av tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="ddf3d-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="ddf3d-120">-ForceUpdate</span></span>
<span data-ttu-id="ddf3d-121">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-121">Generate a tag for force update.</span></span>  <span data-ttu-id="ddf3d-122">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddf3d-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf3d-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddf3d-125">-VMScaleSetName</span></span>
<span data-ttu-id="ddf3d-126">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf3d-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="ddf3d-127">-VolumeType</span></span>
<span data-ttu-id="ddf3d-128">Typ av volym (OS eller data) för att utföra krypterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="ddf3d-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf3d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddf3d-129">-Confirm</span></span>
<span data-ttu-id="ddf3d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf3d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf3d-131">-WhatIf</span></span>
<span data-ttu-id="ddf3d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf3d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf3d-134">CommonParameters</span></span>
<span data-ttu-id="ddf3d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf3d-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf3d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf3d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddf3d-137">INPUTS</span></span>

### <span data-ttu-id="ddf3d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf3d-138">System.String</span></span>

## <span data-ttu-id="ddf3d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddf3d-139">OUTPUTS</span></span>

### <span data-ttu-id="ddf3d-140">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddf3d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddf3d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddf3d-141">NOTES</span></span>

## <span data-ttu-id="ddf3d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddf3d-142">RELATED LINKS</span></span>

