---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b7cc2211df4fd8b9d65c3e93483a485a10ae32
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94100561"
---
# <span data-ttu-id="2eb50-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="2eb50-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="2eb50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eb50-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb50-103">Returnerar en lista med produkter som hämtats från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="2eb50-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="2eb50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eb50-104">SYNTAX</span></span>

### <span data-ttu-id="2eb50-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="2eb50-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2eb50-106">Lära</span><span class="sxs-lookup"><span data-stu-id="2eb50-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="2eb50-107">ID</span><span class="sxs-lookup"><span data-stu-id="2eb50-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2eb50-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eb50-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb50-109">Returnerar en lista med produkter som hämtats från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="2eb50-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="2eb50-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eb50-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb50-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2eb50-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="2eb50-112">Få en lista över nedladdade Azure-bryggor</span><span class="sxs-lookup"><span data-stu-id="2eb50-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="2eb50-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2eb50-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="2eb50-114">Skaffa en Azure-brygga Hämtad produkt efter namn</span><span class="sxs-lookup"><span data-stu-id="2eb50-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="2eb50-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eb50-115">PARAMETERS</span></span>

### <span data-ttu-id="2eb50-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="2eb50-116">-ActivationName</span></span>
<span data-ttu-id="2eb50-117">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="2eb50-117">Name of the activation.</span></span>

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

### <span data-ttu-id="2eb50-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2eb50-118">-Name</span></span>
<span data-ttu-id="2eb50-119">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="2eb50-119">Name of the product.</span></span>

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

### <span data-ttu-id="2eb50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb50-120">-ResourceGroupName</span></span>
<span data-ttu-id="2eb50-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="2eb50-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2eb50-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb50-122">-ResourceId</span></span>
<span data-ttu-id="2eb50-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2eb50-123">The resource id.</span></span>

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

### <span data-ttu-id="2eb50-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="2eb50-124">-Skip</span></span>
<span data-ttu-id="2eb50-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="2eb50-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2eb50-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="2eb50-126">-Top</span></span>
<span data-ttu-id="2eb50-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="2eb50-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2eb50-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="2eb50-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2eb50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb50-129">CommonParameters</span></span>
<span data-ttu-id="2eb50-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb50-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb50-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb50-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eb50-132">INPUTS</span></span>

## <span data-ttu-id="2eb50-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eb50-133">OUTPUTS</span></span>

### <span data-ttu-id="2eb50-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="2eb50-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="2eb50-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eb50-135">NOTES</span></span>

## <span data-ttu-id="2eb50-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eb50-136">RELATED LINKS</span></span>

