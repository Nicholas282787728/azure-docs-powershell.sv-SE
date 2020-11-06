---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577230"
---
# <span data-ttu-id="60e43-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="60e43-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="60e43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60e43-102">SYNOPSIS</span></span>
<span data-ttu-id="60e43-103">Tar bort den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="60e43-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60e43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60e43-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60e43-105">DESCRIPTION</span></span>
<span data-ttu-id="60e43-106">Remove-AzureRmEventHubConsumerGroup-cmdleten tar bort och tar bort den angivna konsument gruppen från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="60e43-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="60e43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60e43-107">EXAMPLES</span></span>

### <span data-ttu-id="60e43-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="60e43-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="60e43-109">Tar bort gruppen konsument \` MyConsumerGroupName \` från \` MyEventHubName med \` \` MyNamespaceName- \` namnområdet.</span><span class="sxs-lookup"><span data-stu-id="60e43-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="60e43-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60e43-110">PARAMETERS</span></span>

### <span data-ttu-id="60e43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e43-111">-DefaultProfile</span></span>
<span data-ttu-id="60e43-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60e43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e43-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="60e43-113">-EventHub</span></span>
<span data-ttu-id="60e43-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="60e43-114">EventHub Name</span></span>

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

### <span data-ttu-id="60e43-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="60e43-115">-Name</span></span>
<span data-ttu-id="60e43-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="60e43-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="60e43-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="60e43-117">-Namespace</span></span>
<span data-ttu-id="60e43-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="60e43-118">Namespace Name</span></span>

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

### <span data-ttu-id="60e43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e43-119">-ResourceGroupName</span></span>
<span data-ttu-id="60e43-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="60e43-120">Resource Group Name</span></span>

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

### <span data-ttu-id="60e43-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60e43-121">-Confirm</span></span>
<span data-ttu-id="60e43-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60e43-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e43-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e43-123">-WhatIf</span></span>
<span data-ttu-id="60e43-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60e43-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e43-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60e43-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e43-126">CommonParameters</span></span>
<span data-ttu-id="60e43-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="60e43-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e43-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e43-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60e43-129">INPUTS</span></span>

### <span data-ttu-id="60e43-130">System. String</span><span class="sxs-lookup"><span data-stu-id="60e43-130">System.String</span></span>


## <span data-ttu-id="60e43-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60e43-131">OUTPUTS</span></span>

### <span data-ttu-id="60e43-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="60e43-132">System.Object</span></span>

## <span data-ttu-id="60e43-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60e43-133">NOTES</span></span>

## <span data-ttu-id="60e43-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60e43-134">RELATED LINKS</span></span>
