---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583307"
---
# <span data-ttu-id="baf66-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="baf66-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="baf66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="baf66-102">SYNOPSIS</span></span>
<span data-ttu-id="baf66-103">Hämtar information om namn området för en händelse hubb eller hämtar en lista över alla namn rymder för händelser i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="baf66-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baf66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="baf66-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="baf66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="baf66-105">DESCRIPTION</span></span>
<span data-ttu-id="baf66-106">Get-AzureRmEventHubNamespace-cmdleten får antingen information om ett angivet namn område för händelse nav, eller en lista över alla namn områden i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="baf66-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="baf66-107">Om namn områdes namnet är angivet returneras informationen om ett namn område med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="baf66-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="baf66-108">Om namn områdes namnet inte anges returneras en lista med namn områden.</span><span class="sxs-lookup"><span data-stu-id="baf66-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="baf66-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="baf66-109">EXAMPLES</span></span>

### <span data-ttu-id="baf66-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="baf66-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="baf66-111">Hämtar information om namn området för Event Hub \` MyNamespaceName \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="baf66-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="baf66-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="baf66-112">PARAMETERS</span></span>

### <span data-ttu-id="baf66-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf66-113">-ResourceGroupName</span></span>
<span data-ttu-id="baf66-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="baf66-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf66-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="baf66-115">-Name</span></span>
<span data-ttu-id="baf66-116">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="baf66-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="baf66-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="baf66-117">INPUTS</span></span>

### <span data-ttu-id="baf66-118">System. String</span><span class="sxs-lookup"><span data-stu-id="baf66-118">System.String</span></span>

## <span data-ttu-id="baf66-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="baf66-119">OUTPUTS</span></span>

### <span data-ttu-id="baf66-120">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. NamespaceAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="baf66-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="baf66-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="baf66-121">NOTES</span></span>

## <span data-ttu-id="baf66-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="baf66-122">RELATED LINKS</span></span>

