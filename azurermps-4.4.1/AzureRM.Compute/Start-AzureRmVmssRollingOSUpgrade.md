---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580664"
---
# <span data-ttu-id="3cbc7-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3cbc7-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="3cbc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbc7-103">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cbc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cbc7-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cbc7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cbc7-105">DESCRIPTION</span></span>
<span data-ttu-id="3cbc7-106">Startar en rullande uppgradering för att flytta alla instanser av virtuell dators skalnings uppsättning till den senaste tillgängliga Platform image OS-versionen.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="3cbc7-107">Instanser som redan kör den senaste tillgängliga OS-versionen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="3cbc7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cbc7-108">EXAMPLES</span></span>

### <span data-ttu-id="3cbc7-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cbc7-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3cbc7-110">Det här kommandot startar en rullande uppgradering av alla virtuella dator instanser av VM-skalan "VMSS001" i resurs gruppen "Group001".</span><span class="sxs-lookup"><span data-stu-id="3cbc7-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3cbc7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cbc7-111">PARAMETERS</span></span>

### <span data-ttu-id="3cbc7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbc7-112">-DefaultProfile</span></span>
<span data-ttu-id="3cbc7-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cbc7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbc7-114">-ResourceGroupName</span></span>
<span data-ttu-id="3cbc7-115">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cbc7-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3cbc7-116">-VMScaleSetName</span></span>
<span data-ttu-id="3cbc7-117">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-117">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="3cbc7-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cbc7-118">-Confirm</span></span>
<span data-ttu-id="3cbc7-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cbc7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cbc7-120">-WhatIf</span></span>
<span data-ttu-id="3cbc7-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cbc7-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cbc7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbc7-123">CommonParameters</span></span>
<span data-ttu-id="3cbc7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cbc7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbc7-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cbc7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbc7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cbc7-126">INPUTS</span></span>

### <span data-ttu-id="3cbc7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3cbc7-127">System.String</span></span>

## <span data-ttu-id="3cbc7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cbc7-128">OUTPUTS</span></span>

### <span data-ttu-id="3cbc7-129">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3cbc7-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3cbc7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cbc7-130">NOTES</span></span>

## <span data-ttu-id="3cbc7-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cbc7-131">RELATED LINKS</span></span>

