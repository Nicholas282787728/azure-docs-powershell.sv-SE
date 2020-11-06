---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575842"
---
# <span data-ttu-id="13725-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="13725-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="13725-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13725-102">SYNOPSIS</span></span>
<span data-ttu-id="13725-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13725-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13725-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13725-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13725-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13725-105">DESCRIPTION</span></span>
<span data-ttu-id="13725-106">Cmdleten **Remove-AzureRmServiceBusNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13725-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="13725-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13725-107">EXAMPLES</span></span>

### <span data-ttu-id="13725-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13725-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="13725-109">Tar bort Service Bus-namnområdet `SB-Example1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="13725-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="13725-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13725-110">PARAMETERS</span></span>

### <span data-ttu-id="13725-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="13725-111">-NamespaceName</span></span>
<span data-ttu-id="13725-112">Namn på Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="13725-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="13725-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13725-113">-ResourceGroup</span></span>
<span data-ttu-id="13725-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13725-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13725-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13725-115">-Confirm</span></span>
<span data-ttu-id="13725-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13725-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13725-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13725-117">-WhatIf</span></span>
<span data-ttu-id="13725-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13725-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13725-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13725-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13725-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13725-120">CommonParameters</span></span>
<span data-ttu-id="13725-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13725-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13725-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13725-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13725-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13725-123">INPUTS</span></span>

### <span data-ttu-id="13725-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13725-124">-ResourceGroup</span></span>
 <span data-ttu-id="13725-125">System. String</span><span class="sxs-lookup"><span data-stu-id="13725-125">System.String</span></span>

### <span data-ttu-id="13725-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="13725-126">-NamespaceName</span></span>
 <span data-ttu-id="13725-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13725-127">System.String</span></span>

## <span data-ttu-id="13725-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13725-128">OUTPUTS</span></span>

### <span data-ttu-id="13725-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="13725-129">System.Object</span></span>

## <span data-ttu-id="13725-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13725-130">NOTES</span></span>

## <span data-ttu-id="13725-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13725-131">RELATED LINKS</span></span>

