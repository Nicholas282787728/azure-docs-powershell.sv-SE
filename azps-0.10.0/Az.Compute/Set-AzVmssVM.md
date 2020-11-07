---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923066"
---
# <span data-ttu-id="b5535-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="b5535-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="b5535-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5535-102">SYNOPSIS</span></span>
<span data-ttu-id="b5535-103">Ändrar tillstånd för en VMSS-instans.</span><span class="sxs-lookup"><span data-stu-id="b5535-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="b5535-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5535-104">SYNTAX</span></span>

### <span data-ttu-id="b5535-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="b5535-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5535-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b5535-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5535-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5535-107">DESCRIPTION</span></span>
<span data-ttu-id="b5535-108">Cmdleten **set-AzVmssVM** ändrar tillståndet för en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b5535-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b5535-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5535-109">EXAMPLES</span></span>

## <span data-ttu-id="b5535-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5535-110">PARAMETERS</span></span>

### <span data-ttu-id="b5535-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5535-111">-AsJob</span></span>
<span data-ttu-id="b5535-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b5535-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5535-113">-DefaultProfile</span></span>
<span data-ttu-id="b5535-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5535-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5535-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b5535-115">-InstanceId</span></span>
<span data-ttu-id="b5535-116">Anger ID för den VMSS-instans som denna cmdlet ändrar tillstånd för.</span><span class="sxs-lookup"><span data-stu-id="b5535-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="b5535-117">-Ombild</span><span class="sxs-lookup"><span data-stu-id="b5535-117">-Reimage</span></span>
<span data-ttu-id="b5535-118">Anger att denna cmdlet ombildar VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="b5535-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="b5535-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="b5535-119">-ReimageAll</span></span>
<span data-ttu-id="b5535-120">Anger att cmdleten återavbildningar alla diskar i VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="b5535-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="b5535-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5535-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5535-122">Anger namnet på den resurs grupp som innehåller VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="b5535-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="b5535-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b5535-123">-VMScaleSetName</span></span>
<span data-ttu-id="b5535-124">Anger namnet på den VMSS-instans som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b5535-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b5535-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5535-125">-Confirm</span></span>
<span data-ttu-id="b5535-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5535-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5535-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5535-127">-WhatIf</span></span>
<span data-ttu-id="b5535-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5535-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5535-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5535-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5535-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5535-130">CommonParameters</span></span>
<span data-ttu-id="b5535-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5535-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5535-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5535-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5535-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5535-133">INPUTS</span></span>

### <span data-ttu-id="b5535-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="b5535-134">None</span></span>
<span data-ttu-id="b5535-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b5535-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5535-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5535-136">OUTPUTS</span></span>

### <span data-ttu-id="b5535-137">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b5535-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b5535-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5535-138">NOTES</span></span>

## <span data-ttu-id="b5535-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5535-139">RELATED LINKS</span></span>

[<span data-ttu-id="b5535-140">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="b5535-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
