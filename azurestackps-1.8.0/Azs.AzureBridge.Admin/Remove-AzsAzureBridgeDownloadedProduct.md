---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93931665"
---
# <span data-ttu-id="cd96d-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="cd96d-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="cd96d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd96d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd96d-103">Ta bort en produkt som har laddats ned från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="cd96d-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="cd96d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd96d-104">SYNTAX</span></span>

### <span data-ttu-id="cd96d-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="cd96d-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd96d-106">ID</span><span class="sxs-lookup"><span data-stu-id="cd96d-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd96d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd96d-107">DESCRIPTION</span></span>
<span data-ttu-id="cd96d-108">Ta bort en produkt som har laddats ned från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="cd96d-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="cd96d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd96d-109">EXAMPLES</span></span>

### <span data-ttu-id="cd96d-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="cd96d-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="cd96d-111">Ta bort en produkt som har laddats ned från Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="cd96d-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="cd96d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd96d-112">PARAMETERS</span></span>

### <span data-ttu-id="cd96d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd96d-113">-Name</span></span>
<span data-ttu-id="cd96d-114">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="cd96d-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd96d-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="cd96d-115">-ActivationName</span></span>
<span data-ttu-id="cd96d-116">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="cd96d-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd96d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd96d-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd96d-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="cd96d-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd96d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cd96d-119">-Force</span></span>
<span data-ttu-id="cd96d-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cd96d-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd96d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd96d-121">-ResourceId</span></span>
<span data-ttu-id="cd96d-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cd96d-122">The resource id.</span></span>

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

### <span data-ttu-id="cd96d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd96d-123">-AsJob</span></span>
<span data-ttu-id="cd96d-124">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="cd96d-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cd96d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd96d-125">-WhatIf</span></span>
<span data-ttu-id="cd96d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd96d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd96d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd96d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd96d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd96d-128">-Confirm</span></span>
<span data-ttu-id="cd96d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd96d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd96d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd96d-130">CommonParameters</span></span>
<span data-ttu-id="cd96d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd96d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd96d-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd96d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd96d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd96d-133">INPUTS</span></span>

## <span data-ttu-id="cd96d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd96d-134">OUTPUTS</span></span>

### <span data-ttu-id="cd96d-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="cd96d-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="cd96d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd96d-136">NOTES</span></span>

## <span data-ttu-id="cd96d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd96d-137">RELATED LINKS</span></span>