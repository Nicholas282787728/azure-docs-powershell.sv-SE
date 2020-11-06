---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584532"
---
# <span data-ttu-id="87c1c-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87c1c-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="87c1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="87c1c-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="87c1c-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87c1c-104">SYNTAX</span></span>

### <span data-ttu-id="87c1c-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="87c1c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c1c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="87c1c-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c1c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="87c1c-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c1c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87c1c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c1c-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="87c1c-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c1c-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87c1c-110">DESCRIPTION</span></span>
<span data-ttu-id="87c1c-111">Cmdleten **set-AzureRmServiceBusAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln i ett angivet Service Bus-namnområde eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="87c1c-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="87c1c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87c1c-112">EXAMPLES</span></span>

### <span data-ttu-id="87c1c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87c1c-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="87c1c-114">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="87c1c-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="87c1c-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="87c1c-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="87c1c-116">Tar **bort** behörigheter från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i kö `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="87c1c-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="87c1c-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="87c1c-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="87c1c-118">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i avsnittet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="87c1c-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="87c1c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87c1c-119">PARAMETERS</span></span>

### <span data-ttu-id="87c1c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87c1c-120">-Confirm</span></span>
<span data-ttu-id="87c1c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87c1c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c1c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87c1c-122">-InputObject</span></span>
<span data-ttu-id="87c1c-123">ServiceBus AuthorizationRule-objekt.</span><span class="sxs-lookup"><span data-stu-id="87c1c-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87c1c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="87c1c-124">-Name</span></span>
<span data-ttu-id="87c1c-125">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="87c1c-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="87c1c-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="87c1c-126">-Namespace</span></span>
<span data-ttu-id="87c1c-127">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="87c1c-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c1c-128">-Kö</span><span class="sxs-lookup"><span data-stu-id="87c1c-128">-Queue</span></span>
<span data-ttu-id="87c1c-129">Könamn.</span><span class="sxs-lookup"><span data-stu-id="87c1c-129">Queue Name.</span></span>

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

### <span data-ttu-id="87c1c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c1c-130">-ResourceGroupName</span></span>
<span data-ttu-id="87c1c-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="87c1c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="87c1c-132">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="87c1c-132">-Rights</span></span>
<span data-ttu-id="87c1c-133">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="87c1c-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c1c-134">-Ämne</span><span class="sxs-lookup"><span data-stu-id="87c1c-134">-Topic</span></span>
<span data-ttu-id="87c1c-135">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="87c1c-135">Topic Name.</span></span>

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

### <span data-ttu-id="87c1c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c1c-136">-WhatIf</span></span>
<span data-ttu-id="87c1c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87c1c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c1c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87c1c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c1c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c1c-139">-DefaultProfile</span></span>
<span data-ttu-id="87c1c-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87c1c-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c1c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c1c-141">CommonParameters</span></span>
<span data-ttu-id="87c1c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c1c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c1c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c1c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c1c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87c1c-144">INPUTS</span></span>

### <span data-ttu-id="87c1c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87c1c-145">System.String</span></span>
<span data-ttu-id="87c1c-146">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes system. string []</span><span class="sxs-lookup"><span data-stu-id="87c1c-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="87c1c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87c1c-147">OUTPUTS</span></span>

### <span data-ttu-id="87c1c-148">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="87c1c-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="87c1c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87c1c-149">NOTES</span></span>

## <span data-ttu-id="87c1c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87c1c-150">RELATED LINKS</span></span>

