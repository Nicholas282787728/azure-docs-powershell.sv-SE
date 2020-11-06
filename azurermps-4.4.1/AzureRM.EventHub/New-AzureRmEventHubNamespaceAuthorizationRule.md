---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585592"
---
# <span data-ttu-id="4cccf-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4cccf-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4cccf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cccf-102">SYNOPSIS</span></span>
<span data-ttu-id="4cccf-103">Skapar en ny auktoriseringsregel i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="4cccf-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cccf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cccf-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4cccf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cccf-105">DESCRIPTION</span></span>
<span data-ttu-id="4cccf-106">New-AzureRmEventHubNamespaceAuthorizationRule-cmdleten skapar en ny auktoriseringsregel i namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="4cccf-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4cccf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cccf-107">EXAMPLES</span></span>

### <span data-ttu-id="4cccf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4cccf-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="4cccf-109">Skapar \` MyAuthRuleName \` med lyssnings-och skicka rättigheter för namn områdes MyNamespaceName för Event Hubs \` \` , i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4cccf-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4cccf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cccf-110">PARAMETERS</span></span>

### <span data-ttu-id="4cccf-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4cccf-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="4cccf-112">Namn på auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="4cccf-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cccf-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4cccf-113">-NamespaceName</span></span>
<span data-ttu-id="4cccf-114">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="4cccf-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="4cccf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cccf-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cccf-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4cccf-116">Resource group name.</span></span>

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

### <span data-ttu-id="4cccf-117">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="4cccf-117">-Rights</span></span>
<span data-ttu-id="4cccf-118">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="4cccf-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cccf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cccf-119">-Confirm</span></span>
<span data-ttu-id="4cccf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cccf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cccf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cccf-121">-WhatIf</span></span>
<span data-ttu-id="4cccf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cccf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cccf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cccf-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4cccf-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cccf-124">INPUTS</span></span>

### <span data-ttu-id="4cccf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4cccf-125">System.String</span></span>

## <span data-ttu-id="4cccf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cccf-126">OUTPUTS</span></span>

### <span data-ttu-id="4cccf-127">Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4cccf-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4cccf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cccf-128">NOTES</span></span>

## <span data-ttu-id="4cccf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cccf-129">RELATED LINKS</span></span>

