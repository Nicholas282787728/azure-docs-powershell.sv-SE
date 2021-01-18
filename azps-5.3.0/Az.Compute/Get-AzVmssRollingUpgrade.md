---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526924"
---
# <span data-ttu-id="0aca1-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="0aca1-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="0aca1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0aca1-102">SYNOPSIS</span></span>
<span data-ttu-id="0aca1-103">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="0aca1-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="0aca1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0aca1-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aca1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0aca1-105">DESCRIPTION</span></span>
<span data-ttu-id="0aca1-106">Visar status för den senaste virtuella dator skalnings den rullande uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="0aca1-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="0aca1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0aca1-107">EXAMPLES</span></span>

### <span data-ttu-id="0aca1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0aca1-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0aca1-109">Det här kommandot visar status för den senaste rullande uppgraderingen för VMSS med VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="0aca1-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0aca1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0aca1-110">PARAMETERS</span></span>

### <span data-ttu-id="0aca1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aca1-111">-DefaultProfile</span></span>
<span data-ttu-id="0aca1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0aca1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aca1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aca1-113">-ResourceGroupName</span></span>
<span data-ttu-id="0aca1-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0aca1-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0aca1-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0aca1-115">-VMScaleSetName</span></span>
<span data-ttu-id="0aca1-116">Namnet på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0aca1-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="0aca1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aca1-117">CommonParameters</span></span>
<span data-ttu-id="0aca1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aca1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aca1-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0aca1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aca1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0aca1-120">INPUTS</span></span>

### <span data-ttu-id="0aca1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0aca1-121">System.String</span></span>

## <span data-ttu-id="0aca1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0aca1-122">OUTPUTS</span></span>

### <span data-ttu-id="0aca1-123">Microsoft. Azure. commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="0aca1-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="0aca1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0aca1-124">NOTES</span></span>

## <span data-ttu-id="0aca1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0aca1-125">RELATED LINKS</span></span>
