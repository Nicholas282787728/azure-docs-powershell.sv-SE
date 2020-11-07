---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93758469"
---
# <span data-ttu-id="d20f5-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="d20f5-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="d20f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d20f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d20f5-103">Ta bort en produkt som har laddats ned från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="d20f5-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d20f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d20f5-104">SYNTAX</span></span>

### <span data-ttu-id="d20f5-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="d20f5-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20f5-106">ID</span><span class="sxs-lookup"><span data-stu-id="d20f5-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d20f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d20f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d20f5-108">Ta bort en produkt som har laddats ned från Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="d20f5-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d20f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d20f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d20f5-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d20f5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="d20f5-111">Ta bort en produkt som har laddats ned från Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="d20f5-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="d20f5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d20f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d20f5-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="d20f5-113">-ActivationName</span></span>
<span data-ttu-id="d20f5-114">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="d20f5-114">Name of the activation.</span></span>

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

### <span data-ttu-id="d20f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d20f5-115">-AsJob</span></span>
<span data-ttu-id="d20f5-116">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="d20f5-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d20f5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d20f5-117">-Force</span></span>
<span data-ttu-id="d20f5-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d20f5-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d20f5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d20f5-119">-Name</span></span>
<span data-ttu-id="d20f5-120">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="d20f5-120">Name of the product.</span></span>

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

### <span data-ttu-id="d20f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d20f5-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="d20f5-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d20f5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20f5-123">-ResourceId</span></span>
<span data-ttu-id="d20f5-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d20f5-124">The resource id.</span></span>

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

### <span data-ttu-id="d20f5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d20f5-125">-Confirm</span></span>
<span data-ttu-id="d20f5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d20f5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d20f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d20f5-127">-WhatIf</span></span>
<span data-ttu-id="d20f5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d20f5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d20f5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d20f5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d20f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20f5-130">CommonParameters</span></span>
<span data-ttu-id="d20f5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20f5-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20f5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d20f5-133">INPUTS</span></span>

## <span data-ttu-id="d20f5-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d20f5-134">OUTPUTS</span></span>

### <span data-ttu-id="d20f5-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="d20f5-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="d20f5-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d20f5-136">NOTES</span></span>

## <span data-ttu-id="d20f5-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d20f5-137">RELATED LINKS</span></span>

