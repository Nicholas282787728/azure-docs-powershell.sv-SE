---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585620"
---
# <span data-ttu-id="0614a-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="0614a-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="0614a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0614a-102">SYNOPSIS</span></span>
<span data-ttu-id="0614a-103">Hämtar information om en enkel Event-hubb eller hämtar en lista över händelse nav.</span><span class="sxs-lookup"><span data-stu-id="0614a-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0614a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0614a-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="0614a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0614a-105">DESCRIPTION</span></span>
<span data-ttu-id="0614a-106">Get-AzureRmEventHub cmdlet returnerar antingen informationen om en Händelsehubben eller en lista över alla händelse nav i det aktuella namn området.</span><span class="sxs-lookup"><span data-stu-id="0614a-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="0614a-107">Om namnet på händelsehubben är angivet returneras informationen om en enskild Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="0614a-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="0614a-108">Om ett namn på en Händelsehubben inte anges returneras en lista över alla händelse nav i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="0614a-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="0614a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0614a-109">EXAMPLES</span></span>

### <span data-ttu-id="0614a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0614a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="0614a-111">Returnerar information om Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="0614a-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="0614a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0614a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="0614a-113">Returnerar en lista med händelse nav i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="0614a-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="0614a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0614a-114">PARAMETERS</span></span>

### <span data-ttu-id="0614a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0614a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0614a-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0614a-116">Resource group name.</span></span>

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

### <span data-ttu-id="0614a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0614a-117">-Name</span></span>
<span data-ttu-id="0614a-118">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="0614a-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0614a-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="0614a-119">-Namespace</span></span>
<span data-ttu-id="0614a-120">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="0614a-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="0614a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0614a-121">INPUTS</span></span>

### <span data-ttu-id="0614a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0614a-122">System.String</span></span>

## <span data-ttu-id="0614a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0614a-123">OUTPUTS</span></span>

### <span data-ttu-id="0614a-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. EventHubAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0614a-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0614a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0614a-125">NOTES</span></span>

## <span data-ttu-id="0614a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0614a-126">RELATED LINKS</span></span>

