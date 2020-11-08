---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269106"
---
# <span data-ttu-id="70eee-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="70eee-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="70eee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70eee-102">SYNOPSIS</span></span>
<span data-ttu-id="70eee-103">Hämtar primära och sekundära anslutnings strängar för ett namn område eller en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="70eee-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="70eee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70eee-104">SYNTAX</span></span>

### <span data-ttu-id="70eee-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70eee-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70eee-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70eee-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70eee-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70eee-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70eee-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="70eee-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70eee-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70eee-109">DESCRIPTION</span></span>
<span data-ttu-id="70eee-110">Cmdleten **Get-AzServiceBusKey** returnerar de primära och sekundära anslutnings strängarna för ett namn område, en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="70eee-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="70eee-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70eee-111">EXAMPLES</span></span>

### <span data-ttu-id="70eee-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70eee-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="70eee-113">Primära och sekundära anslutnings strängar till det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="70eee-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="70eee-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="70eee-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="70eee-115">Primära och sekundära anslutnings strängar till den angivna kön.</span><span class="sxs-lookup"><span data-stu-id="70eee-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="70eee-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="70eee-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="70eee-117">Primära och sekundära anslutnings strängar till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="70eee-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="70eee-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="70eee-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="70eee-119">Primära och sekundära anslutnings strängar till det angivna namn området och aliaset.</span><span class="sxs-lookup"><span data-stu-id="70eee-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="70eee-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70eee-120">PARAMETERS</span></span>

### <span data-ttu-id="70eee-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="70eee-121">-AliasName</span></span>
<span data-ttu-id="70eee-122">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="70eee-122">Alias Name</span></span>

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

### <span data-ttu-id="70eee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70eee-123">-DefaultProfile</span></span>
<span data-ttu-id="70eee-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70eee-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70eee-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="70eee-125">-Name</span></span>
<span data-ttu-id="70eee-126">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="70eee-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="70eee-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="70eee-127">-Namespace</span></span>
<span data-ttu-id="70eee-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="70eee-128">Namespace Name</span></span>

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

### <span data-ttu-id="70eee-129">-Kö</span><span class="sxs-lookup"><span data-stu-id="70eee-129">-Queue</span></span>
<span data-ttu-id="70eee-130">Könamn</span><span class="sxs-lookup"><span data-stu-id="70eee-130">Queue Name</span></span>

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

### <span data-ttu-id="70eee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70eee-131">-ResourceGroupName</span></span>
<span data-ttu-id="70eee-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="70eee-132">Resource Group Name</span></span>

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

### <span data-ttu-id="70eee-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="70eee-133">-Topic</span></span>
<span data-ttu-id="70eee-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="70eee-134">Topic Name</span></span>

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

### <span data-ttu-id="70eee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70eee-135">CommonParameters</span></span>
<span data-ttu-id="70eee-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70eee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70eee-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70eee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70eee-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70eee-138">INPUTS</span></span>

### <span data-ttu-id="70eee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70eee-139">System.String</span></span>

## <span data-ttu-id="70eee-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70eee-140">OUTPUTS</span></span>

### <span data-ttu-id="70eee-141">Microsoft. Azure. commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="70eee-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="70eee-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70eee-142">NOTES</span></span>

## <span data-ttu-id="70eee-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70eee-143">RELATED LINKS</span></span>
