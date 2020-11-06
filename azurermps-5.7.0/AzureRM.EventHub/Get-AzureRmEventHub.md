---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576529"
---
# <span data-ttu-id="3d081-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="3d081-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="3d081-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d081-102">SYNOPSIS</span></span>
<span data-ttu-id="3d081-103">Hämtar information om en enkel Event-hubb eller hämtar en lista över händelse nav.</span><span class="sxs-lookup"><span data-stu-id="3d081-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d081-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d081-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d081-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d081-105">DESCRIPTION</span></span>
<span data-ttu-id="3d081-106">Get-AzureRmEventHub cmdlet returnerar antingen informationen om en Händelsehubben eller en lista över alla händelse nav i det aktuella namn området.</span><span class="sxs-lookup"><span data-stu-id="3d081-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="3d081-107">Om namnet på händelsehubben är angivet returneras informationen om en enskild Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="3d081-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="3d081-108">Om ett namn på en Händelsehubben inte anges returneras en lista över alla händelse nav i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="3d081-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="3d081-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d081-109">EXAMPLES</span></span>

### <span data-ttu-id="3d081-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d081-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="3d081-111">Returnerar information om Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="3d081-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="3d081-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d081-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="3d081-113">Returnerar en lista med händelse nav i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="3d081-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="3d081-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d081-114">PARAMETERS</span></span>

### <span data-ttu-id="3d081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d081-115">-DefaultProfile</span></span>
<span data-ttu-id="3d081-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d081-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d081-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d081-117">-Name</span></span>
<span data-ttu-id="3d081-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="3d081-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d081-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3d081-119">-Namespace</span></span>
<span data-ttu-id="3d081-120">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="3d081-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d081-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d081-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d081-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3d081-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3d081-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d081-123">CommonParameters</span></span>
<span data-ttu-id="3d081-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d081-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3d081-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d081-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d081-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d081-126">INPUTS</span></span>

### <span data-ttu-id="3d081-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3d081-127">System.String</span></span>


## <span data-ttu-id="3d081-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d081-128">OUTPUTS</span></span>

### <span data-ttu-id="3d081-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes, Microsoft. Azure. commands. EventHub, version = 0.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3d081-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="3d081-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d081-130">NOTES</span></span>

## <span data-ttu-id="3d081-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d081-131">RELATED LINKS</span></span>
