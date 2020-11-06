---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 7ff2512fa7c6247d75eb8b288c888dc2aff670dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577259"
---
# <span data-ttu-id="a776c-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a776c-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="a776c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a776c-102">SYNOPSIS</span></span>
<span data-ttu-id="a776c-103">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="a776c-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a776c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a776c-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a776c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a776c-105">DESCRIPTION</span></span>
<span data-ttu-id="a776c-106">Inaktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="a776c-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="a776c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a776c-107">EXAMPLES</span></span>

### <span data-ttu-id="a776c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a776c-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a776c-109">Inaktiverar disk kryptering på den virtuella datorns skal uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="a776c-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a776c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a776c-110">PARAMETERS</span></span>

### <span data-ttu-id="a776c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a776c-111">-AsJob</span></span>
<span data-ttu-id="a776c-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a776c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a776c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a776c-113">-DefaultProfile</span></span>
<span data-ttu-id="a776c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a776c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a776c-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="a776c-115">-ExtensionName</span></span>
<span data-ttu-id="a776c-116">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="a776c-116">The extension name.</span></span>
<span data-ttu-id="a776c-117">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="a776c-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="a776c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a776c-118">-Force</span></span>
<span data-ttu-id="a776c-119">För att framtvinga borttagning av tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a776c-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="a776c-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="a776c-120">-ForceUpdate</span></span>
<span data-ttu-id="a776c-121">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="a776c-121">Generate a tag for force update.</span></span>  <span data-ttu-id="a776c-122">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="a776c-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="a776c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a776c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a776c-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a776c-124">The resource group name.</span></span>

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

### <span data-ttu-id="a776c-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a776c-125">-VMScaleSetName</span></span>
<span data-ttu-id="a776c-126">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="a776c-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="a776c-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a776c-127">-VolumeType</span></span>
<span data-ttu-id="a776c-128">Typ av volym (OS eller data) för att utföra krypterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="a776c-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="a776c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a776c-129">-Confirm</span></span>
<span data-ttu-id="a776c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a776c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a776c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a776c-131">-WhatIf</span></span>
<span data-ttu-id="a776c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a776c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a776c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a776c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a776c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a776c-134">CommonParameters</span></span>
<span data-ttu-id="a776c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a776c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a776c-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a776c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a776c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a776c-137">INPUTS</span></span>

### <span data-ttu-id="a776c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a776c-138">System.String</span></span>

## <span data-ttu-id="a776c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a776c-139">OUTPUTS</span></span>

### <span data-ttu-id="a776c-140">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a776c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a776c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a776c-141">NOTES</span></span>

## <span data-ttu-id="a776c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a776c-142">RELATED LINKS</span></span>
