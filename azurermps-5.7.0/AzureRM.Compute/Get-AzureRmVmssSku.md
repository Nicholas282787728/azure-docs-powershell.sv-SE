---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574357"
---
# <span data-ttu-id="bbe5d-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="bbe5d-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="bbe5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbe5d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe5d-103">Hämtar de tillgängliga SKU: erna för VMSS.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbe5d-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="bbe5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbe5d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe5d-106">Cmdleten **Get-AzureRmVmssSku** hämtar tillgängliga SKU: er för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bbe5d-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bbe5d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbe5d-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe5d-108">Exempel 1: Hämta alla tillgängliga SKU från VMSS</span><span class="sxs-lookup"><span data-stu-id="bbe5d-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="bbe5d-109">Det här kommandot får alla tillgängliga SKU: er från VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="bbe5d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbe5d-110">PARAMETERS</span></span>

### <span data-ttu-id="bbe5d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe5d-111">-ResourceGroupName</span></span>
<span data-ttu-id="bbe5d-112">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-112">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bbe5d-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bbe5d-113">-VMScaleSetName</span></span>
<span data-ttu-id="bbe5d-114">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-114">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="bbe5d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe5d-115">CommonParameters</span></span>
<span data-ttu-id="bbe5d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe5d-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe5d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe5d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbe5d-118">INPUTS</span></span>

### <span data-ttu-id="bbe5d-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="bbe5d-119">None</span></span>
<span data-ttu-id="bbe5d-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbe5d-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbe5d-121">OUTPUTS</span></span>

### <span data-ttu-id="bbe5d-122">Denna cmdlet ger ingen utmatning.</span><span class="sxs-lookup"><span data-stu-id="bbe5d-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="bbe5d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbe5d-123">NOTES</span></span>

## <span data-ttu-id="bbe5d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbe5d-124">RELATED LINKS</span></span>

[<span data-ttu-id="bbe5d-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bbe5d-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


