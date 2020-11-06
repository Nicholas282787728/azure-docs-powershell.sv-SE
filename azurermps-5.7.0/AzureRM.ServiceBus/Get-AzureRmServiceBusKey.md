---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: da2794fc390ecce13c466fc4ff2d2efb92205a8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575501"
---
# <span data-ttu-id="c2c6d-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c2c6d-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="c2c6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c6d-103">Hämtar primära och sekundära anslutnings strängar för ett namn område eller en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="c2c6d-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2c6d-104">SYNTAX</span></span>

### <span data-ttu-id="c2c6d-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2c6d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2c6d-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2c6d-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2c6d-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2c6d-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2c6d-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2c6d-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c6d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2c6d-109">DESCRIPTION</span></span>
<span data-ttu-id="c2c6d-110">Cmdleten **Get-AzureRmServiceBusKey** returnerar de primära och sekundära anslutnings strängarna för ett namn område, en kö eller ett ämne (GeoDR-konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="c2c6d-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="c2c6d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2c6d-111">EXAMPLES</span></span>

### <span data-ttu-id="c2c6d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2c6d-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="c2c6d-113">Primära och sekundära anslutnings strängar till det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="c2c6d-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c2c6d-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="c2c6d-115">Primära och sekundära anslutnings strängar till den angivna kön.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="c2c6d-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c2c6d-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="c2c6d-117">Primära och sekundära anslutnings strängar till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="c2c6d-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c2c6d-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="c2c6d-119">Primära och sekundära anslutnings strängar till det angivna namn området och aliaset.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="c2c6d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2c6d-120">PARAMETERS</span></span>

### <span data-ttu-id="c2c6d-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c2c6d-121">-AliasName</span></span>
<span data-ttu-id="c2c6d-122">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="c2c6d-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c6d-123">-DefaultProfile</span></span>
<span data-ttu-id="c2c6d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2c6d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2c6d-125">-Name</span></span>
<span data-ttu-id="c2c6d-126">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="c2c6d-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6d-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c2c6d-127">-Namespace</span></span>
<span data-ttu-id="c2c6d-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c2c6d-128">Namespace Name</span></span>

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

### <span data-ttu-id="c2c6d-129">-Kö</span><span class="sxs-lookup"><span data-stu-id="c2c6d-129">-Queue</span></span>
<span data-ttu-id="c2c6d-130">Könamn</span><span class="sxs-lookup"><span data-stu-id="c2c6d-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c6d-131">-ResourceGroupName</span></span>
<span data-ttu-id="c2c6d-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c2c6d-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6d-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="c2c6d-133">-Topic</span></span>
<span data-ttu-id="c2c6d-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="c2c6d-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c6d-135">CommonParameters</span></span>
<span data-ttu-id="c2c6d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c2c6d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c6d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c6d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2c6d-138">INPUTS</span></span>

### <span data-ttu-id="c2c6d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c2c6d-139">System.String</span></span>


## <span data-ttu-id="c2c6d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2c6d-140">OUTPUTS</span></span>

### <span data-ttu-id="c2c6d-141">Microsoft. Azure. commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c2c6d-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="c2c6d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2c6d-142">NOTES</span></span>

## <span data-ttu-id="c2c6d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2c6d-143">RELATED LINKS</span></span>
