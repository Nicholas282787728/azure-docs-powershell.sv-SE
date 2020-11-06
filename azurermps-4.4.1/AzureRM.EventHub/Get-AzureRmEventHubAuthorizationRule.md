---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585616"
---
# <span data-ttu-id="aa04a-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aa04a-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="aa04a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa04a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa04a-103">Hämtar information om en auktoriseringsregel eller hämtar en lista över auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="aa04a-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa04a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa04a-104">SYNTAX</span></span>

### <span data-ttu-id="aa04a-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aa04a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="aa04a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa04a-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="aa04a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa04a-107">DESCRIPTION</span></span>
<span data-ttu-id="aa04a-108">Get-AzureRmEventHubAuthorizationRule-cmdleten får antingen information om en auktoriseringsregel eller en lista över alla auktoriseringsregler för en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="aa04a-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="aa04a-109">Om namnet på en auktoriseringsregel tillhandahålls returneras informationen om den enskilda auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="aa04a-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="aa04a-110">Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="aa04a-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="aa04a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa04a-111">EXAMPLES</span></span>

### <span data-ttu-id="aa04a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa04a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="aa04a-113">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i \` MyEventHubName \` som befinner sig i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="aa04a-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="aa04a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="aa04a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="aa04a-115">Hämtar en lista över alla auktoriseringsregler i \` MyEventHubName, som besvaras \` av namn områdes \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="aa04a-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="aa04a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa04a-116">PARAMETERS</span></span>

### <span data-ttu-id="aa04a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa04a-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa04a-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="aa04a-118">Resource group name.</span></span>

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

### <span data-ttu-id="aa04a-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="aa04a-119">-Eventhub</span></span>
<span data-ttu-id="aa04a-120">Namn på Eventhub.</span><span class="sxs-lookup"><span data-stu-id="aa04a-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="aa04a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa04a-121">-Name</span></span>
<span data-ttu-id="aa04a-122">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="aa04a-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa04a-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="aa04a-123">-Namespace</span></span>
<span data-ttu-id="aa04a-124">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="aa04a-124">Namespace Name.</span></span>

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

## <span data-ttu-id="aa04a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa04a-125">INPUTS</span></span>

### <span data-ttu-id="aa04a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="aa04a-126">System.String</span></span>

## <span data-ttu-id="aa04a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa04a-127">OUTPUTS</span></span>

### <span data-ttu-id="aa04a-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aa04a-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aa04a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa04a-129">NOTES</span></span>

## <span data-ttu-id="aa04a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa04a-130">RELATED LINKS</span></span>

