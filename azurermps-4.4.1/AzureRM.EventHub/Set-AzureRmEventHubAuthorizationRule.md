---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580620"
---
# <span data-ttu-id="d699a-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d699a-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="d699a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d699a-102">SYNOPSIS</span></span>
<span data-ttu-id="d699a-103">Uppdaterar den angivna auktoriseringsregeln i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="d699a-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d699a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d699a-104">SYNTAX</span></span>

### <span data-ttu-id="d699a-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d699a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d699a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d699a-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d699a-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d699a-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d699a-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d699a-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="d699a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d699a-109">DESCRIPTION</span></span>
<span data-ttu-id="d699a-110">Set-AzureRmEventHubAuthorizationRule cmdlet uppdaterar den angivna auktoriseringsregeln för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="d699a-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="d699a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d699a-111">EXAMPLES</span></span>

### <span data-ttu-id="d699a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d699a-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="d699a-113">Uppdaterar \` MyAuthRuleName \` för att bevilja behörighet att hantera behörigheter till MyEventHubName för Event Hub som bevaras \` \` av namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="d699a-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="d699a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d699a-114">PARAMETERS</span></span>

### <span data-ttu-id="d699a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d699a-115">-ResourceGroupName</span></span>
<span data-ttu-id="d699a-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d699a-116">Resource group name.</span></span>

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

### <span data-ttu-id="d699a-117">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="d699a-117">-Rights</span></span>
<span data-ttu-id="d699a-118">Obligatoriskt om ' AuthruleObj ' inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="d699a-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="d699a-119">Behörighet till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="d699a-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d699a-120">-Confirm</span></span>
<span data-ttu-id="d699a-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d699a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d699a-122">-WhatIf</span></span>
<span data-ttu-id="d699a-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d699a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d699a-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d699a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d699a-125">-EventHub</span></span>
<span data-ttu-id="d699a-126">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="d699a-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d699a-127">-InputObject</span></span>
<span data-ttu-id="d699a-128">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="d699a-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="d699a-129">-Name</span></span>
<span data-ttu-id="d699a-130">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="d699a-130">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d699a-131">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d699a-131">-Namespace</span></span>
<span data-ttu-id="d699a-132">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="d699a-132">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d699a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d699a-133">INPUTS</span></span>

### <span data-ttu-id="d699a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d699a-134">System.String</span></span>

## <span data-ttu-id="d699a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d699a-135">OUTPUTS</span></span>

### <span data-ttu-id="d699a-136">Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d699a-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d699a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d699a-137">NOTES</span></span>

## <span data-ttu-id="d699a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d699a-138">RELATED LINKS</span></span>

