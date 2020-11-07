---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93931674"
---
# <span data-ttu-id="ed10d-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="ed10d-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="ed10d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed10d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed10d-103">Laddar ned en produkt från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ed10d-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="ed10d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed10d-104">SYNTAX</span></span>

### <span data-ttu-id="ed10d-105">Products_Download (standard)</span><span class="sxs-lookup"><span data-stu-id="ed10d-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed10d-106">ID</span><span class="sxs-lookup"><span data-stu-id="ed10d-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed10d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed10d-107">DESCRIPTION</span></span>
<span data-ttu-id="ed10d-108">Laddar ned en produkt från Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ed10d-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="ed10d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed10d-109">EXAMPLES</span></span>

### <span data-ttu-id="ed10d-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ed10d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="ed10d-111">Ladda ned en produkt från Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="ed10d-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="ed10d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed10d-112">PARAMETERS</span></span>

### <span data-ttu-id="ed10d-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="ed10d-113">-ActivationName</span></span>
<span data-ttu-id="ed10d-114">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="ed10d-114">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed10d-115">-AsJob</span></span>
<span data-ttu-id="ed10d-116">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="ed10d-116">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ed10d-117">-Force</span></span>
<span data-ttu-id="ed10d-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ed10d-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed10d-119">-Name</span></span>
<span data-ttu-id="ed10d-120">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="ed10d-120">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed10d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed10d-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="ed10d-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed10d-123">-ResourceId</span></span>
<span data-ttu-id="ed10d-124">Resurs-ID för Azure Bridge-produkten.</span><span class="sxs-lookup"><span data-stu-id="ed10d-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="ed10d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed10d-125">-Confirm</span></span>
<span data-ttu-id="ed10d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed10d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed10d-127">-WhatIf</span></span>
<span data-ttu-id="ed10d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed10d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed10d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed10d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed10d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed10d-130">CommonParameters</span></span>
<span data-ttu-id="ed10d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed10d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed10d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed10d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed10d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed10d-133">INPUTS</span></span>

## <span data-ttu-id="ed10d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed10d-134">OUTPUTS</span></span>

## <span data-ttu-id="ed10d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed10d-135">NOTES</span></span>

## <span data-ttu-id="ed10d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed10d-136">RELATED LINKS</span></span>

