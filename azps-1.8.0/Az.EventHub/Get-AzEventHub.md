---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: 662c2b5ed487a13c557e85709ed7b850a28acb2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916798"
---
# <span data-ttu-id="cc7c1-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="cc7c1-101">Get-AzEventHub</span></span>

## <span data-ttu-id="cc7c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7c1-103">Hämtar information om en enkel Event-hubb eller hämtar en lista över händelse nav.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="cc7c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc7c1-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc7c1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7c1-106">Get-AzEventHub cmdlet returnerar antingen informationen om en Händelsehubben eller en lista över alla händelse nav i det aktuella namn området.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="cc7c1-107">Om namnet på händelsehubben är angivet returneras informationen om en enskild Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="cc7c1-108">Om ett namn på en Händelsehubben inte anges returneras en lista över alla händelse nav i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="cc7c1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc7c1-109">EXAMPLES</span></span>

### <span data-ttu-id="cc7c1-110">Exempel 1-angiven EventHub</span><span class="sxs-lookup"><span data-stu-id="cc7c1-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="cc7c1-111">Returnerar information om Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="cc7c1-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="cc7c1-112">Exempel 2 – lista över EventHub i angivet namn område</span><span class="sxs-lookup"><span data-stu-id="cc7c1-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="cc7c1-113">Returnerar en lista med händelse nav i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="cc7c1-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="cc7c1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc7c1-114">PARAMETERS</span></span>

### <span data-ttu-id="cc7c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7c1-115">-DefaultProfile</span></span>
<span data-ttu-id="cc7c1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c1-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cc7c1-117">-MaxCount</span></span>
<span data-ttu-id="cc7c1-118">Fastställ maximalt antal EventHubs som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc7c1-119">-Name</span></span>
<span data-ttu-id="cc7c1-120">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="cc7c1-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c1-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="cc7c1-121">-Namespace</span></span>
<span data-ttu-id="cc7c1-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="cc7c1-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc7c1-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cc7c1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7c1-125">CommonParameters</span></span>
<span data-ttu-id="cc7c1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc7c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7c1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc7c1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7c1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc7c1-128">INPUTS</span></span>

### <span data-ttu-id="cc7c1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cc7c1-129">System.String</span></span>

## <span data-ttu-id="cc7c1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc7c1-130">OUTPUTS</span></span>

### <span data-ttu-id="cc7c1-131">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="cc7c1-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="cc7c1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc7c1-132">NOTES</span></span>

## <span data-ttu-id="cc7c1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc7c1-133">RELATED LINKS</span></span>
