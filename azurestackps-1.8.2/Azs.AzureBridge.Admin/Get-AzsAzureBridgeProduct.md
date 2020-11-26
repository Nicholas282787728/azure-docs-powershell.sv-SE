---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "94262856"
---
# <span data-ttu-id="29aca-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="29aca-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="29aca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29aca-102">SYNOPSIS</span></span>
<span data-ttu-id="29aca-103">Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="29aca-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="29aca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29aca-104">SYNTAX</span></span>

### <span data-ttu-id="29aca-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="29aca-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="29aca-106">Lära</span><span class="sxs-lookup"><span data-stu-id="29aca-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="29aca-107">ID</span><span class="sxs-lookup"><span data-stu-id="29aca-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="29aca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29aca-108">DESCRIPTION</span></span>
<span data-ttu-id="29aca-109">Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="29aca-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="29aca-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29aca-110">EXAMPLES</span></span>

### <span data-ttu-id="29aca-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="29aca-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="29aca-112">Få en lista med tillgängliga produkter att ladda ned från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="29aca-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="29aca-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="29aca-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="29aca-114">Skaffa en produkt information som kan laddas ner från Azure Marketplace med namn.</span><span class="sxs-lookup"><span data-stu-id="29aca-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="29aca-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29aca-115">PARAMETERS</span></span>

### <span data-ttu-id="29aca-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="29aca-116">-Name</span></span>
<span data-ttu-id="29aca-117">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="29aca-117">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29aca-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="29aca-118">-ActivationName</span></span>
<span data-ttu-id="29aca-119">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="29aca-119">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29aca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29aca-120">-ResourceGroupName</span></span>
<span data-ttu-id="29aca-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="29aca-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29aca-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29aca-122">-ResourceId</span></span>
<span data-ttu-id="29aca-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="29aca-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29aca-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="29aca-124">-Skip</span></span>
<span data-ttu-id="29aca-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="29aca-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="29aca-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="29aca-126">-Top</span></span>
<span data-ttu-id="29aca-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="29aca-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="29aca-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="29aca-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="29aca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29aca-129">CommonParameters</span></span>
<span data-ttu-id="29aca-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29aca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29aca-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29aca-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29aca-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29aca-132">INPUTS</span></span>

## <span data-ttu-id="29aca-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29aca-133">OUTPUTS</span></span>

### <span data-ttu-id="29aca-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="29aca-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="29aca-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29aca-135">NOTES</span></span>

## <span data-ttu-id="29aca-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29aca-136">RELATED LINKS</span></span>