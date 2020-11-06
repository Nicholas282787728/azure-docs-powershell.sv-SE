---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0dc0e2ebf22d995577abd37e2eef2b16b0ea4001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580988"
---
# <span data-ttu-id="ccdde-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="ccdde-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="ccdde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccdde-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdde-103">Återskapar primära eller sekundära anslutnings strängar för Service Bus namn området eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="ccdde-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccdde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccdde-104">SYNTAX</span></span>

### <span data-ttu-id="ccdde-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ccdde-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdde-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ccdde-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdde-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ccdde-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdde-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccdde-108">DESCRIPTION</span></span>
<span data-ttu-id="ccdde-109">**New-AzureRmServiceBusKey-** cmdleten skapar nya primära eller sekundära anslutnings strängar för det angivna namn området eller kön eller ämnet och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="ccdde-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="ccdde-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccdde-110">EXAMPLES</span></span>

### <span data-ttu-id="ccdde-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ccdde-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ccdde-112">Återskapar primära eller sekundära anslutnings strängar för namn området.</span><span class="sxs-lookup"><span data-stu-id="ccdde-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="ccdde-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ccdde-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ccdde-114">Återskapar primära eller sekundära anslutnings strängar för kön.</span><span class="sxs-lookup"><span data-stu-id="ccdde-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="ccdde-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ccdde-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ccdde-116">Återskapar de primära eller sekundära anslutnings strängarna för ämnet.</span><span class="sxs-lookup"><span data-stu-id="ccdde-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="ccdde-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccdde-117">PARAMETERS</span></span>

### <span data-ttu-id="ccdde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdde-118">-DefaultProfile</span></span>
<span data-ttu-id="ccdde-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccdde-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccdde-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccdde-120">-Name</span></span>
<span data-ttu-id="ccdde-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="ccdde-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ccdde-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ccdde-122">-Namespace</span></span>
<span data-ttu-id="ccdde-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ccdde-123">Namespace Name</span></span>

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

### <span data-ttu-id="ccdde-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="ccdde-124">-Queue</span></span>
<span data-ttu-id="ccdde-125">Könamn</span><span class="sxs-lookup"><span data-stu-id="ccdde-125">Queue Name</span></span>

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

### <span data-ttu-id="ccdde-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ccdde-126">-RegenerateKey</span></span>
<span data-ttu-id="ccdde-127">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="ccdde-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdde-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdde-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccdde-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ccdde-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ccdde-130">-Ämne</span><span class="sxs-lookup"><span data-stu-id="ccdde-130">-Topic</span></span>
<span data-ttu-id="ccdde-131">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="ccdde-131">Topic Name</span></span>

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

### <span data-ttu-id="ccdde-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ccdde-132">-Confirm</span></span>
<span data-ttu-id="ccdde-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccdde-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdde-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdde-134">-WhatIf</span></span>
<span data-ttu-id="ccdde-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ccdde-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdde-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ccdde-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdde-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdde-137">CommonParameters</span></span>
<span data-ttu-id="ccdde-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdde-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ccdde-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdde-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdde-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccdde-140">INPUTS</span></span>

### <span data-ttu-id="ccdde-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ccdde-141">System.String</span></span>


## <span data-ttu-id="ccdde-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccdde-142">OUTPUTS</span></span>

### <span data-ttu-id="ccdde-143">Microsoft. Azure. commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ccdde-143">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="ccdde-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccdde-144">NOTES</span></span>

## <span data-ttu-id="ccdde-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccdde-145">RELATED LINKS</span></span>
