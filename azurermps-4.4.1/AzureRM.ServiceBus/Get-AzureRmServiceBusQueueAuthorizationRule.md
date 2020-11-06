---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575851"
---
# <span data-ttu-id="0ad67-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0ad67-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="0ad67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ad67-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad67-103">Hämtar beskrivningen av en angiven auktoriseringsregel för en given Service Bus-kö.</span><span class="sxs-lookup"><span data-stu-id="0ad67-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ad67-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ad67-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad67-106">Cmdleten **Get-AzureRmServiceBusQueueAuthorizationRule** hämtar beskrivningen av en angiven auktoriseringsregel i den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="0ad67-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="0ad67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ad67-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad67-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ad67-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="0ad67-109">Returnerar den angivna beskrivningen för auktoriseringsregeln för en given tjänst buss kö.</span><span class="sxs-lookup"><span data-stu-id="0ad67-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="0ad67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ad67-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad67-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ad67-111">-ResourceGroup</span></span>
<span data-ttu-id="0ad67-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0ad67-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad67-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad67-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad67-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad67-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ad67-115">-Name</span></span>
<span data-ttu-id="0ad67-116">EventHub-AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="0ad67-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad67-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="0ad67-117">-Namespace</span></span>
<span data-ttu-id="0ad67-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="0ad67-118">Namespace Name.</span></span>

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

### <span data-ttu-id="0ad67-119">-Kö</span><span class="sxs-lookup"><span data-stu-id="0ad67-119">-Queue</span></span>
<span data-ttu-id="0ad67-120">Könamn.</span><span class="sxs-lookup"><span data-stu-id="0ad67-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad67-121">CommonParameters</span></span>
<span data-ttu-id="0ad67-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad67-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad67-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad67-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ad67-124">INPUTS</span></span>

### <span data-ttu-id="0ad67-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ad67-125">-ResourceGroup</span></span>
 <span data-ttu-id="0ad67-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad67-126">System.String</span></span>
 

### <span data-ttu-id="0ad67-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0ad67-127">-NamespaceName</span></span>
 <span data-ttu-id="0ad67-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad67-128">System.String</span></span>
 

### <span data-ttu-id="0ad67-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="0ad67-129">-QueueName</span></span>
 <span data-ttu-id="0ad67-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad67-130">System.String</span></span>
 

### <span data-ttu-id="0ad67-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0ad67-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="0ad67-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad67-132">System.String</span></span>

## <span data-ttu-id="0ad67-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ad67-133">OUTPUTS</span></span>

### <span data-ttu-id="0ad67-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0ad67-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0ad67-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Skriv: Microsoft. ServiceBus/AuthorizationRules namn: SBAuthoRule1 plats: West US-Taggar: rättigheter: {avlyssna, skicka}</span><span class="sxs-lookup"><span data-stu-id="0ad67-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="0ad67-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ad67-136">NOTES</span></span>

## <span data-ttu-id="0ad67-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ad67-137">RELATED LINKS</span></span>

