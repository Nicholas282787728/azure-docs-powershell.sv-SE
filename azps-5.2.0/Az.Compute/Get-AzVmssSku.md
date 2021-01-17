---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415875"
---
# <span data-ttu-id="1842c-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="1842c-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="1842c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1842c-102">SYNOPSIS</span></span>
<span data-ttu-id="1842c-103">Hämtar de tillgängliga SKU: erna för VMSS.</span><span class="sxs-lookup"><span data-stu-id="1842c-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="1842c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1842c-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1842c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1842c-105">DESCRIPTION</span></span>
<span data-ttu-id="1842c-106">Cmdleten **Get-AzVmssSku** hämtar tillgängliga SKU: er för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1842c-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1842c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1842c-107">EXAMPLES</span></span>

### <span data-ttu-id="1842c-108">Exempel 1: Hämta alla tillgängliga SKU från VMSS</span><span class="sxs-lookup"><span data-stu-id="1842c-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="1842c-109">Det här kommandot får alla tillgängliga SKU: er från VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="1842c-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="1842c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1842c-110">PARAMETERS</span></span>

### <span data-ttu-id="1842c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1842c-111">-DefaultProfile</span></span>
<span data-ttu-id="1842c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1842c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1842c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1842c-113">-ResourceGroupName</span></span>
<span data-ttu-id="1842c-114">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="1842c-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="1842c-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1842c-115">-VMScaleSetName</span></span>
<span data-ttu-id="1842c-116">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="1842c-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="1842c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1842c-117">CommonParameters</span></span>
<span data-ttu-id="1842c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1842c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1842c-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1842c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1842c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1842c-120">INPUTS</span></span>

### <span data-ttu-id="1842c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1842c-121">System.String</span></span>

## <span data-ttu-id="1842c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1842c-122">OUTPUTS</span></span>

### <span data-ttu-id="1842c-123">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="1842c-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="1842c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1842c-124">NOTES</span></span>

## <span data-ttu-id="1842c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1842c-125">RELATED LINKS</span></span>

[<span data-ttu-id="1842c-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1842c-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


