---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092349"
---
# <span data-ttu-id="e6f29-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="e6f29-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="e6f29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6f29-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f29-103">Ställer in information om Marketplace på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e6f29-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="e6f29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6f29-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6f29-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f29-106">Cmdleten **set-AzVMPlan** anger abonnemangs informationen för Azure Marketplace för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e6f29-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="e6f29-107">Innan du kan distribuera en Marketplace-avbildning via kommando raden måste program varan vara aktive rad eller den virtuella datorn måste distribueras med Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="e6f29-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="e6f29-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6f29-108">EXAMPLES</span></span>

## <span data-ttu-id="e6f29-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6f29-109">PARAMETERS</span></span>

### <span data-ttu-id="e6f29-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f29-110">-DefaultProfile</span></span>
<span data-ttu-id="e6f29-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f29-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f29-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6f29-112">-Name</span></span>
<span data-ttu-id="e6f29-113">Anger namnet på bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e6f29-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="e6f29-114">Det här är samma värde som returneras av Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f29-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="e6f29-115">Mer information om hur du hittar bild information finns i navigera och välja bilder i Azure Virtual Machine med PowerShell och Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) i dokumentationen till Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f29-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="e6f29-116">-Produkt</span><span class="sxs-lookup"><span data-stu-id="e6f29-116">-Product</span></span>
<span data-ttu-id="e6f29-117">Anger produkten av bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e6f29-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="e6f29-118">Det här är samma information **som värdet för** **imageReference** -elementet.</span><span class="sxs-lookup"><span data-stu-id="e6f29-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f29-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="e6f29-119">-PromotionCode</span></span>
<span data-ttu-id="e6f29-120">Anger en kampanj kod.</span><span class="sxs-lookup"><span data-stu-id="e6f29-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f29-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e6f29-121">-Publisher</span></span>
<span data-ttu-id="e6f29-122">Anger bildens utgivare.</span><span class="sxs-lookup"><span data-stu-id="e6f29-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="e6f29-123">Du kan hitta den här informationen genom att använda Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f29-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f29-124">-VM</span><span class="sxs-lookup"><span data-stu-id="e6f29-124">-VM</span></span>
<span data-ttu-id="e6f29-125">Anger det virtuella dator objekt för vilket du vill ange en Marketplace-plan.</span><span class="sxs-lookup"><span data-stu-id="e6f29-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="e6f29-126">Du kan använda Get-AzVM cmdlet för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e6f29-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="e6f29-127">Du kan använda New-AzVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e6f29-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f29-128">CommonParameters</span></span>
<span data-ttu-id="e6f29-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f29-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6f29-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f29-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6f29-131">INPUTS</span></span>

### <span data-ttu-id="e6f29-132">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6f29-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e6f29-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f29-133">System.String</span></span>

## <span data-ttu-id="e6f29-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6f29-134">OUTPUTS</span></span>

### <span data-ttu-id="e6f29-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6f29-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e6f29-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6f29-136">NOTES</span></span>

## <span data-ttu-id="e6f29-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6f29-137">RELATED LINKS</span></span>

[<span data-ttu-id="e6f29-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6f29-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e6f29-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e6f29-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e6f29-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e6f29-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="e6f29-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e6f29-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
