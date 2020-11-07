---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917194"
---
# <span data-ttu-id="8fb9e-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8fb9e-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="8fb9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb9e-103">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="8fb9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fb9e-104">SYNTAX</span></span>

### <span data-ttu-id="8fb9e-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="8fb9e-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fb9e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8fb9e-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fb9e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fb9e-107">DESCRIPTION</span></span>
<span data-ttu-id="8fb9e-108">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="8fb9e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fb9e-109">EXAMPLES</span></span>

### <span data-ttu-id="8fb9e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8fb9e-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="8fb9e-111">Det här kommandot avbryter pågående rullande uppgradering av VM-Scale set "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="8fb9e-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="8fb9e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fb9e-112">PARAMETERS</span></span>

### <span data-ttu-id="8fb9e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fb9e-113">-AsJob</span></span>
<span data-ttu-id="8fb9e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8fb9e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fb9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb9e-115">-DefaultProfile</span></span>
<span data-ttu-id="8fb9e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fb9e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8fb9e-117">-Force</span></span>
<span data-ttu-id="8fb9e-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fb9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8fb9e-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8fb9e-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8fb9e-121">-VMScaleSetName</span></span>
<span data-ttu-id="8fb9e-122">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="8fb9e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fb9e-123">-Confirm</span></span>
<span data-ttu-id="8fb9e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fb9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fb9e-125">-WhatIf</span></span>
<span data-ttu-id="8fb9e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fb9e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fb9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb9e-128">CommonParameters</span></span>
<span data-ttu-id="8fb9e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb9e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb9e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb9e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fb9e-131">INPUTS</span></span>

### <span data-ttu-id="8fb9e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8fb9e-132">System.String</span></span>

## <span data-ttu-id="8fb9e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fb9e-133">OUTPUTS</span></span>

### <span data-ttu-id="8fb9e-134">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8fb9e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8fb9e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fb9e-135">NOTES</span></span>

## <span data-ttu-id="8fb9e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fb9e-136">RELATED LINKS</span></span>
