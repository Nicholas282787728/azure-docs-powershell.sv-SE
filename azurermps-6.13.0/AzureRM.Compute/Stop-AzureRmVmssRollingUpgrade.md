---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 92a3a98ba5e6743b5d52ad619501fd6ed56c10c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575259"
---
# <span data-ttu-id="3e1de-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3e1de-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="3e1de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e1de-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1de-103">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e1de-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e1de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e1de-104">SYNTAX</span></span>

### <span data-ttu-id="3e1de-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="3e1de-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1de-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3e1de-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e1de-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1de-108">Avbryter den befintliga rullande uppgraderingen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e1de-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3e1de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e1de-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1de-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e1de-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3e1de-111">Det här kommandot avbryter pågående rullande uppgradering av VM-Scale set "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="3e1de-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3e1de-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e1de-112">PARAMETERS</span></span>

### <span data-ttu-id="3e1de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e1de-113">-AsJob</span></span>
<span data-ttu-id="3e1de-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e1de-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e1de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1de-115">-DefaultProfile</span></span>
<span data-ttu-id="3e1de-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1de-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3e1de-117">-Force</span></span>
<span data-ttu-id="3e1de-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3e1de-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e1de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1de-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e1de-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e1de-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1de-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3e1de-121">-VMScaleSetName</span></span>
<span data-ttu-id="3e1de-122">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3e1de-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1de-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e1de-123">-Confirm</span></span>
<span data-ttu-id="3e1de-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e1de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1de-125">-WhatIf</span></span>
<span data-ttu-id="3e1de-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e1de-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1de-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e1de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1de-128">CommonParameters</span></span>
<span data-ttu-id="3e1de-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1de-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1de-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e1de-131">INPUTS</span></span>

### <span data-ttu-id="3e1de-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1de-132">System.String</span></span>

## <span data-ttu-id="3e1de-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e1de-133">OUTPUTS</span></span>

### <span data-ttu-id="3e1de-134">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3e1de-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3e1de-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e1de-135">NOTES</span></span>

## <span data-ttu-id="3e1de-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e1de-136">RELATED LINKS</span></span>
