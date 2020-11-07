---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756607"
---
# <span data-ttu-id="cf601-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf601-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="cf601-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf601-102">SYNOPSIS</span></span>
<span data-ttu-id="cf601-103">Skapar en ny auktoriseringsregel för Event Hub för namn område eller eventhub.</span><span class="sxs-lookup"><span data-stu-id="cf601-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf601-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf601-104">SYNTAX</span></span>

### <span data-ttu-id="cf601-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cf601-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cf601-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cf601-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cf601-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf601-107">DESCRIPTION</span></span>
<span data-ttu-id="cf601-108">New-AzureRmEventHubAuthorizationRule-cmdleten skapar en ny auktoriseringsregel för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="cf601-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="cf601-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf601-109">EXAMPLES</span></span>

### <span data-ttu-id="cf601-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cf601-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="cf601-111">Skapar en auktoriseringsregel \` MyAuthRuleName \` tilldelar lyssnar och skickar rättigheter till namn områdets \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cf601-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cf601-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cf601-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="cf601-113">Skapar en auktoriseringsregel \` för MyAuthRuleName \` bevilja lyssnings-och behörighets rättigheter till \` MyEventHubName \` i namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cf601-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cf601-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf601-114">PARAMETERS</span></span>

### <span data-ttu-id="cf601-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf601-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf601-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cf601-116">Resource group name.</span></span>

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

### <span data-ttu-id="cf601-117">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="cf601-117">-Rights</span></span>
<span data-ttu-id="cf601-118">Behörighet till exempel @ ("lyssna", "Skicka", "hantera").</span><span class="sxs-lookup"><span data-stu-id="cf601-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf601-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf601-119">-Confirm</span></span>
<span data-ttu-id="cf601-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf601-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf601-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf601-121">-WhatIf</span></span>
<span data-ttu-id="cf601-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf601-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf601-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf601-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf601-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cf601-124">-EventHub</span></span>
<span data-ttu-id="cf601-125">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="cf601-125">EventHub Name.</span></span>

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

### <span data-ttu-id="cf601-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf601-126">-Name</span></span>
<span data-ttu-id="cf601-127">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="cf601-127">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="cf601-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="cf601-128">-Namespace</span></span>
<span data-ttu-id="cf601-129">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="cf601-129">Namespace Name.</span></span>

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

## <span data-ttu-id="cf601-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf601-130">INPUTS</span></span>

### <span data-ttu-id="cf601-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cf601-131">System.String</span></span>

## <span data-ttu-id="cf601-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf601-132">OUTPUTS</span></span>

### <span data-ttu-id="cf601-133">Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cf601-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cf601-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf601-134">NOTES</span></span>

## <span data-ttu-id="cf601-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf601-135">RELATED LINKS</span></span>

