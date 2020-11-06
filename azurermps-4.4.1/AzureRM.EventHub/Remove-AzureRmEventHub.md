---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585584"
---
# <span data-ttu-id="ce669-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="ce669-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="ce669-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce669-102">SYNOPSIS</span></span>
<span data-ttu-id="ce669-103">Tar bort den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ce669-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce669-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce669-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ce669-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce669-105">DESCRIPTION</span></span>
<span data-ttu-id="ce669-106">Remove-AzureRmEventHub cmdlet tar bort och tar bort den angivna händelsehubben från det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="ce669-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="ce669-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce669-107">EXAMPLES</span></span>

### <span data-ttu-id="ce669-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce669-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="ce669-109">Tar bort Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="ce669-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="ce669-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce669-110">PARAMETERS</span></span>

### <span data-ttu-id="ce669-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce669-111">-ResourceGroupName</span></span>
<span data-ttu-id="ce669-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ce669-112">Resource group name.</span></span>

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

### <span data-ttu-id="ce669-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce669-113">-Confirm</span></span>
<span data-ttu-id="ce669-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce669-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce669-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce669-115">-WhatIf</span></span>
<span data-ttu-id="ce669-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce669-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce669-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce669-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce669-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce669-118">-Name</span></span>
<span data-ttu-id="ce669-119">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="ce669-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce669-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ce669-120">-Namespace</span></span>
<span data-ttu-id="ce669-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ce669-121">Namespace Name.</span></span>

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

## <span data-ttu-id="ce669-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce669-122">INPUTS</span></span>

### <span data-ttu-id="ce669-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ce669-123">System.String</span></span>

## <span data-ttu-id="ce669-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce669-124">OUTPUTS</span></span>

### <span data-ttu-id="ce669-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce669-125">System.Object</span></span>

## <span data-ttu-id="ce669-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce669-126">NOTES</span></span>

## <span data-ttu-id="ce669-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce669-127">RELATED LINKS</span></span>

