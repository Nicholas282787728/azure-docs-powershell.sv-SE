---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586528"
---
# <span data-ttu-id="a5d83-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5d83-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a5d83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5d83-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d83-103">Uppdaterar auktoriseringsregeln för de angivna namn rymderna för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="a5d83-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5d83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5d83-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a5d83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5d83-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d83-106">Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet uppdaterar auktoriseringsregeln för de angivna namn rymderna för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="a5d83-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a5d83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5d83-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d83-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5d83-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="a5d83-109">Uppdaterar \` MyAuthRuleName \` för auktoriseringsregler för att ge behörighet hantera rättigheter.</span><span class="sxs-lookup"><span data-stu-id="a5d83-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="a5d83-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5d83-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d83-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a5d83-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a5d83-112">Namn på auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="a5d83-112">The authorization rule name.</span></span>
<span data-ttu-id="a5d83-113">Obligatoriskt om-AuthruleObj inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="a5d83-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d83-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a5d83-114">-AuthRuleObj</span></span>
<span data-ttu-id="a5d83-115">Principobjektet för auktoriseringsregler för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="a5d83-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d83-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a5d83-116">-NamespaceName</span></span>
<span data-ttu-id="a5d83-117">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="a5d83-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d83-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d83-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5d83-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a5d83-119">Resource group name.</span></span>

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

### <span data-ttu-id="a5d83-120">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="a5d83-120">-Rights</span></span>
<span data-ttu-id="a5d83-121">Obligatoriskt om-AuthruleObj inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="a5d83-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="a5d83-122">Behörighet till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="a5d83-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d83-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5d83-123">-Confirm</span></span>
<span data-ttu-id="a5d83-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5d83-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d83-125">-WhatIf</span></span>
<span data-ttu-id="a5d83-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5d83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d83-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5d83-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a5d83-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5d83-128">INPUTS</span></span>

### <span data-ttu-id="a5d83-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d83-129">System.String</span></span>

## <span data-ttu-id="a5d83-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5d83-130">OUTPUTS</span></span>

### <span data-ttu-id="a5d83-131">Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a5d83-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a5d83-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5d83-132">NOTES</span></span>

## <span data-ttu-id="a5d83-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5d83-133">RELATED LINKS</span></span>

