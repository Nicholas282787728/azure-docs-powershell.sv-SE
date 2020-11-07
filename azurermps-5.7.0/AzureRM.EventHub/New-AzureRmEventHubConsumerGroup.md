---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757254"
---
# <span data-ttu-id="d05d7-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d05d7-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d05d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d05d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d05d7-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="d05d7-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d05d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d05d7-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d05d7-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d05d7-105">EXAMPLES</span></span>

### <span data-ttu-id="d05d7-106">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d05d7-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d05d7-107">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d05d7-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d05d7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d05d7-108">PARAMETERS</span></span>

### <span data-ttu-id="d05d7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05d7-109">-DefaultProfile</span></span>
<span data-ttu-id="d05d7-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d05d7-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d05d7-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d05d7-111">-EventHub</span></span>
<span data-ttu-id="d05d7-112">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="d05d7-112">EventHub Name</span></span>

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

### <span data-ttu-id="d05d7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d05d7-113">-Name</span></span>
<span data-ttu-id="d05d7-114">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="d05d7-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05d7-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d05d7-115">-Namespace</span></span>
<span data-ttu-id="d05d7-116">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="d05d7-116">Namespace Name</span></span>

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

### <span data-ttu-id="d05d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d05d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d05d7-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d05d7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d05d7-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d05d7-119">-UserMetadata</span></span>
<span data-ttu-id="d05d7-120">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d05d7-120">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05d7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d05d7-121">-Confirm</span></span>
<span data-ttu-id="d05d7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d05d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d05d7-123">-WhatIf</span></span>
<span data-ttu-id="d05d7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d05d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d05d7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d05d7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05d7-126">CommonParameters</span></span>
<span data-ttu-id="d05d7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d05d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d05d7-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05d7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05d7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d05d7-129">INPUTS</span></span>

### <span data-ttu-id="d05d7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d05d7-130">System.String</span></span>


## <span data-ttu-id="d05d7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d05d7-131">OUTPUTS</span></span>

### <span data-ttu-id="d05d7-132">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="d05d7-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="d05d7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d05d7-133">NOTES</span></span>

## <span data-ttu-id="d05d7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d05d7-134">RELATED LINKS</span></span>
