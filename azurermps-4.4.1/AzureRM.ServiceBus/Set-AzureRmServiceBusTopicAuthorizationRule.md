---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757456"
---
# <span data-ttu-id="0fd97-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0fd97-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="0fd97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd97-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd97-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="0fd97-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd97-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd97-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd97-106">Cmdleten **set-AzureRmServiceBusTopicAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="0fd97-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="0fd97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd97-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd97-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fd97-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="0fd97-109">Lägger **till behörigheter för** behörighets regeln `SBTopicAuthoRule1` i avsnittet `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="0fd97-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="0fd97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd97-110">PARAMETERS</span></span>

### <span data-ttu-id="0fd97-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0fd97-111">-ResourceGroup</span></span>
<span data-ttu-id="0fd97-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fd97-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fd97-113">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="0fd97-113">-Rights</span></span>
<span data-ttu-id="0fd97-114">Behörighet till exempel @ ("lyssna", "Skicka", "hantera").</span><span class="sxs-lookup"><span data-stu-id="0fd97-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="0fd97-115">Obligatoriskt om **-AuthruleObj** inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="0fd97-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fd97-116">-Confirm</span></span>
<span data-ttu-id="0fd97-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fd97-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd97-118">-WhatIf</span></span>
<span data-ttu-id="0fd97-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fd97-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd97-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fd97-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd97-121">-DefaultProfile</span></span>
<span data-ttu-id="0fd97-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd97-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd97-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="0fd97-123">-InputObj</span></span>
<span data-ttu-id="0fd97-124">ServiceBus ämne AuthorizationRule objekt.</span><span class="sxs-lookup"><span data-stu-id="0fd97-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fd97-125">-Name</span></span>
<span data-ttu-id="0fd97-126">AuthorizationRule-namn – obligatoriskt om ' AuthruleObj ' inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="0fd97-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="0fd97-127">-Namespace</span></span>
<span data-ttu-id="0fd97-128">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="0fd97-128">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-129">-Ämne</span><span class="sxs-lookup"><span data-stu-id="0fd97-129">-Topic</span></span>
<span data-ttu-id="0fd97-130">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="0fd97-130">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd97-131">CommonParameters</span></span>
<span data-ttu-id="0fd97-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd97-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd97-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd97-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd97-134">INPUTS</span></span>

### <span data-ttu-id="0fd97-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0fd97-135">-ResourceGroup</span></span>
 <span data-ttu-id="0fd97-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd97-136">System.String</span></span>

### <span data-ttu-id="0fd97-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0fd97-137">-NamespaceName</span></span>
 <span data-ttu-id="0fd97-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd97-138">System.String</span></span>

### <span data-ttu-id="0fd97-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0fd97-139">-TopicName</span></span>
 <span data-ttu-id="0fd97-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd97-140">System.String</span></span>

### <span data-ttu-id="0fd97-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="0fd97-141">-AuthRuleObj</span></span>
 <span data-ttu-id="0fd97-142">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0fd97-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0fd97-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd97-143">OUTPUTS</span></span>

### <span data-ttu-id="0fd97-144">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0fd97-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="0fd97-145">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization-regler/SBTopicAuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: West US-Taggar: rättigheter: {avlyssna, skicka, hantera}</span><span class="sxs-lookup"><span data-stu-id="0fd97-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="0fd97-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd97-146">NOTES</span></span>

## <span data-ttu-id="0fd97-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd97-147">RELATED LINKS</span></span>

