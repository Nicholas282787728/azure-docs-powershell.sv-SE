---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583000"
---
# <span data-ttu-id="4d91d-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4d91d-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="4d91d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d91d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d91d-103">Tar bort abonnemanget till ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="4d91d-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d91d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d91d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d91d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d91d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d91d-106">Cmdleten **Remove-AzureRmServiceBusSubscription** tar bort prenumerationen på ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="4d91d-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4d91d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d91d-107">EXAMPLES</span></span>

### <span data-ttu-id="4d91d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d91d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="4d91d-109">Tar bort abonnemanget `SB-TopicSubscription-Example1` till avsnittet `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="4d91d-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="4d91d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d91d-110">PARAMETERS</span></span>

### <span data-ttu-id="4d91d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d91d-111">-DefaultProfile</span></span>
<span data-ttu-id="4d91d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d91d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d91d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d91d-113">-Name</span></span>
<span data-ttu-id="4d91d-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="4d91d-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d91d-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="4d91d-115">-Namespace</span></span>
<span data-ttu-id="4d91d-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="4d91d-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d91d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d91d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d91d-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4d91d-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d91d-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="4d91d-119">-Topic</span></span>
<span data-ttu-id="4d91d-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="4d91d-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d91d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d91d-121">-Confirm</span></span>
<span data-ttu-id="4d91d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d91d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d91d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d91d-123">-WhatIf</span></span>
<span data-ttu-id="4d91d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d91d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d91d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d91d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d91d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d91d-126">CommonParameters</span></span>
<span data-ttu-id="4d91d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d91d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d91d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d91d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d91d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d91d-129">INPUTS</span></span>

### <span data-ttu-id="4d91d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d91d-130">-ResourceGroup</span></span>
 <span data-ttu-id="4d91d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d91d-131">System.String</span></span>

### <span data-ttu-id="4d91d-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4d91d-132">-NamespaceName</span></span>
 <span data-ttu-id="4d91d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d91d-133">System.String</span></span>

### <span data-ttu-id="4d91d-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4d91d-134">-TopicName</span></span>
 <span data-ttu-id="4d91d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4d91d-135">System.String</span></span>

### <span data-ttu-id="4d91d-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4d91d-136">-SubscriptionName</span></span>
 <span data-ttu-id="4d91d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4d91d-137">System.String</span></span>

## <span data-ttu-id="4d91d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d91d-138">OUTPUTS</span></span>

### <span data-ttu-id="4d91d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d91d-139">System.Boolean</span></span>

## <span data-ttu-id="4d91d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d91d-140">NOTES</span></span>

## <span data-ttu-id="4d91d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d91d-141">RELATED LINKS</span></span>

