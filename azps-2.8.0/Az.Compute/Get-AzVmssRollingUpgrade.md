---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745136"
---
# <span data-ttu-id="b32fe-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b32fe-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="b32fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b32fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b32fe-103">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="b32fe-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b32fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b32fe-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b32fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b32fe-105">DESCRIPTION</span></span>
<span data-ttu-id="b32fe-106">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="b32fe-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b32fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b32fe-107">EXAMPLES</span></span>

### <span data-ttu-id="b32fe-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b32fe-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b32fe-109">Det här kommandot visar status för den senaste rullande uppgraderingen för VMSS med VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="b32fe-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b32fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b32fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b32fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32fe-111">-DefaultProfile</span></span>
<span data-ttu-id="b32fe-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b32fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32fe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32fe-113">-ResourceGroupName</span></span>
<span data-ttu-id="b32fe-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b32fe-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b32fe-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b32fe-115">-VMScaleSetName</span></span>
<span data-ttu-id="b32fe-116">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b32fe-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="b32fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32fe-117">CommonParameters</span></span>
<span data-ttu-id="b32fe-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32fe-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b32fe-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32fe-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b32fe-120">INPUTS</span></span>

### <span data-ttu-id="b32fe-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b32fe-121">System.String</span></span>

## <span data-ttu-id="b32fe-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b32fe-122">OUTPUTS</span></span>

### <span data-ttu-id="b32fe-123">Microsoft. Azure. commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="b32fe-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="b32fe-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b32fe-124">NOTES</span></span>

## <span data-ttu-id="b32fe-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b32fe-125">RELATED LINKS</span></span>
