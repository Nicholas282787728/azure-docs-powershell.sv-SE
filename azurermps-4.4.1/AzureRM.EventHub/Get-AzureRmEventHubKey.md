---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585611"
---
# <span data-ttu-id="b30c8-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="b30c8-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="b30c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b30c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b30c8-103">Hämtar primär nyckelinformation för de angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="b30c8-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b30c8-104">SYNTAX</span></span>

### <span data-ttu-id="b30c8-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b30c8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="b30c8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b30c8-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="b30c8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b30c8-107">DESCRIPTION</span></span>
<span data-ttu-id="b30c8-108">Get-AzureRmEventHubKey cmdlet returnerar primära och sekundära ConnectionString och nycklar med de angivna reglerna för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="b30c8-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b30c8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b30c8-109">EXAMPLES</span></span>

### <span data-ttu-id="b30c8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b30c8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="b30c8-111">Hämtar information om primära och sekundära ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b30c8-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="b30c8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b30c8-112">PARAMETERS</span></span>

### <span data-ttu-id="b30c8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30c8-113">-ResourceGroupName</span></span>
<span data-ttu-id="b30c8-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b30c8-114">Resource group name.</span></span>

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

### <span data-ttu-id="b30c8-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b30c8-115">-EventHub</span></span>
<span data-ttu-id="b30c8-116">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="b30c8-116">EventHub Name.</span></span>

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

### <span data-ttu-id="b30c8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b30c8-117">-Name</span></span>
<span data-ttu-id="b30c8-118">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="b30c8-118">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b30c8-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b30c8-119">-Namespace</span></span>
<span data-ttu-id="b30c8-120">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b30c8-120">Namespace Name.</span></span>

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

## <span data-ttu-id="b30c8-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b30c8-121">INPUTS</span></span>

### <span data-ttu-id="b30c8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b30c8-122">System.String</span></span>

## <span data-ttu-id="b30c8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b30c8-123">OUTPUTS</span></span>

### <span data-ttu-id="b30c8-124">Microsoft. Azure. commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b30c8-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="b30c8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b30c8-125">NOTES</span></span>

## <span data-ttu-id="b30c8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b30c8-126">RELATED LINKS</span></span>

