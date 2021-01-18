---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524433"
---
# <span data-ttu-id="07fe5-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="07fe5-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="07fe5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="07fe5-103">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="07fe5-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="07fe5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07fe5-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07fe5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="07fe5-106">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="07fe5-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="07fe5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="07fe5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07fe5-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="07fe5-109">Det här kommandot avbryter pågående rullande uppgradering av VM-Scale set "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="07fe5-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="07fe5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07fe5-110">PARAMETERS</span></span>

### <span data-ttu-id="07fe5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07fe5-111">-AsJob</span></span>
<span data-ttu-id="07fe5-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="07fe5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07fe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fe5-113">-DefaultProfile</span></span>
<span data-ttu-id="07fe5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07fe5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07fe5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="07fe5-115">-Force</span></span>
<span data-ttu-id="07fe5-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="07fe5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07fe5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fe5-117">-ResourceGroupName</span></span>
<span data-ttu-id="07fe5-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="07fe5-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="07fe5-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07fe5-119">-VMScaleSetName</span></span>
<span data-ttu-id="07fe5-120">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="07fe5-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="07fe5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07fe5-121">-Confirm</span></span>
<span data-ttu-id="07fe5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07fe5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07fe5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07fe5-123">-WhatIf</span></span>
<span data-ttu-id="07fe5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07fe5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07fe5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07fe5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07fe5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fe5-126">CommonParameters</span></span>
<span data-ttu-id="07fe5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fe5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fe5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07fe5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fe5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07fe5-129">INPUTS</span></span>

### <span data-ttu-id="07fe5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="07fe5-130">System.String</span></span>

## <span data-ttu-id="07fe5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07fe5-131">OUTPUTS</span></span>

### <span data-ttu-id="07fe5-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="07fe5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="07fe5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07fe5-133">NOTES</span></span>

## <span data-ttu-id="07fe5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07fe5-134">RELATED LINKS</span></span>
