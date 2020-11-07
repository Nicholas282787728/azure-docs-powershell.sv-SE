---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755388"
---
# <span data-ttu-id="f2478-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="f2478-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="f2478-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2478-102">SYNOPSIS</span></span>
<span data-ttu-id="f2478-103">Ställer in information om Marketplace på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f2478-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2478-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2478-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2478-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2478-105">DESCRIPTION</span></span>
<span data-ttu-id="f2478-106">Cmdleten **set-AzureRmVMPlan** anger abonnemangs informationen för Azure Marketplace för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f2478-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="f2478-107">Innan du kan distribuera en Marketplace-avbildning via kommando raden måste program varan vara aktive rad eller den virtuella datorn måste distribueras med Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="f2478-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="f2478-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2478-108">EXAMPLES</span></span>

## <span data-ttu-id="f2478-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2478-109">PARAMETERS</span></span>

### <span data-ttu-id="f2478-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2478-110">-Name</span></span>
<span data-ttu-id="f2478-111">Anger namnet på bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f2478-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="f2478-112">Det här är samma värde som returneras av Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2478-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="f2478-113">Mer information om hur du hittar bild information finns i [navigera och välja bilder i Azure Virtual Machine med PowerShell och Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) i Microsoft Azure-dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="f2478-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="f2478-114">-Produkt</span><span class="sxs-lookup"><span data-stu-id="f2478-114">-Product</span></span>
<span data-ttu-id="f2478-115">Anger produkten av bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f2478-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="f2478-116">Det här är samma information **som värdet för** **imageReference** -elementet.</span><span class="sxs-lookup"><span data-stu-id="f2478-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2478-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="f2478-117">-PromotionCode</span></span>
<span data-ttu-id="f2478-118">Anger en kampanj kod.</span><span class="sxs-lookup"><span data-stu-id="f2478-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2478-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f2478-119">-Publisher</span></span>
<span data-ttu-id="f2478-120">Anger bildens utgivare.</span><span class="sxs-lookup"><span data-stu-id="f2478-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="f2478-121">Du kan hitta den här informationen genom att använda Get-AzureRmVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2478-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2478-122">-VM</span><span class="sxs-lookup"><span data-stu-id="f2478-122">-VM</span></span>
<span data-ttu-id="f2478-123">Anger det virtuella dator objekt för vilket du vill ange en Marketplace-plan.</span><span class="sxs-lookup"><span data-stu-id="f2478-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="f2478-124">Du kan använda Get-AzureRmVM cmdlet för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="f2478-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="f2478-125">Du kan använda New-AzureRmVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="f2478-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2478-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2478-126">CommonParameters</span></span>
<span data-ttu-id="f2478-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2478-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2478-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2478-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2478-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2478-129">INPUTS</span></span>

### <span data-ttu-id="f2478-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="f2478-130">None</span></span>
<span data-ttu-id="f2478-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f2478-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2478-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2478-132">OUTPUTS</span></span>

## <span data-ttu-id="f2478-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2478-133">NOTES</span></span>

## <span data-ttu-id="f2478-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2478-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2478-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f2478-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f2478-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f2478-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f2478-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f2478-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f2478-138">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f2478-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
