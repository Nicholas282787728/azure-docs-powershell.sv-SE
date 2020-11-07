---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
ms.openlocfilehash: 7f1cd0680d42ab83ec797b675e4505515a90548e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931477"
---
# <span data-ttu-id="1ec8c-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="1ec8c-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="1ec8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ec8c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec8c-103">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ec8c-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ec8c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec8c-106">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="1ec8c-107">Instanser som redan kör den senaste tillgängliga OS-versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="1ec8c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ec8c-108">EXAMPLES</span></span>

### <span data-ttu-id="1ec8c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ec8c-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="1ec8c-110">Det här kommandot startar en rullande uppgradering av alla virtuella dator instanser av VM-skalan "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="1ec8c-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="1ec8c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ec8c-111">PARAMETERS</span></span>

### <span data-ttu-id="1ec8c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec8c-112">-AsJob</span></span>
<span data-ttu-id="1ec8c-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1ec8c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ec8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec8c-114">-DefaultProfile</span></span>
<span data-ttu-id="1ec8c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec8c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec8c-116">-ResourceGroupName</span></span>
<span data-ttu-id="1ec8c-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ec8c-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1ec8c-118">-VMScaleSetName</span></span>
<span data-ttu-id="1ec8c-119">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="1ec8c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ec8c-120">-Confirm</span></span>
<span data-ttu-id="1ec8c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec8c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec8c-122">-WhatIf</span></span>
<span data-ttu-id="1ec8c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec8c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec8c-125">CommonParameters</span></span>
<span data-ttu-id="1ec8c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec8c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec8c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec8c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ec8c-128">INPUTS</span></span>

### <span data-ttu-id="1ec8c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1ec8c-129">System.String</span></span>

## <span data-ttu-id="1ec8c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ec8c-130">OUTPUTS</span></span>

### <span data-ttu-id="1ec8c-131">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1ec8c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1ec8c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ec8c-132">NOTES</span></span>

## <span data-ttu-id="1ec8c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ec8c-133">RELATED LINKS</span></span>

