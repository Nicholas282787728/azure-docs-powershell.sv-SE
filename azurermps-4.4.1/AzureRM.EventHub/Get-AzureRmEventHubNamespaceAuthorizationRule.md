---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758086"
---
# <span data-ttu-id="52e23-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="52e23-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="52e23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52e23-102">SYNOPSIS</span></span>
<span data-ttu-id="52e23-103">Hämtar information om en auktoriseringsregel för Eventubs, eller hämtar en lista över auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="52e23-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52e23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52e23-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="52e23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52e23-105">DESCRIPTION</span></span>
<span data-ttu-id="52e23-106">Get-AzureRmEventHubNamespaceAuthorizationRule-cmdleten får antingen information om en angiven regel för en namnrymd eller en lista över auktoriseringsregler för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="52e23-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="52e23-107">Om namnet på auktoriseringsregeln anges returneras informationen om en enda auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="52e23-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="52e23-108">Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler i namn området.</span><span class="sxs-lookup"><span data-stu-id="52e23-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="52e23-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52e23-109">EXAMPLES</span></span>

### <span data-ttu-id="52e23-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52e23-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="52e23-111">Returnerar \` MyAuthRuleName \` i \` MyNamespaceName \` , med resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="52e23-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="52e23-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52e23-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="52e23-113">Returnerar standard regeln för \` RootManageSharedAccessKey \` i namn området för Event Hubs \` \` , med resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="52e23-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="52e23-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="52e23-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="52e23-115">Returnerar alla auktoriseringsregler i MyNamespaceName för Event Hubs \` \` , med resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="52e23-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="52e23-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52e23-116">PARAMETERS</span></span>

### <span data-ttu-id="52e23-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="52e23-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="52e23-118">Namn på auktoriseringsregeln för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="52e23-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e23-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="52e23-119">-NamespaceName</span></span>
<span data-ttu-id="52e23-120">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="52e23-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="52e23-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e23-121">-ResourceGroupName</span></span>
<span data-ttu-id="52e23-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="52e23-122">Resource group name.</span></span>

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

## <span data-ttu-id="52e23-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52e23-123">INPUTS</span></span>

### <span data-ttu-id="52e23-124">System. String</span><span class="sxs-lookup"><span data-stu-id="52e23-124">System.String</span></span>

## <span data-ttu-id="52e23-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52e23-125">OUTPUTS</span></span>

### <span data-ttu-id="52e23-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="52e23-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="52e23-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52e23-127">NOTES</span></span>

## <span data-ttu-id="52e23-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52e23-128">RELATED LINKS</span></span>

