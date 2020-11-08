---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088211"
---
# <span data-ttu-id="b8899-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b8899-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="b8899-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8899-102">SYNOPSIS</span></span>
<span data-ttu-id="b8899-103">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="b8899-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b8899-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8899-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8899-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8899-105">DESCRIPTION</span></span>
<span data-ttu-id="b8899-106">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="b8899-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b8899-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8899-107">EXAMPLES</span></span>

### <span data-ttu-id="b8899-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8899-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b8899-109">Det här kommandot visar status för den senaste rullande uppgraderingen för VMSS med VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="b8899-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b8899-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8899-110">PARAMETERS</span></span>

### <span data-ttu-id="b8899-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8899-111">-DefaultProfile</span></span>
<span data-ttu-id="b8899-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8899-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8899-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8899-113">-ResourceGroupName</span></span>
<span data-ttu-id="b8899-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b8899-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8899-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b8899-115">-VMScaleSetName</span></span>
<span data-ttu-id="b8899-116">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b8899-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="b8899-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8899-117">CommonParameters</span></span>
<span data-ttu-id="b8899-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8899-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8899-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8899-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8899-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8899-120">INPUTS</span></span>

### <span data-ttu-id="b8899-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b8899-121">System.String</span></span>

## <span data-ttu-id="b8899-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8899-122">OUTPUTS</span></span>

### <span data-ttu-id="b8899-123">Microsoft. Azure. commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="b8899-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="b8899-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8899-124">NOTES</span></span>

## <span data-ttu-id="b8899-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8899-125">RELATED LINKS</span></span>
