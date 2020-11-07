---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 239397bc91e42c55d400caf00a83619c4665bbce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757113"
---
# <span data-ttu-id="3557d-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3557d-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="3557d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3557d-102">SYNOPSIS</span></span>
<span data-ttu-id="3557d-103">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="3557d-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3557d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3557d-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3557d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3557d-105">DESCRIPTION</span></span>
<span data-ttu-id="3557d-106">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="3557d-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="3557d-107">Instanser som redan kör den senaste tillgängliga OS-versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="3557d-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="3557d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3557d-108">EXAMPLES</span></span>

### <span data-ttu-id="3557d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3557d-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3557d-110">Det här kommandot startar en rullande uppgradering av alla virtuella dator instanser av VM-skalan "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="3557d-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3557d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3557d-111">PARAMETERS</span></span>

### <span data-ttu-id="3557d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3557d-112">-AsJob</span></span>
<span data-ttu-id="3557d-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3557d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3557d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3557d-114">-DefaultProfile</span></span>
<span data-ttu-id="3557d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3557d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3557d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3557d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3557d-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3557d-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3557d-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3557d-118">-VMScaleSetName</span></span>
<span data-ttu-id="3557d-119">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3557d-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3557d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3557d-120">-Confirm</span></span>
<span data-ttu-id="3557d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3557d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3557d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3557d-122">-WhatIf</span></span>
<span data-ttu-id="3557d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3557d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3557d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3557d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3557d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3557d-125">CommonParameters</span></span>
<span data-ttu-id="3557d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3557d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3557d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3557d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3557d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3557d-128">INPUTS</span></span>

### <span data-ttu-id="3557d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3557d-129">System.String</span></span>

## <span data-ttu-id="3557d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3557d-130">OUTPUTS</span></span>

### <span data-ttu-id="3557d-131">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3557d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3557d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3557d-132">NOTES</span></span>

## <span data-ttu-id="3557d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3557d-133">RELATED LINKS</span></span>
