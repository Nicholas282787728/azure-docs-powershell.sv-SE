---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580627"
---
# <span data-ttu-id="ef1f3-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ef1f3-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="ef1f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1f3-103">Tar bort det angivna namn området för Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef1f3-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ef1f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1f3-106">Remove-AzureRmEventHubNamespace-cmdleten tar bort och tar bort det angivna namn området för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ef1f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="ef1f3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef1f3-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="ef1f3-109">Tar bort namn områdes \` MyNamespaceName \` för Event Hub i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ef1f3-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ef1f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="ef1f3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1f3-111">-ResourceGroupName</span></span>
<span data-ttu-id="ef1f3-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-112">Resource group name.</span></span>

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

### <span data-ttu-id="ef1f3-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef1f3-113">-Confirm</span></span>
<span data-ttu-id="ef1f3-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1f3-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1f3-115">-WhatIf</span></span>
<span data-ttu-id="ef1f3-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef1f3-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1f3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef1f3-118">-Name</span></span>
<span data-ttu-id="ef1f3-119">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="ef1f3-119">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="ef1f3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef1f3-120">INPUTS</span></span>

### <span data-ttu-id="ef1f3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1f3-121">System.String</span></span>

## <span data-ttu-id="ef1f3-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef1f3-122">OUTPUTS</span></span>

### <span data-ttu-id="ef1f3-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="ef1f3-123">System.Object</span></span>

## <span data-ttu-id="ef1f3-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef1f3-124">NOTES</span></span>

## <span data-ttu-id="ef1f3-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef1f3-125">RELATED LINKS</span></span>

