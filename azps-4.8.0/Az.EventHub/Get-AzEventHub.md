---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261316"
---
# <span data-ttu-id="df0cc-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="df0cc-101">Get-AzEventHub</span></span>

## <span data-ttu-id="df0cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="df0cc-103">Hämtar information om en enkel Event-hubb eller hämtar en lista över händelse nav.</span><span class="sxs-lookup"><span data-stu-id="df0cc-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="df0cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df0cc-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df0cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="df0cc-106">Get-AzEventHub cmdlet returnerar antingen informationen om en Händelsehubben eller en lista över alla händelse nav i det aktuella namn området.</span><span class="sxs-lookup"><span data-stu-id="df0cc-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="df0cc-107">Om namnet på händelsehubben är angivet returneras informationen om en enskild Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="df0cc-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="df0cc-108">Om ett namn på en Händelsehubben inte anges returneras en lista över alla händelse nav i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="df0cc-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="df0cc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df0cc-109">EXAMPLES</span></span>

### <span data-ttu-id="df0cc-110">Exempel 1: angiven EventHub</span><span class="sxs-lookup"><span data-stu-id="df0cc-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="df0cc-111">Returnerar information om Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="df0cc-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="df0cc-112">Exempel 2: lista över EventHub i angivet namn område</span><span class="sxs-lookup"><span data-stu-id="df0cc-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="df0cc-113">Returnerar en lista med händelse nav i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="df0cc-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="df0cc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df0cc-114">PARAMETERS</span></span>

### <span data-ttu-id="df0cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0cc-115">-DefaultProfile</span></span>
<span data-ttu-id="df0cc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df0cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df0cc-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="df0cc-117">-MaxCount</span></span>
<span data-ttu-id="df0cc-118">Fastställ maximalt antal EventHubs som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="df0cc-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="df0cc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="df0cc-119">-Name</span></span>
<span data-ttu-id="df0cc-120">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="df0cc-120">EventHub Name</span></span>

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

### <span data-ttu-id="df0cc-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="df0cc-121">-Namespace</span></span>
<span data-ttu-id="df0cc-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="df0cc-122">Namespace Name</span></span>

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

### <span data-ttu-id="df0cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df0cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="df0cc-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="df0cc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="df0cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0cc-125">CommonParameters</span></span>
<span data-ttu-id="df0cc-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0cc-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0cc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0cc-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df0cc-128">INPUTS</span></span>

### <span data-ttu-id="df0cc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="df0cc-129">System.String</span></span>

## <span data-ttu-id="df0cc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df0cc-130">OUTPUTS</span></span>

### <span data-ttu-id="df0cc-131">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="df0cc-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="df0cc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df0cc-132">NOTES</span></span>

## <span data-ttu-id="df0cc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df0cc-133">RELATED LINKS</span></span>
