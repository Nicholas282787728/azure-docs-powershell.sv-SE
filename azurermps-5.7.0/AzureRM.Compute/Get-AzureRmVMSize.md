---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578303"
---
# <span data-ttu-id="f1efa-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="f1efa-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="f1efa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1efa-102">SYNOPSIS</span></span>
<span data-ttu-id="f1efa-103">Hämtar tillgängliga storlekar på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f1efa-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1efa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1efa-104">SYNTAX</span></span>

### <span data-ttu-id="f1efa-105">ListVirtualMachineSizeParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1efa-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="f1efa-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f1efa-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="f1efa-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1efa-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="f1efa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1efa-108">DESCRIPTION</span></span>
<span data-ttu-id="f1efa-109">Cmdleten **Get-AzureRmVMSize** hämtar tillgängliga storlekar på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="f1efa-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="f1efa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1efa-110">EXAMPLES</span></span>

### <span data-ttu-id="f1efa-111">Exempel 1: Hämta storlekar på en virtuell dator för en plats</span><span class="sxs-lookup"><span data-stu-id="f1efa-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="f1efa-112">Det här kommandot får de tillgängliga storlekarna för virtuella datorer på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="f1efa-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="f1efa-113">Exempel 2: Hämta storlekar för en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="f1efa-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="f1efa-114">Det här kommandot får tillgängliga storlekar för virtuella datorer som du kan distribuera i tillgänglighets uppsättningen med namnet AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="f1efa-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="f1efa-115">Exempel 3: skapa storlekar för en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f1efa-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="f1efa-116">Det här kommandot får tillgängliga storlekar för den befintliga virtuella datorn med namnet VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="f1efa-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="f1efa-117">Du kan ändra storlek på den virtuella datorn till de storlekar det här kommandot får.</span><span class="sxs-lookup"><span data-stu-id="f1efa-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="f1efa-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1efa-118">PARAMETERS</span></span>

### <span data-ttu-id="f1efa-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="f1efa-119">-AvailabilitySetName</span></span>
<span data-ttu-id="f1efa-120">Anger namnet på den tillgänglighets uppsättning för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="f1efa-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efa-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="f1efa-121">-Location</span></span>
<span data-ttu-id="f1efa-122">Anger platsen för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="f1efa-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1efa-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1efa-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f1efa-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efa-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f1efa-125">-VMName</span></span>
<span data-ttu-id="f1efa-126">Anger namnet på den virtuella dator där den här cmdleten får de tillgängliga storlekarna för storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="f1efa-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1efa-127">CommonParameters</span></span>
<span data-ttu-id="f1efa-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1efa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1efa-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1efa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1efa-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1efa-130">INPUTS</span></span>

### <span data-ttu-id="f1efa-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="f1efa-131">None</span></span>
<span data-ttu-id="f1efa-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f1efa-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1efa-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1efa-133">OUTPUTS</span></span>

## <span data-ttu-id="f1efa-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1efa-134">NOTES</span></span>

## <span data-ttu-id="f1efa-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1efa-135">RELATED LINKS</span></span>

[<span data-ttu-id="f1efa-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f1efa-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


