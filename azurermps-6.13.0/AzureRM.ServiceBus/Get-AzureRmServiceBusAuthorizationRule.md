---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 8c69ab59f539180c3146f01c7a5fce9907b40c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755320"
---
# <span data-ttu-id="35003-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="35003-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="35003-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35003-102">SYNOPSIS</span></span>
<span data-ttu-id="35003-103">Hämtar en beskrivning av den angivna auktoriseringsregeln för ett angivet namn område eller en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="35003-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35003-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35003-104">SYNTAX</span></span>

### <span data-ttu-id="35003-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="35003-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35003-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="35003-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35003-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="35003-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35003-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="35003-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35003-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35003-109">DESCRIPTION</span></span>
<span data-ttu-id="35003-110">Cmdleten **Get-AzureRmServiceBusAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i det angivna namn området, i kön eller i ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="35003-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="35003-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35003-111">EXAMPLES</span></span>

### <span data-ttu-id="35003-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35003-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="35003-113">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="35003-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="35003-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="35003-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="35003-115">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss kö.</span><span class="sxs-lookup"><span data-stu-id="35003-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="35003-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="35003-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="35003-117">Returnerar den angivna beskrivningen av auktoriseringsregeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="35003-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="35003-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="35003-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="35003-119">Returnerar den angivna beskrivningen för auktoriseringsregeln för en viss namnrymd och ett alias.</span><span class="sxs-lookup"><span data-stu-id="35003-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="35003-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35003-120">PARAMETERS</span></span>

### <span data-ttu-id="35003-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="35003-121">-AliasName</span></span>
<span data-ttu-id="35003-122">GeoDR konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="35003-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="35003-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35003-123">-DefaultProfile</span></span>
<span data-ttu-id="35003-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35003-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35003-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="35003-125">-Name</span></span>
<span data-ttu-id="35003-126">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="35003-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="35003-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="35003-127">-Namespace</span></span>
<span data-ttu-id="35003-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="35003-128">Namespace Name</span></span>

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

### <span data-ttu-id="35003-129">-Kö</span><span class="sxs-lookup"><span data-stu-id="35003-129">-Queue</span></span>
<span data-ttu-id="35003-130">Könamn</span><span class="sxs-lookup"><span data-stu-id="35003-130">Queue Name</span></span>

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

### <span data-ttu-id="35003-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35003-131">-ResourceGroupName</span></span>
<span data-ttu-id="35003-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="35003-132">Resource Group Name</span></span>

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

### <span data-ttu-id="35003-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="35003-133">-Topic</span></span>
<span data-ttu-id="35003-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="35003-134">Topic Name</span></span>

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

### <span data-ttu-id="35003-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35003-135">CommonParameters</span></span>
<span data-ttu-id="35003-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35003-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35003-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35003-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35003-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35003-138">INPUTS</span></span>

### <span data-ttu-id="35003-139">System. String</span><span class="sxs-lookup"><span data-stu-id="35003-139">System.String</span></span>

## <span data-ttu-id="35003-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35003-140">OUTPUTS</span></span>

### <span data-ttu-id="35003-141">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="35003-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="35003-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35003-142">NOTES</span></span>

## <span data-ttu-id="35003-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35003-143">RELATED LINKS</span></span>
