---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574528"
---
# <span data-ttu-id="97c37-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="97c37-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="97c37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97c37-102">SYNOPSIS</span></span>
<span data-ttu-id="97c37-103">Hämtar primära och sekundära anslutnings strängar för ett namn område eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="97c37-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97c37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97c37-104">SYNTAX</span></span>

### <span data-ttu-id="97c37-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="97c37-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c37-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="97c37-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c37-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="97c37-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c37-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97c37-108">DESCRIPTION</span></span>
<span data-ttu-id="97c37-109">Cmdleten **Get-AzureRmServiceBusKey** returnerar primära och sekundära anslutnings strängar för ett namn område eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="97c37-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="97c37-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97c37-110">EXAMPLES</span></span>

### <span data-ttu-id="97c37-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97c37-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="97c37-112">Primära och sekundära anslutnings strängar till det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="97c37-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="97c37-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="97c37-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="97c37-114">Primära och sekundära anslutnings strängar till den angivna kön.</span><span class="sxs-lookup"><span data-stu-id="97c37-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="97c37-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="97c37-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="97c37-116">Primära och sekundära anslutnings strängar till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="97c37-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="97c37-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97c37-117">PARAMETERS</span></span>

### <span data-ttu-id="97c37-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="97c37-118">-Name</span></span>
<span data-ttu-id="97c37-119">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="97c37-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c37-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="97c37-120">-Namespace</span></span>
<span data-ttu-id="97c37-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="97c37-121">Namespace Name.</span></span>

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

### <span data-ttu-id="97c37-122">-Kö</span><span class="sxs-lookup"><span data-stu-id="97c37-122">-Queue</span></span>
<span data-ttu-id="97c37-123">Könamn.</span><span class="sxs-lookup"><span data-stu-id="97c37-123">Queue Name.</span></span>

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

### <span data-ttu-id="97c37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c37-124">-ResourceGroupName</span></span>
<span data-ttu-id="97c37-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="97c37-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="97c37-126">-Ämne</span><span class="sxs-lookup"><span data-stu-id="97c37-126">-Topic</span></span>
<span data-ttu-id="97c37-127">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="97c37-127">Topic Name.</span></span>

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

### <span data-ttu-id="97c37-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c37-128">-DefaultProfile</span></span>
<span data-ttu-id="97c37-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97c37-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c37-130">CommonParameters</span></span>
<span data-ttu-id="97c37-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c37-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c37-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c37-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97c37-133">INPUTS</span></span>

### <span data-ttu-id="97c37-134">System. String</span><span class="sxs-lookup"><span data-stu-id="97c37-134">System.String</span></span>

## <span data-ttu-id="97c37-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97c37-135">OUTPUTS</span></span>

### <span data-ttu-id="97c37-136">Microsoft. Azure. commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="97c37-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="97c37-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97c37-137">NOTES</span></span>

## <span data-ttu-id="97c37-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97c37-138">RELATED LINKS</span></span>

