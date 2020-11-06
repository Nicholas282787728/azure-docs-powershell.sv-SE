---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585311"
---
# <span data-ttu-id="c3879-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3879-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="c3879-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3879-102">SYNOPSIS</span></span>
<span data-ttu-id="c3879-103">Hämtar en beskrivning av den angivna auktoriseringsregeln för ett angivet namn område eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="c3879-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3879-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3879-104">SYNTAX</span></span>

### <span data-ttu-id="c3879-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c3879-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3879-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3879-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3879-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3879-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3879-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3879-108">DESCRIPTION</span></span>
<span data-ttu-id="c3879-109">Cmdleten **Get-AzureRmServiceBusAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i ett namn område eller i en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="c3879-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="c3879-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3879-110">EXAMPLES</span></span>

### <span data-ttu-id="c3879-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3879-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="c3879-112">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="c3879-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="c3879-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c3879-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="c3879-114">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss kö.</span><span class="sxs-lookup"><span data-stu-id="c3879-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="c3879-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c3879-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="c3879-116">Returnerar den angivna beskrivningen av auktoriseringsregeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="c3879-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="c3879-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3879-117">PARAMETERS</span></span>

### <span data-ttu-id="c3879-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3879-118">-Name</span></span>
<span data-ttu-id="c3879-119">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="c3879-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3879-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c3879-120">-Namespace</span></span>
<span data-ttu-id="c3879-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="c3879-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3879-122">-Kö</span><span class="sxs-lookup"><span data-stu-id="c3879-122">-Queue</span></span>
<span data-ttu-id="c3879-123">Könamn.</span><span class="sxs-lookup"><span data-stu-id="c3879-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3879-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3879-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3879-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c3879-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c3879-126">-Ämne</span><span class="sxs-lookup"><span data-stu-id="c3879-126">-Topic</span></span>
<span data-ttu-id="c3879-127">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="c3879-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3879-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3879-128">-DefaultProfile</span></span>
<span data-ttu-id="c3879-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3879-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3879-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3879-130">CommonParameters</span></span>
<span data-ttu-id="c3879-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3879-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3879-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3879-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3879-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3879-133">INPUTS</span></span>

### <span data-ttu-id="c3879-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c3879-134">System.String</span></span>

## <span data-ttu-id="c3879-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3879-135">OUTPUTS</span></span>

### <span data-ttu-id="c3879-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c3879-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c3879-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3879-137">NOTES</span></span>
## <span data-ttu-id="c3879-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3879-138">RELATED LINKS</span></span>

## <span data-ttu-id="c3879-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3879-139">RELATED LINKS</span></span>

