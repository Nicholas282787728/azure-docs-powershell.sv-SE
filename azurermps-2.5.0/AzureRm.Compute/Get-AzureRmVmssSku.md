---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930353"
---
# <span data-ttu-id="d4ff8-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="d4ff8-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="d4ff8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ff8-103">Hämtar de tillgängliga SKU: erna för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4ff8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4ff8-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4ff8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ff8-106">Cmdleten **Get-AzureRmVmssSku** hämtar tillgängliga SKU: er för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d4ff8-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d4ff8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="d4ff8-108">Exempel 1: Hämta alla tillgängliga SKU från VMSS</span><span class="sxs-lookup"><span data-stu-id="d4ff8-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d4ff8-109">Det här kommandot får alla tillgängliga SKU: er från VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d4ff8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="d4ff8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ff8-111">-DefaultProfile</span></span>
<span data-ttu-id="d4ff8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ff8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ff8-113">-ResourceGroupName</span></span>
<span data-ttu-id="d4ff8-114">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d4ff8-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4ff8-115">-VMScaleSetName</span></span>
<span data-ttu-id="d4ff8-116">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="d4ff8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ff8-117">CommonParameters</span></span>
<span data-ttu-id="d4ff8-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ff8-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ff8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ff8-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4ff8-120">INPUTS</span></span>

### <span data-ttu-id="d4ff8-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d4ff8-121">None</span></span>
<span data-ttu-id="d4ff8-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4ff8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4ff8-123">OUTPUTS</span></span>

### <span data-ttu-id="d4ff8-124">Denna cmdlet ger ingen utmatning.</span><span class="sxs-lookup"><span data-stu-id="d4ff8-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="d4ff8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4ff8-125">NOTES</span></span>

## <span data-ttu-id="d4ff8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4ff8-126">RELATED LINKS</span></span>

[<span data-ttu-id="d4ff8-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4ff8-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


