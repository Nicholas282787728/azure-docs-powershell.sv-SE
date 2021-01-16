---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400264"
---
# <span data-ttu-id="e0515-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0515-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e0515-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0515-102">SYNOPSIS</span></span>
<span data-ttu-id="e0515-103">Hämtar en beskrivning av den angivna auktoriseringsregeln för ett angivet namn område eller en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="e0515-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="e0515-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0515-104">SYNTAX</span></span>

### <span data-ttu-id="e0515-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e0515-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0515-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0515-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0515-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0515-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0515-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0515-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0515-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0515-109">DESCRIPTION</span></span>
<span data-ttu-id="e0515-110">Cmdleten **Get-AzServiceBusAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i det angivna namn området, i kön eller i ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="e0515-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="e0515-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0515-111">EXAMPLES</span></span>

### <span data-ttu-id="e0515-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0515-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e0515-113">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="e0515-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e0515-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e0515-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e0515-115">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss kö.</span><span class="sxs-lookup"><span data-stu-id="e0515-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="e0515-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e0515-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e0515-117">Returnerar den angivna beskrivningen av auktoriseringsregeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="e0515-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="e0515-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="e0515-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="e0515-119">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss namnrymd och ett alias.</span><span class="sxs-lookup"><span data-stu-id="e0515-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="e0515-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0515-120">PARAMETERS</span></span>

### <span data-ttu-id="e0515-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e0515-121">-AliasName</span></span>
<span data-ttu-id="e0515-122">GeoDR konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="e0515-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="e0515-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0515-123">-DefaultProfile</span></span>
<span data-ttu-id="e0515-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0515-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0515-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0515-125">-Name</span></span>
<span data-ttu-id="e0515-126">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="e0515-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e0515-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e0515-127">-Namespace</span></span>
<span data-ttu-id="e0515-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e0515-128">Namespace Name</span></span>

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

### <span data-ttu-id="e0515-129">-Kö</span><span class="sxs-lookup"><span data-stu-id="e0515-129">-Queue</span></span>
<span data-ttu-id="e0515-130">Könamn</span><span class="sxs-lookup"><span data-stu-id="e0515-130">Queue Name</span></span>

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

### <span data-ttu-id="e0515-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0515-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0515-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e0515-132">Resource Group Name</span></span>

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

### <span data-ttu-id="e0515-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="e0515-133">-Topic</span></span>
<span data-ttu-id="e0515-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="e0515-134">Topic Name</span></span>

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

### <span data-ttu-id="e0515-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0515-135">CommonParameters</span></span>
<span data-ttu-id="e0515-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0515-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0515-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0515-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0515-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0515-138">INPUTS</span></span>

### <span data-ttu-id="e0515-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e0515-139">System.String</span></span>

## <span data-ttu-id="e0515-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0515-140">OUTPUTS</span></span>

### <span data-ttu-id="e0515-141">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e0515-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e0515-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0515-142">NOTES</span></span>

## <span data-ttu-id="e0515-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0515-143">RELATED LINKS</span></span>
