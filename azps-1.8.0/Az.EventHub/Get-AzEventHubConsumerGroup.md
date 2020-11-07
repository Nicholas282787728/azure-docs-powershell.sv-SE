---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 7f10df478851679afeb73157252d954f756f0c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754079"
---
# <span data-ttu-id="f3745-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f3745-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="f3745-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3745-102">SYNOPSIS</span></span>
<span data-ttu-id="f3745-103">Hämtar information om en viss konsument grupp för händelse nav eller hämtar en lista över konsument grupper i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="f3745-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="f3745-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3745-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3745-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3745-105">DESCRIPTION</span></span>
<span data-ttu-id="f3745-106">Get-AzEventHubConsumerGroup-cmdleten får antingen information om en viss konsument grupp för händelse nav eller en lista över konsument grupper i en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="f3745-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="f3745-107">Om namnet på en konsument grupp är angivet returneras informationen om en enskild konsument grupp information.</span><span class="sxs-lookup"><span data-stu-id="f3745-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="f3745-108">Om namnet på en konsument grupp inte har angetts returneras en lista över konsument grupper i den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="f3745-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="f3745-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3745-109">EXAMPLES</span></span>

### <span data-ttu-id="f3745-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f3745-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="f3745-111">Hämtar gruppen konsument \` MyConsumerGroupName \` i \` MyEventHubName \` som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3745-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f3745-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f3745-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="f3745-113">Hämtar en lista över konsument grupper i Händelsehubben \` MyEventHubName \` , som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3745-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f3745-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3745-114">PARAMETERS</span></span>

### <span data-ttu-id="f3745-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3745-115">-DefaultProfile</span></span>
<span data-ttu-id="f3745-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3745-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3745-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f3745-117">-EventHub</span></span>
<span data-ttu-id="f3745-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="f3745-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3745-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f3745-119">-MaxCount</span></span>
<span data-ttu-id="f3745-120">Fastställ maximalt antal ConsumerGroups som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="f3745-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="f3745-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3745-121">-Name</span></span>
<span data-ttu-id="f3745-122">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="f3745-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3745-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f3745-123">-Namespace</span></span>
<span data-ttu-id="f3745-124">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="f3745-124">Namespace Name</span></span>

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

### <span data-ttu-id="f3745-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3745-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3745-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f3745-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f3745-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3745-127">CommonParameters</span></span>
<span data-ttu-id="f3745-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3745-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3745-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3745-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3745-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3745-130">INPUTS</span></span>

### <span data-ttu-id="f3745-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f3745-131">System.String</span></span>

## <span data-ttu-id="f3745-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3745-132">OUTPUTS</span></span>

### <span data-ttu-id="f3745-133">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="f3745-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="f3745-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3745-134">NOTES</span></span>

## <span data-ttu-id="f3745-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3745-135">RELATED LINKS</span></span>
