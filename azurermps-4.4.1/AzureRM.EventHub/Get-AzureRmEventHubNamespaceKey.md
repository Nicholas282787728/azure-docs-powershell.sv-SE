---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585600"
---
# <span data-ttu-id="f5b93-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f5b93-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="f5b93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5b93-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b93-103">Hämtar information om primära, sekundära ConnectionString och nycklar för auktoriseringsregeln för den angivna auktoriseringsregeln för Event Hub namespace.</span><span class="sxs-lookup"><span data-stu-id="f5b93-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5b93-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="f5b93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5b93-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b93-106">Get-AzureRmEventHubNamespaceKey cmdlet returnerar den primära och sekundära ConnectionString och information om tangenterna för den angivna auktoriseringsregeln i det angivna namn området Event Hub.</span><span class="sxs-lookup"><span data-stu-id="f5b93-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="f5b93-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5b93-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b93-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5b93-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="f5b93-109">Hämtar information om primära, sekundära ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` på namn området för Event Hub- \` MyNamespaceName \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f5b93-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f5b93-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5b93-110">PARAMETERS</span></span>

### <span data-ttu-id="f5b93-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f5b93-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="f5b93-112">Namnet på auktoriseringsregeln i namn området Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="f5b93-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

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

### <span data-ttu-id="f5b93-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f5b93-113">-NamespaceName</span></span>
<span data-ttu-id="f5b93-114">Namn områdes namn för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="f5b93-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="f5b93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5b93-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5b93-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f5b93-116">Resource group name.</span></span>

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

## <span data-ttu-id="f5b93-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5b93-117">INPUTS</span></span>

### <span data-ttu-id="f5b93-118">System. String</span><span class="sxs-lookup"><span data-stu-id="f5b93-118">System.String</span></span>

## <span data-ttu-id="f5b93-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5b93-119">OUTPUTS</span></span>

### <span data-ttu-id="f5b93-120">Microsoft. Azure. commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f5b93-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="f5b93-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5b93-121">NOTES</span></span>

## <span data-ttu-id="f5b93-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5b93-122">RELATED LINKS</span></span>

