---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585588"
---
# <span data-ttu-id="525cf-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="525cf-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="525cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="525cf-102">SYNOPSIS</span></span>
<span data-ttu-id="525cf-103">Skapar en ny primär eller sekundär nycklar för auktoriseringsregeln för den angivna namn rymden för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="525cf-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="525cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="525cf-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="525cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="525cf-105">DESCRIPTION</span></span>
<span data-ttu-id="525cf-106">New-AzureRmEventHubNamespaceKey cmdlet återskapar den primära eller sekundära nyckeln för den angivna auktoriseringsregeln för den angivna verifierings namn området.</span><span class="sxs-lookup"><span data-stu-id="525cf-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="525cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="525cf-107">EXAMPLES</span></span>

### <span data-ttu-id="525cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="525cf-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="525cf-109">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` i \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="525cf-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="525cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="525cf-110">PARAMETERS</span></span>

### <span data-ttu-id="525cf-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="525cf-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="525cf-112">Namn på auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="525cf-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="525cf-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="525cf-113">-NamespaceName</span></span>
<span data-ttu-id="525cf-114">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="525cf-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="525cf-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="525cf-115">-RegenerateKeys</span></span>
<span data-ttu-id="525cf-116">För att återskapa: \` PrimaryKey \` eller \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="525cf-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="525cf-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="525cf-117">-ResourceGroup</span></span>
<span data-ttu-id="525cf-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="525cf-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="525cf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="525cf-119">-Confirm</span></span>
<span data-ttu-id="525cf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="525cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525cf-121">-WhatIf</span></span>
<span data-ttu-id="525cf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="525cf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="525cf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="525cf-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="525cf-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="525cf-124">INPUTS</span></span>

### <span data-ttu-id="525cf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="525cf-125">System.String</span></span>

## <span data-ttu-id="525cf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="525cf-126">OUTPUTS</span></span>

### <span data-ttu-id="525cf-127">Microsoft. Azure. commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="525cf-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="525cf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="525cf-128">NOTES</span></span>

## <span data-ttu-id="525cf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="525cf-129">RELATED LINKS</span></span>

