---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c906d7b0b10197e934ace7f9c913ee36e02be7ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582791"
---
# <span data-ttu-id="ddb0f-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="ddb0f-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="ddb0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb0f-103">Hämtar de tillgängliga SKU: erna för VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddb0f-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddb0f-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb0f-106">Cmdleten **Get-AzureRmVmssSku** hämtar tillgängliga SKU: er för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ddb0f-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ddb0f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddb0f-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb0f-108">Exempel 1: Hämta alla tillgängliga SKU från VMSS</span><span class="sxs-lookup"><span data-stu-id="ddb0f-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ddb0f-109">Det här kommandot får alla tillgängliga SKU: er från VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ddb0f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddb0f-110">PARAMETERS</span></span>

### <span data-ttu-id="ddb0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb0f-111">-DefaultProfile</span></span>
<span data-ttu-id="ddb0f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb0f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb0f-113">-ResourceGroupName</span></span>
<span data-ttu-id="ddb0f-114">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ddb0f-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddb0f-115">-VMScaleSetName</span></span>
<span data-ttu-id="ddb0f-116">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ddb0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb0f-117">CommonParameters</span></span>
<span data-ttu-id="ddb0f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb0f-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb0f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb0f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddb0f-120">INPUTS</span></span>

### <span data-ttu-id="ddb0f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb0f-121">System.String</span></span>

## <span data-ttu-id="ddb0f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddb0f-122">OUTPUTS</span></span>

### <span data-ttu-id="ddb0f-123">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="ddb0f-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="ddb0f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddb0f-124">NOTES</span></span>

## <span data-ttu-id="ddb0f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddb0f-125">RELATED LINKS</span></span>

[<span data-ttu-id="ddb0f-126">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddb0f-126">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


