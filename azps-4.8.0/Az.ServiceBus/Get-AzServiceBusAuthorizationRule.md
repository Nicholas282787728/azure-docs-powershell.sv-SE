---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101970"
---
# <span data-ttu-id="e14ea-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e14ea-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e14ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e14ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e14ea-103">Hämtar en beskrivning av den angivna auktoriseringsregeln för ett angivet namn område eller en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="e14ea-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="e14ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e14ea-104">SYNTAX</span></span>

### <span data-ttu-id="e14ea-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e14ea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e14ea-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e14ea-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e14ea-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e14ea-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e14ea-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e14ea-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e14ea-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e14ea-109">DESCRIPTION</span></span>
<span data-ttu-id="e14ea-110">Cmdleten **Get-AzServiceBusAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i det angivna namn området, i kön eller i ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="e14ea-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="e14ea-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e14ea-111">EXAMPLES</span></span>

### <span data-ttu-id="e14ea-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e14ea-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e14ea-113">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="e14ea-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e14ea-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e14ea-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e14ea-115">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss kö.</span><span class="sxs-lookup"><span data-stu-id="e14ea-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="e14ea-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e14ea-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e14ea-117">Returnerar den angivna beskrivningen av auktoriseringsregeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="e14ea-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="e14ea-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="e14ea-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="e14ea-119">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss namnrymd och ett alias.</span><span class="sxs-lookup"><span data-stu-id="e14ea-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="e14ea-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e14ea-120">PARAMETERS</span></span>

### <span data-ttu-id="e14ea-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e14ea-121">-AliasName</span></span>
<span data-ttu-id="e14ea-122">GeoDR konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="e14ea-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e14ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14ea-123">-DefaultProfile</span></span>
<span data-ttu-id="e14ea-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e14ea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14ea-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e14ea-125">-Name</span></span>
<span data-ttu-id="e14ea-126">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="e14ea-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e14ea-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e14ea-127">-Namespace</span></span>
<span data-ttu-id="e14ea-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e14ea-128">Namespace Name</span></span>

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

### <span data-ttu-id="e14ea-129">-Kö</span><span class="sxs-lookup"><span data-stu-id="e14ea-129">-Queue</span></span>
<span data-ttu-id="e14ea-130">Könamn</span><span class="sxs-lookup"><span data-stu-id="e14ea-130">Queue Name</span></span>

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

### <span data-ttu-id="e14ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="e14ea-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e14ea-132">Resource Group Name</span></span>

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

### <span data-ttu-id="e14ea-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="e14ea-133">-Topic</span></span>
<span data-ttu-id="e14ea-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="e14ea-134">Topic Name</span></span>

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

### <span data-ttu-id="e14ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14ea-135">CommonParameters</span></span>
<span data-ttu-id="e14ea-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14ea-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e14ea-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14ea-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e14ea-138">INPUTS</span></span>

### <span data-ttu-id="e14ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e14ea-139">System.String</span></span>

## <span data-ttu-id="e14ea-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e14ea-140">OUTPUTS</span></span>

### <span data-ttu-id="e14ea-141">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e14ea-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e14ea-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e14ea-142">NOTES</span></span>

## <span data-ttu-id="e14ea-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e14ea-143">RELATED LINKS</span></span>
