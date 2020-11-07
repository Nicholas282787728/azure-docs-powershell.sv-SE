---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925130"
---
# <span data-ttu-id="d7f1b-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="d7f1b-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="d7f1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f1b-103">Hämtar de tillgängliga SKU: erna för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="d7f1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7f1b-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f1b-106">Cmdleten **Get-AzVmssSku** hämtar tillgängliga SKU: er för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d7f1b-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d7f1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f1b-108">Exempel 1: Hämta alla tillgängliga SKU från VMSS</span><span class="sxs-lookup"><span data-stu-id="d7f1b-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d7f1b-109">Det här kommandot får alla tillgängliga SKU: er från VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d7f1b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7f1b-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f1b-111">-DefaultProfile</span></span>
<span data-ttu-id="d7f1b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7f1b-114">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d7f1b-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d7f1b-115">-VMScaleSetName</span></span>
<span data-ttu-id="d7f1b-116">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="d7f1b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f1b-117">CommonParameters</span></span>
<span data-ttu-id="d7f1b-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f1b-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f1b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f1b-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7f1b-120">INPUTS</span></span>

### <span data-ttu-id="d7f1b-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7f1b-121">None</span></span>
<span data-ttu-id="d7f1b-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7f1b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7f1b-123">OUTPUTS</span></span>

### <span data-ttu-id="d7f1b-124">Denna cmdlet ger ingen utmatning.</span><span class="sxs-lookup"><span data-stu-id="d7f1b-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="d7f1b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7f1b-125">NOTES</span></span>

## <span data-ttu-id="d7f1b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7f1b-126">RELATED LINKS</span></span>

[<span data-ttu-id="d7f1b-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7f1b-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


