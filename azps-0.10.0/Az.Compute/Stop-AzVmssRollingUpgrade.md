---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 915dd31b522fdbc7955494c0f76d69ee5a4b8376
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923033"
---
# <span data-ttu-id="3e0af-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3e0af-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="3e0af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e0af-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0af-103">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e0af-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3e0af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e0af-104">SYNTAX</span></span>

### <span data-ttu-id="3e0af-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="3e0af-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e0af-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3e0af-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e0af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e0af-107">DESCRIPTION</span></span>
<span data-ttu-id="3e0af-108">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e0af-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3e0af-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e0af-109">EXAMPLES</span></span>

### <span data-ttu-id="3e0af-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e0af-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3e0af-111">Det här kommandot avbryter pågående rullande uppgradering av VM-Scale set "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="3e0af-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3e0af-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e0af-112">PARAMETERS</span></span>

### <span data-ttu-id="3e0af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e0af-113">-AsJob</span></span>
<span data-ttu-id="3e0af-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e0af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e0af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0af-115">-DefaultProfile</span></span>
<span data-ttu-id="3e0af-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e0af-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3e0af-117">-Force</span></span>
<span data-ttu-id="3e0af-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3e0af-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e0af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0af-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e0af-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e0af-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0af-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3e0af-121">-VMScaleSetName</span></span>
<span data-ttu-id="3e0af-122">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3e0af-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0af-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e0af-123">-Confirm</span></span>
<span data-ttu-id="3e0af-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e0af-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e0af-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e0af-125">-WhatIf</span></span>
<span data-ttu-id="3e0af-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e0af-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e0af-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e0af-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e0af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0af-128">CommonParameters</span></span>
<span data-ttu-id="3e0af-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0af-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e0af-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0af-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e0af-131">INPUTS</span></span>

### <span data-ttu-id="3e0af-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3e0af-132">System.String</span></span>

## <span data-ttu-id="3e0af-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e0af-133">OUTPUTS</span></span>

### <span data-ttu-id="3e0af-134">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3e0af-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3e0af-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e0af-135">NOTES</span></span>

## <span data-ttu-id="3e0af-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e0af-136">RELATED LINKS</span></span>

