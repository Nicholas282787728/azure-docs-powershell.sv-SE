---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271866"
---
# <span data-ttu-id="b5ae7-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b5ae7-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="b5ae7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ae7-103">Ta bort ett bud från en privat butik.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="b5ae7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5ae7-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ae7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5ae7-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ae7-106">Ta bort ett bud från en privat butik som har skapats i klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b5ae7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5ae7-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ae7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5ae7-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="b5ae7-109">Ta bort ett bud från en privat butik som har skapats i klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b5ae7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5ae7-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ae7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ae7-111">-DefaultProfile</span></span>
<span data-ttu-id="b5ae7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ae7-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b5ae7-113">-OfferId</span></span>
<span data-ttu-id="b5ae7-114">PrivateStore-utbud för Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="b5ae7-114">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ae7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5ae7-115">-PassThru</span></span>
<span data-ttu-id="b5ae7-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b5ae7-116">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ae7-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="b5ae7-117">-PrivateStoreId</span></span>
<span data-ttu-id="b5ae7-118">Obligatoriska Azure Marketplace-privateStore</span><span class="sxs-lookup"><span data-stu-id="b5ae7-118">Required Azure Marketplace privateStore</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ae7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5ae7-119">-Confirm</span></span>
<span data-ttu-id="b5ae7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ae7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ae7-121">-WhatIf</span></span>
<span data-ttu-id="b5ae7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ae7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ae7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ae7-124">CommonParameters</span></span>
<span data-ttu-id="b5ae7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ae7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ae7-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5ae7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ae7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5ae7-127">INPUTS</span></span>

### <span data-ttu-id="b5ae7-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="b5ae7-128">None</span></span>

## <span data-ttu-id="b5ae7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5ae7-129">OUTPUTS</span></span>

### <span data-ttu-id="b5ae7-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5ae7-130">System.Boolean</span></span>

## <span data-ttu-id="b5ae7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5ae7-131">NOTES</span></span>

## <span data-ttu-id="b5ae7-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5ae7-132">RELATED LINKS</span></span>
