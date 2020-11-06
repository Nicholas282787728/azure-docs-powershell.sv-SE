---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583168"
---
# <span data-ttu-id="82f5d-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="82f5d-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="82f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="82f5d-103">Hämtar information om en viss konsument grupp för händelse nav eller hämtar en lista över konsument grupper i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="82f5d-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82f5d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82f5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="82f5d-106">Get-AzureRmEventHubConsumerGroup-cmdleten får antingen information om en viss konsument grupp för händelse nav eller en lista över konsument grupper i en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="82f5d-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="82f5d-107">Om namnet på en konsument grupp är angivet returneras informationen om en enskild konsument grupp information.</span><span class="sxs-lookup"><span data-stu-id="82f5d-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="82f5d-108">Om namnet på en konsument grupp inte har angetts returneras en lista över konsument grupper i den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="82f5d-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="82f5d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="82f5d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82f5d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="82f5d-111">Hämtar gruppen konsument \` MyConsumerGroupName \` i \` MyEventHubName \` som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="82f5d-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="82f5d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="82f5d-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="82f5d-113">Hämtar en lista över konsument grupper i Händelsehubben \` MyEventHubName \` , som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="82f5d-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="82f5d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="82f5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f5d-115">-DefaultProfile</span></span>
<span data-ttu-id="82f5d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82f5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f5d-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="82f5d-117">-EventHub</span></span>
<span data-ttu-id="82f5d-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="82f5d-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="82f5d-119">-Name</span></span>
<span data-ttu-id="82f5d-120">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="82f5d-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5d-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="82f5d-121">-Namespace</span></span>
<span data-ttu-id="82f5d-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="82f5d-122">Namespace Name</span></span>

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

### <span data-ttu-id="82f5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="82f5d-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="82f5d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="82f5d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f5d-125">CommonParameters</span></span>
<span data-ttu-id="82f5d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f5d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82f5d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f5d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f5d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82f5d-128">INPUTS</span></span>

### <span data-ttu-id="82f5d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="82f5d-129">System.String</span></span>


## <span data-ttu-id="82f5d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82f5d-130">OUTPUTS</span></span>

### <span data-ttu-id="82f5d-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes, Microsoft. Azure. commands. EventHub, version = 0.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="82f5d-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="82f5d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82f5d-132">NOTES</span></span>

## <span data-ttu-id="82f5d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82f5d-133">RELATED LINKS</span></span>
