---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091826"
---
# <span data-ttu-id="786b4-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="786b4-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="786b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="786b4-102">SYNOPSIS</span></span>
<span data-ttu-id="786b4-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="786b4-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="786b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="786b4-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="786b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="786b4-105">DESCRIPTION</span></span>
<span data-ttu-id="786b4-106">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="786b4-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="786b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="786b4-107">EXAMPLES</span></span>

### <span data-ttu-id="786b4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="786b4-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="786b4-109">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="786b4-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="786b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="786b4-110">PARAMETERS</span></span>

### <span data-ttu-id="786b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786b4-111">-DefaultProfile</span></span>
<span data-ttu-id="786b4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="786b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786b4-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="786b4-113">-EventHub</span></span>
<span data-ttu-id="786b4-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="786b4-114">EventHub Name</span></span>

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

### <span data-ttu-id="786b4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="786b4-115">-Name</span></span>
<span data-ttu-id="786b4-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="786b4-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="786b4-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="786b4-117">-Namespace</span></span>
<span data-ttu-id="786b4-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="786b4-118">Namespace Name</span></span>

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

### <span data-ttu-id="786b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="786b4-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="786b4-120">Resource Group Name</span></span>

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

### <span data-ttu-id="786b4-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="786b4-121">-UserMetadata</span></span>
<span data-ttu-id="786b4-122">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="786b4-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="786b4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="786b4-123">-Confirm</span></span>
<span data-ttu-id="786b4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="786b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="786b4-125">-WhatIf</span></span>
<span data-ttu-id="786b4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="786b4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="786b4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="786b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786b4-128">CommonParameters</span></span>
<span data-ttu-id="786b4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="786b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786b4-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="786b4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786b4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="786b4-131">INPUTS</span></span>

### <span data-ttu-id="786b4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="786b4-132">System.String</span></span>

## <span data-ttu-id="786b4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="786b4-133">OUTPUTS</span></span>

### <span data-ttu-id="786b4-134">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="786b4-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="786b4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="786b4-135">NOTES</span></span>

## <span data-ttu-id="786b4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="786b4-136">RELATED LINKS</span></span>