---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757460"
---
# <span data-ttu-id="6a138-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="6a138-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="6a138-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a138-102">SYNOPSIS</span></span>
<span data-ttu-id="6a138-103">Återskapar primära eller sekundära anslutnings strängar för Service Bus namn området eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="6a138-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a138-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a138-104">SYNTAX</span></span>

### <span data-ttu-id="6a138-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6a138-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a138-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a138-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a138-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a138-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a138-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a138-108">DESCRIPTION</span></span>
<span data-ttu-id="6a138-109">**New-AzureRmServiceBusKey-** cmdleten skapar nya primära eller sekundära anslutnings strängar för det angivna namn området eller kön eller ämnet och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="6a138-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="6a138-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a138-110">EXAMPLES</span></span>

### <span data-ttu-id="6a138-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a138-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="6a138-112">Återskapar primära eller sekundära anslutnings strängar för namn området.</span><span class="sxs-lookup"><span data-stu-id="6a138-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="6a138-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6a138-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="6a138-114">Återskapar primära eller sekundära anslutnings strängar för kön.</span><span class="sxs-lookup"><span data-stu-id="6a138-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="6a138-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6a138-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="6a138-116">Återskapar de primära eller sekundära anslutnings strängarna för ämnet.</span><span class="sxs-lookup"><span data-stu-id="6a138-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="6a138-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a138-117">PARAMETERS</span></span>

### <span data-ttu-id="6a138-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a138-118">-Confirm</span></span>
<span data-ttu-id="6a138-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a138-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a138-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a138-120">-Name</span></span>
<span data-ttu-id="6a138-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="6a138-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6a138-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6a138-122">-Namespace</span></span>
<span data-ttu-id="6a138-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="6a138-123">Namespace Name.</span></span>

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

### <span data-ttu-id="6a138-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="6a138-124">-Queue</span></span>
<span data-ttu-id="6a138-125">Könamn.</span><span class="sxs-lookup"><span data-stu-id="6a138-125">Queue Name.</span></span>

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

### <span data-ttu-id="6a138-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6a138-126">-RegenerateKey</span></span>
<span data-ttu-id="6a138-127">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="6a138-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a138-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a138-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a138-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6a138-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6a138-130">-Ämne</span><span class="sxs-lookup"><span data-stu-id="6a138-130">-Topic</span></span>
<span data-ttu-id="6a138-131">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="6a138-131">Topic Name.</span></span>

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

### <span data-ttu-id="6a138-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a138-132">-WhatIf</span></span>
<span data-ttu-id="6a138-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a138-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a138-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a138-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a138-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a138-135">-DefaultProfile</span></span>
<span data-ttu-id="6a138-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a138-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a138-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a138-137">CommonParameters</span></span>
<span data-ttu-id="6a138-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a138-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a138-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a138-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a138-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a138-140">INPUTS</span></span>

### <span data-ttu-id="6a138-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6a138-141">System.String</span></span>

## <span data-ttu-id="6a138-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a138-142">OUTPUTS</span></span>

### <span data-ttu-id="6a138-143">Microsoft. Azure. commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6a138-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="6a138-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a138-144">NOTES</span></span>

## <span data-ttu-id="6a138-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a138-145">RELATED LINKS</span></span>

