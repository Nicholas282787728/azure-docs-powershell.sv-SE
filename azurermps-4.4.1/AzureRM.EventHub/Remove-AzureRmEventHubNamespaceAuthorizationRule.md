---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756350"
---
# <span data-ttu-id="0d35e-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0d35e-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="0d35e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d35e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d35e-103">Tar bort den angivna auktoriseringsregeln för de angivna namn rymderna för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="0d35e-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d35e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d35e-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0d35e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d35e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d35e-106">Remove-AzureRmEventHubNamespaceAuthorizationRule-cmdleten tar bort och tar bort den angivna auktoriseringsregeln i namn området för angivna händelse nav.</span><span class="sxs-lookup"><span data-stu-id="0d35e-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="0d35e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d35e-107">EXAMPLES</span></span>

### <span data-ttu-id="0d35e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d35e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="0d35e-109">Tar bort \` MyAuthRuleName \` från namn områdes \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="0d35e-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="0d35e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d35e-110">PARAMETERS</span></span>

### <span data-ttu-id="0d35e-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0d35e-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="0d35e-112">Namn på auktoriseringsregeln för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="0d35e-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="0d35e-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0d35e-113">-NamespaceName</span></span>
<span data-ttu-id="0d35e-114">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="0d35e-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="0d35e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d35e-115">-ResourceGroupName</span></span>
<span data-ttu-id="0d35e-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0d35e-116">Resource group name.</span></span>

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

### <span data-ttu-id="0d35e-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d35e-117">-Confirm</span></span>
<span data-ttu-id="0d35e-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d35e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d35e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d35e-119">-WhatIf</span></span>
<span data-ttu-id="0d35e-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d35e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d35e-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d35e-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0d35e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d35e-122">INPUTS</span></span>

### <span data-ttu-id="0d35e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0d35e-123">System.String</span></span>

## <span data-ttu-id="0d35e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d35e-124">OUTPUTS</span></span>

### <span data-ttu-id="0d35e-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d35e-125">System.Boolean</span></span>

## <span data-ttu-id="0d35e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d35e-126">NOTES</span></span>

## <span data-ttu-id="0d35e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d35e-127">RELATED LINKS</span></span>

