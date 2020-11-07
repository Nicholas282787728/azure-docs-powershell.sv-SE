---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 4c9281bc7eea4f8bf3b60d458f662ada19d97807
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929117"
---
# <span data-ttu-id="14709-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="14709-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="14709-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14709-102">SYNOPSIS</span></span>
<span data-ttu-id="14709-103">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="14709-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14709-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14709-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14709-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14709-105">DESCRIPTION</span></span>
<span data-ttu-id="14709-106">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="14709-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="14709-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14709-107">EXAMPLES</span></span>

### <span data-ttu-id="14709-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14709-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="14709-109">Det här kommandot visar status för den senaste rullande uppgraderingen för VMSS med VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="14709-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="14709-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14709-110">PARAMETERS</span></span>

### <span data-ttu-id="14709-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14709-111">-DefaultProfile</span></span>
<span data-ttu-id="14709-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14709-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14709-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14709-113">-ResourceGroupName</span></span>
<span data-ttu-id="14709-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="14709-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="14709-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="14709-115">-VMScaleSetName</span></span>
<span data-ttu-id="14709-116">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="14709-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="14709-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14709-117">CommonParameters</span></span>
<span data-ttu-id="14709-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14709-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14709-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14709-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14709-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14709-120">INPUTS</span></span>

### <span data-ttu-id="14709-121">System. String</span><span class="sxs-lookup"><span data-stu-id="14709-121">System.String</span></span>

## <span data-ttu-id="14709-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14709-122">OUTPUTS</span></span>

### <span data-ttu-id="14709-123">Microsoft. Azure. commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="14709-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="14709-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14709-124">NOTES</span></span>

## <span data-ttu-id="14709-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14709-125">RELATED LINKS</span></span>

