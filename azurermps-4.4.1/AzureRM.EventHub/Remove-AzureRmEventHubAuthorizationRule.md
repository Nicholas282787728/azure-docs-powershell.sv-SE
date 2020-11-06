---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585583"
---
# <span data-ttu-id="7d6f6-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d6f6-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7d6f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6f6-103">Tar bort den angivna auktoriseringsregeln för Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d6f6-104">SYNTAX</span></span>

### <span data-ttu-id="7d6f6-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7d6f6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7d6f6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d6f6-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7d6f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d6f6-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6f6-108">Remove-AzureRmEventHubAuthorizationRule-cmdleten tar bort och tar bort den angivna auktoriseringsregeln från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="7d6f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d6f6-109">EXAMPLES</span></span>

### <span data-ttu-id="7d6f6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d6f6-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="7d6f6-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7d6f6-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="7d6f6-112">Tar bort \` MyAuthRuleName från händelsehubben \` \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="7d6f6-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="7d6f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d6f6-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6f6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6f6-114">-ResourceGroupName</span></span>
<span data-ttu-id="7d6f6-115">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-115">Resource group name.</span></span>

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

### <span data-ttu-id="7d6f6-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d6f6-116">-Confirm</span></span>
<span data-ttu-id="7d6f6-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6f6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6f6-118">-WhatIf</span></span>
<span data-ttu-id="7d6f6-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6f6-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6f6-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7d6f6-121">-EventHub</span></span>
<span data-ttu-id="7d6f6-122">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-122">EventHub Name.</span></span>

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

### <span data-ttu-id="7d6f6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7d6f6-123">-Force</span></span>
<span data-ttu-id="7d6f6-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f6-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d6f6-125">-Name</span></span>
<span data-ttu-id="7d6f6-126">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7d6f6-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="7d6f6-127">-Namespace</span></span>
<span data-ttu-id="7d6f6-128">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-128">Namespace Name.</span></span>

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

### <span data-ttu-id="7d6f6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d6f6-129">-PassThru</span></span>
<span data-ttu-id="7d6f6-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7d6f6-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="7d6f6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d6f6-131">INPUTS</span></span>

### <span data-ttu-id="7d6f6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7d6f6-132">System.String</span></span>

## <span data-ttu-id="7d6f6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d6f6-133">OUTPUTS</span></span>

### <span data-ttu-id="7d6f6-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d6f6-134">System.Boolean</span></span>

## <span data-ttu-id="7d6f6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d6f6-135">NOTES</span></span>

## <span data-ttu-id="7d6f6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d6f6-136">RELATED LINKS</span></span>

