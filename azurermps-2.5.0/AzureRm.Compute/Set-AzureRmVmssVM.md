---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931474"
---
# <span data-ttu-id="76ae0-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="76ae0-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="76ae0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="76ae0-103">Ändrar tillstånd för en VMSS-instans.</span><span class="sxs-lookup"><span data-stu-id="76ae0-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76ae0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76ae0-104">SYNTAX</span></span>

### <span data-ttu-id="76ae0-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="76ae0-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76ae0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="76ae0-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76ae0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76ae0-107">DESCRIPTION</span></span>
<span data-ttu-id="76ae0-108">Cmdleten **set-AzureRmVmssVM** ändrar tillståndet för en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="76ae0-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="76ae0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76ae0-109">EXAMPLES</span></span>

## <span data-ttu-id="76ae0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76ae0-110">PARAMETERS</span></span>

### <span data-ttu-id="76ae0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76ae0-111">-AsJob</span></span>
<span data-ttu-id="76ae0-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="76ae0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76ae0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ae0-113">-DefaultProfile</span></span>
<span data-ttu-id="76ae0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76ae0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ae0-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="76ae0-115">-InstanceId</span></span>
<span data-ttu-id="76ae0-116">Anger ID för den VMSS-instans som denna cmdlet ändrar tillstånd för.</span><span class="sxs-lookup"><span data-stu-id="76ae0-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ae0-117">-Ombild</span><span class="sxs-lookup"><span data-stu-id="76ae0-117">-Reimage</span></span>
<span data-ttu-id="76ae0-118">Anger att denna cmdlet ombildar VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="76ae0-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="76ae0-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="76ae0-119">-ReimageAll</span></span>
<span data-ttu-id="76ae0-120">Anger att cmdleten återavbildningar alla diskar i VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="76ae0-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="76ae0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ae0-121">-ResourceGroupName</span></span>
<span data-ttu-id="76ae0-122">Anger namnet på den resurs grupp som innehåller VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="76ae0-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="76ae0-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="76ae0-123">-VMScaleSetName</span></span>
<span data-ttu-id="76ae0-124">Anger namnet på den VMSS-instans som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="76ae0-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="76ae0-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76ae0-125">-Confirm</span></span>
<span data-ttu-id="76ae0-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76ae0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76ae0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76ae0-127">-WhatIf</span></span>
<span data-ttu-id="76ae0-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76ae0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76ae0-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76ae0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76ae0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ae0-130">CommonParameters</span></span>
<span data-ttu-id="76ae0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ae0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ae0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ae0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ae0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76ae0-133">INPUTS</span></span>

### <span data-ttu-id="76ae0-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="76ae0-134">None</span></span>
<span data-ttu-id="76ae0-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="76ae0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76ae0-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76ae0-136">OUTPUTS</span></span>

### <span data-ttu-id="76ae0-137">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="76ae0-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="76ae0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76ae0-138">NOTES</span></span>

## <span data-ttu-id="76ae0-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76ae0-139">RELATED LINKS</span></span>

[<span data-ttu-id="76ae0-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="76ae0-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
