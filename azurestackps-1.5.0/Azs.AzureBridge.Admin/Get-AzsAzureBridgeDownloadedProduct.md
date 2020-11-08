---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93758465"
---
# <span data-ttu-id="b8b03-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="b8b03-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="b8b03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8b03-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b03-103">Returnerar en lista med produkter som hämtats från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="b8b03-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b8b03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8b03-104">SYNTAX</span></span>

### <span data-ttu-id="b8b03-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b8b03-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8b03-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b8b03-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="b8b03-107">ID</span><span class="sxs-lookup"><span data-stu-id="b8b03-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8b03-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8b03-108">DESCRIPTION</span></span>
<span data-ttu-id="b8b03-109">Returnerar en lista med produkter som hämtats från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="b8b03-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b8b03-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8b03-110">EXAMPLES</span></span>

### <span data-ttu-id="b8b03-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8b03-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b8b03-112">Få en lista över nedladdade Azure-bryggor</span><span class="sxs-lookup"><span data-stu-id="b8b03-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="b8b03-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8b03-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b8b03-114">Skaffa en Azure-brygga Hämtad produkt efter namn</span><span class="sxs-lookup"><span data-stu-id="b8b03-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="b8b03-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8b03-115">PARAMETERS</span></span>

### <span data-ttu-id="b8b03-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="b8b03-116">-ActivationName</span></span>
<span data-ttu-id="b8b03-117">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="b8b03-117">Name of the activation.</span></span>

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

### <span data-ttu-id="b8b03-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8b03-118">-Name</span></span>
<span data-ttu-id="b8b03-119">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="b8b03-119">Name of the product.</span></span>

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

### <span data-ttu-id="b8b03-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b03-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8b03-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="b8b03-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b8b03-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8b03-122">-ResourceId</span></span>
<span data-ttu-id="b8b03-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b8b03-123">The resource id.</span></span>

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

### <span data-ttu-id="b8b03-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b8b03-124">-Skip</span></span>
<span data-ttu-id="b8b03-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b8b03-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8b03-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="b8b03-126">-Top</span></span>
<span data-ttu-id="b8b03-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b8b03-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8b03-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b8b03-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8b03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b03-129">CommonParameters</span></span>
<span data-ttu-id="b8b03-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b03-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b03-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b03-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8b03-132">INPUTS</span></span>

## <span data-ttu-id="b8b03-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8b03-133">OUTPUTS</span></span>

### <span data-ttu-id="b8b03-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="b8b03-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="b8b03-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8b03-135">NOTES</span></span>

## <span data-ttu-id="b8b03-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8b03-136">RELATED LINKS</span></span>
