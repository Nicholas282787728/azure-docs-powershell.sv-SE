---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929946"
---
# <span data-ttu-id="d64dc-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="d64dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d64dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d64dc-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64dc-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d64dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d64dc-104">SYNTAX</span></span>

### <span data-ttu-id="d64dc-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="d64dc-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64dc-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d64dc-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d64dc-107">DESCRIPTION</span></span>
<span data-ttu-id="d64dc-108">Cmdleten **set-AzureRmVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d64dc-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d64dc-109">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="d64dc-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="d64dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d64dc-110">EXAMPLES</span></span>

### <span data-ttu-id="d64dc-111">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="d64dc-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d64dc-112">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="d64dc-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d64dc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d64dc-113">PARAMETERS</span></span>

### <span data-ttu-id="d64dc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d64dc-114">-AsJob</span></span>
<span data-ttu-id="d64dc-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d64dc-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d64dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64dc-116">-DefaultProfile</span></span>
<span data-ttu-id="d64dc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d64dc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64dc-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d64dc-118">-InstanceId</span></span>
<span data-ttu-id="d64dc-119">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d64dc-119">The instance ID of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d64dc-120">-Ombild</span><span class="sxs-lookup"><span data-stu-id="d64dc-120">-Reimage</span></span>
<span data-ttu-id="d64dc-121">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64dc-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64dc-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="d64dc-122">-ReimageAll</span></span>
<span data-ttu-id="d64dc-123">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64dc-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="d64dc-125">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d64dc-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d64dc-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d64dc-126">-VMScaleSetName</span></span>
<span data-ttu-id="d64dc-127">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="d64dc-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d64dc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d64dc-128">-Confirm</span></span>
<span data-ttu-id="d64dc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d64dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64dc-130">-WhatIf</span></span>
<span data-ttu-id="d64dc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d64dc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d64dc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d64dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64dc-133">CommonParameters</span></span>
<span data-ttu-id="d64dc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64dc-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64dc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64dc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d64dc-136">INPUTS</span></span>

### <span data-ttu-id="d64dc-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="d64dc-137">None</span></span>
<span data-ttu-id="d64dc-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d64dc-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d64dc-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d64dc-139">OUTPUTS</span></span>

### <span data-ttu-id="d64dc-140">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d64dc-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d64dc-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d64dc-141">NOTES</span></span>

## <span data-ttu-id="d64dc-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d64dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="d64dc-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d64dc-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d64dc-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d64dc-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d64dc-147">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d64dc-148">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="d64dc-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d64dc-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


