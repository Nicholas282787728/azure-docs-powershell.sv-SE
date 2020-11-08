---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092330"
---
# <span data-ttu-id="0a3a1-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0a3a1-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="0a3a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3a1-103">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="0a3a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a3a1-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a3a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="0a3a1-106">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="0a3a1-107">Instanser som redan kör den senaste tillgängliga OS-versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="0a3a1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a3a1-108">EXAMPLES</span></span>

### <span data-ttu-id="0a3a1-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a3a1-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0a3a1-110">Det här kommandot startar en rullande uppgradering av alla virtuella dator instanser av VM-skalan "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="0a3a1-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="0a3a1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a3a1-111">PARAMETERS</span></span>

### <span data-ttu-id="0a3a1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a3a1-112">-AsJob</span></span>
<span data-ttu-id="0a3a1-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0a3a1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a3a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a3a1-114">-DefaultProfile</span></span>
<span data-ttu-id="0a3a1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a3a1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a3a1-116">-ResourceGroupName</span></span>
<span data-ttu-id="0a3a1-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a3a1-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0a3a1-118">-VMScaleSetName</span></span>
<span data-ttu-id="0a3a1-119">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="0a3a1-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a3a1-120">-Confirm</span></span>
<span data-ttu-id="0a3a1-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a3a1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a3a1-122">-WhatIf</span></span>
<span data-ttu-id="0a3a1-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a3a1-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a3a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3a1-125">CommonParameters</span></span>
<span data-ttu-id="0a3a1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a3a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3a1-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a3a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3a1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a3a1-128">INPUTS</span></span>

### <span data-ttu-id="0a3a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0a3a1-129">System.String</span></span>

## <span data-ttu-id="0a3a1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a3a1-130">OUTPUTS</span></span>

### <span data-ttu-id="0a3a1-131">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0a3a1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0a3a1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a3a1-132">NOTES</span></span>

## <span data-ttu-id="0a3a1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a3a1-133">RELATED LINKS</span></span>