---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575836"
---
# <span data-ttu-id="54155-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="54155-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="54155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54155-102">SYNOPSIS</span></span>
<span data-ttu-id="54155-103">Tar bort abonnemanget till ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="54155-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54155-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54155-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54155-105">DESCRIPTION</span></span>
<span data-ttu-id="54155-106">Cmdleten **Remove-AzureRmServiceBusSubscription** tar bort prenumerationen på ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="54155-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="54155-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54155-107">EXAMPLES</span></span>

### <span data-ttu-id="54155-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54155-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="54155-109">Tar bort abonnemanget `SB-TopicSubscription-Example1` till avsnittet `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="54155-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="54155-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54155-110">PARAMETERS</span></span>

### <span data-ttu-id="54155-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54155-111">-Confirm</span></span>
<span data-ttu-id="54155-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54155-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54155-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54155-113">-WhatIf</span></span>
<span data-ttu-id="54155-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54155-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54155-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54155-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54155-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54155-116">-DefaultProfile</span></span>
<span data-ttu-id="54155-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54155-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54155-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="54155-118">-Name</span></span>
<span data-ttu-id="54155-119">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="54155-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54155-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="54155-120">-Namespace</span></span>
<span data-ttu-id="54155-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="54155-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54155-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54155-122">-ResourceGroupName</span></span>
<span data-ttu-id="54155-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="54155-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54155-124">-Ämne</span><span class="sxs-lookup"><span data-stu-id="54155-124">-Topic</span></span>
<span data-ttu-id="54155-125">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="54155-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54155-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54155-126">CommonParameters</span></span>
<span data-ttu-id="54155-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54155-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54155-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54155-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54155-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54155-129">INPUTS</span></span>

### <span data-ttu-id="54155-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54155-130">-ResourceGroup</span></span>
 <span data-ttu-id="54155-131">System. String</span><span class="sxs-lookup"><span data-stu-id="54155-131">System.String</span></span>

### <span data-ttu-id="54155-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="54155-132">-NamespaceName</span></span>
 <span data-ttu-id="54155-133">System. String</span><span class="sxs-lookup"><span data-stu-id="54155-133">System.String</span></span>

### <span data-ttu-id="54155-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="54155-134">-TopicName</span></span>
 <span data-ttu-id="54155-135">System. String</span><span class="sxs-lookup"><span data-stu-id="54155-135">System.String</span></span>

### <span data-ttu-id="54155-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="54155-136">-SubscriptionName</span></span>
 <span data-ttu-id="54155-137">System. String</span><span class="sxs-lookup"><span data-stu-id="54155-137">System.String</span></span>

## <span data-ttu-id="54155-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54155-138">OUTPUTS</span></span>

### <span data-ttu-id="54155-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54155-139">System.Boolean</span></span>

## <span data-ttu-id="54155-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54155-140">NOTES</span></span>

## <span data-ttu-id="54155-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54155-141">RELATED LINKS</span></span>

