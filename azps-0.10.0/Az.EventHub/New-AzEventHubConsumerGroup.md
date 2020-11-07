---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: 2e9a3340e2e514d00c43328308f95bf35b38932c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922898"
---
# <span data-ttu-id="b57e2-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b57e2-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="b57e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b57e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b57e2-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="b57e2-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="b57e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b57e2-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b57e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b57e2-105">DESCRIPTION</span></span>
<span data-ttu-id="b57e2-106">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="b57e2-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="b57e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b57e2-107">EXAMPLES</span></span>

### <span data-ttu-id="b57e2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b57e2-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="b57e2-109">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b57e2-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b57e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b57e2-110">PARAMETERS</span></span>

### <span data-ttu-id="b57e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57e2-111">-DefaultProfile</span></span>
<span data-ttu-id="b57e2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b57e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57e2-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b57e2-113">-EventHub</span></span>
<span data-ttu-id="b57e2-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="b57e2-114">EventHub Name</span></span>

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

### <span data-ttu-id="b57e2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b57e2-115">-Name</span></span>
<span data-ttu-id="b57e2-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="b57e2-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57e2-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b57e2-117">-Namespace</span></span>
<span data-ttu-id="b57e2-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b57e2-118">Namespace Name</span></span>

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

### <span data-ttu-id="b57e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="b57e2-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b57e2-120">Resource Group Name</span></span>

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

### <span data-ttu-id="b57e2-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b57e2-121">-UserMetadata</span></span>
<span data-ttu-id="b57e2-122">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b57e2-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57e2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b57e2-123">-Confirm</span></span>
<span data-ttu-id="b57e2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b57e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b57e2-125">-WhatIf</span></span>
<span data-ttu-id="b57e2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b57e2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b57e2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b57e2-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57e2-128">CommonParameters</span></span>
<span data-ttu-id="b57e2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57e2-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57e2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57e2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b57e2-131">INPUTS</span></span>

### <span data-ttu-id="b57e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b57e2-132">System.String</span></span>

## <span data-ttu-id="b57e2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b57e2-133">OUTPUTS</span></span>

### <span data-ttu-id="b57e2-134">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="b57e2-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="b57e2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b57e2-135">NOTES</span></span>

## <span data-ttu-id="b57e2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b57e2-136">RELATED LINKS</span></span>
