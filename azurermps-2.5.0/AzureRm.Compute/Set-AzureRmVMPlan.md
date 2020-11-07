---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931482"
---
# <span data-ttu-id="4777d-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="4777d-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="4777d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4777d-102">SYNOPSIS</span></span>
<span data-ttu-id="4777d-103">Ställer in information om Marketplace på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4777d-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4777d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4777d-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4777d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4777d-105">DESCRIPTION</span></span>
<span data-ttu-id="4777d-106">Cmdleten **set-AzureRmVMPlan** anger abonnemangs informationen för Azure Marketplace för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4777d-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="4777d-107">Innan du kan distribuera en Marketplace-avbildning via kommando raden måste program varan vara aktive rad eller den virtuella datorn måste distribueras med Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="4777d-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="4777d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4777d-108">EXAMPLES</span></span>

## <span data-ttu-id="4777d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4777d-109">PARAMETERS</span></span>

### <span data-ttu-id="4777d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4777d-110">-DefaultProfile</span></span>
<span data-ttu-id="4777d-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4777d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4777d-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="4777d-112">-Name</span></span>
<span data-ttu-id="4777d-113">Anger namnet på bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4777d-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="4777d-114">Det här är samma värde som returneras av Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4777d-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="4777d-115">Mer information om hur du hittar bild information finns i navigera och välja bilder i Azure Virtual Machine med PowerShell och Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) i dokumentationen till Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4777d-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="4777d-116">-Produkt</span><span class="sxs-lookup"><span data-stu-id="4777d-116">-Product</span></span>
<span data-ttu-id="4777d-117">Anger produkten av bilden från Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4777d-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="4777d-118">Det här är samma information **som värdet för** **imageReference** -elementet.</span><span class="sxs-lookup"><span data-stu-id="4777d-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="4777d-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="4777d-119">-PromotionCode</span></span>
<span data-ttu-id="4777d-120">Anger en kampanj kod.</span><span class="sxs-lookup"><span data-stu-id="4777d-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="4777d-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4777d-121">-Publisher</span></span>
<span data-ttu-id="4777d-122">Anger bildens utgivare.</span><span class="sxs-lookup"><span data-stu-id="4777d-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="4777d-123">Du kan hitta den här informationen genom att använda Get-AzureRmVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4777d-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4777d-124">-VM</span><span class="sxs-lookup"><span data-stu-id="4777d-124">-VM</span></span>
<span data-ttu-id="4777d-125">Anger det virtuella dator objekt för vilket du vill ange en Marketplace-plan.</span><span class="sxs-lookup"><span data-stu-id="4777d-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="4777d-126">Du kan använda Get-AzureRmVM cmdlet för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="4777d-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="4777d-127">Du kan använda New-AzureRmVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="4777d-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="4777d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4777d-128">CommonParameters</span></span>
<span data-ttu-id="4777d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4777d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4777d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4777d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4777d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4777d-131">INPUTS</span></span>

### <span data-ttu-id="4777d-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4777d-132">PSVirtualMachine</span></span>
<span data-ttu-id="4777d-133">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4777d-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="4777d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4777d-134">OUTPUTS</span></span>

### <span data-ttu-id="4777d-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4777d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4777d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4777d-136">NOTES</span></span>

## <span data-ttu-id="4777d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4777d-137">RELATED LINKS</span></span>

[<span data-ttu-id="4777d-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4777d-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4777d-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4777d-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4777d-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4777d-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4777d-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4777d-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
