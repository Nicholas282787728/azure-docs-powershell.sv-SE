---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94100569"
---
# <span data-ttu-id="66c03-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="66c03-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="66c03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66c03-102">SYNOPSIS</span></span>
<span data-ttu-id="66c03-103">Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="66c03-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="66c03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66c03-104">SYNTAX</span></span>

### <span data-ttu-id="66c03-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="66c03-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="66c03-106">Lära</span><span class="sxs-lookup"><span data-stu-id="66c03-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="66c03-107">ID</span><span class="sxs-lookup"><span data-stu-id="66c03-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="66c03-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66c03-108">DESCRIPTION</span></span>
<span data-ttu-id="66c03-109">Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="66c03-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="66c03-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66c03-110">EXAMPLES</span></span>

### <span data-ttu-id="66c03-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="66c03-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="66c03-112">Få en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="66c03-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="66c03-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="66c03-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="66c03-114">Skaffa en produkt information som kan laddas ner från Azure Marketplace med namn.</span><span class="sxs-lookup"><span data-stu-id="66c03-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="66c03-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66c03-115">PARAMETERS</span></span>

### <span data-ttu-id="66c03-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="66c03-116">-ActivationName</span></span>
<span data-ttu-id="66c03-117">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="66c03-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="66c03-118">-Name</span></span>
<span data-ttu-id="66c03-119">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="66c03-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c03-120">-ResourceGroupName</span></span>
<span data-ttu-id="66c03-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="66c03-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c03-122">-ResourceId</span></span>
<span data-ttu-id="66c03-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="66c03-123">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="66c03-124">-Skip</span></span>
<span data-ttu-id="66c03-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="66c03-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="66c03-126">-Top</span></span>
<span data-ttu-id="66c03-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="66c03-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="66c03-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="66c03-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c03-129">CommonParameters</span></span>
<span data-ttu-id="66c03-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c03-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c03-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c03-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66c03-132">INPUTS</span></span>

## <span data-ttu-id="66c03-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66c03-133">OUTPUTS</span></span>

### <span data-ttu-id="66c03-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="66c03-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="66c03-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66c03-135">NOTES</span></span>

## <span data-ttu-id="66c03-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66c03-136">RELATED LINKS</span></span>

