---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583784"
---
# <span data-ttu-id="21127-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="21127-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="21127-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21127-102">SYNOPSIS</span></span>
<span data-ttu-id="21127-103">Returnerar beskrivningen av den angivna beskrivningen av auktoriseringsregeln för det angivna ämnet.</span><span class="sxs-lookup"><span data-stu-id="21127-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21127-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21127-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21127-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21127-105">DESCRIPTION</span></span>
<span data-ttu-id="21127-106">Cmdleten **Get-AzureRmServiceBusTopicAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="21127-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="21127-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21127-107">EXAMPLES</span></span>

### <span data-ttu-id="21127-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="21127-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="21127-109">Returnerar beskrivningen av den angivna auktoriseringsregeln för det angivna ämnet.</span><span class="sxs-lookup"><span data-stu-id="21127-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="21127-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21127-110">PARAMETERS</span></span>

### <span data-ttu-id="21127-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21127-111">-ResourceGroup</span></span>
<span data-ttu-id="21127-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="21127-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="21127-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21127-113">-DefaultProfile</span></span>
<span data-ttu-id="21127-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21127-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21127-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="21127-115">-Name</span></span>
<span data-ttu-id="21127-116">Ämnes namn för AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="21127-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="21127-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="21127-117">-Namespace</span></span>
<span data-ttu-id="21127-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="21127-118">Namespace Name.</span></span>

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

### <span data-ttu-id="21127-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="21127-119">-Topic</span></span>
<span data-ttu-id="21127-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="21127-120">Topic Name.</span></span>

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

### <span data-ttu-id="21127-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21127-121">CommonParameters</span></span>
<span data-ttu-id="21127-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21127-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21127-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21127-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21127-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21127-124">INPUTS</span></span>

### <span data-ttu-id="21127-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21127-125">-ResourceGroup</span></span>
 <span data-ttu-id="21127-126">System. String</span><span class="sxs-lookup"><span data-stu-id="21127-126">System.String</span></span>
 

### <span data-ttu-id="21127-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="21127-127">-NamespaceName</span></span>
 <span data-ttu-id="21127-128">System. String</span><span class="sxs-lookup"><span data-stu-id="21127-128">System.String</span></span>
 

### <span data-ttu-id="21127-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="21127-129">-TopicName</span></span>
 <span data-ttu-id="21127-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21127-130">System.String</span></span>
 

### <span data-ttu-id="21127-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="21127-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="21127-132">System. String</span><span class="sxs-lookup"><span data-stu-id="21127-132">System.String</span></span>

## <span data-ttu-id="21127-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21127-133">OUTPUTS</span></span>

### <span data-ttu-id="21127-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="21127-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="21127-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Skriv: Microsoft. ServiceBus/AuthorizationRules namn: SBTopicAuthoRule1 plats: West US-Taggar: rättigheter: {avlyssna, skicka}</span><span class="sxs-lookup"><span data-stu-id="21127-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="21127-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21127-136">NOTES</span></span>

## <span data-ttu-id="21127-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21127-137">RELATED LINKS</span></span>

