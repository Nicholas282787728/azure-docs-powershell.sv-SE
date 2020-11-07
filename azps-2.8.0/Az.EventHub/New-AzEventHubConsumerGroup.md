---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: c887aab15e0874357ec32d9c815a9a9b1dd1227a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744203"
---
# <span data-ttu-id="1e18f-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1e18f-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="1e18f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e18f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e18f-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="1e18f-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="1e18f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e18f-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e18f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e18f-105">DESCRIPTION</span></span>
<span data-ttu-id="1e18f-106">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="1e18f-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="1e18f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e18f-107">EXAMPLES</span></span>

### <span data-ttu-id="1e18f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1e18f-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="1e18f-109">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1e18f-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1e18f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e18f-110">PARAMETERS</span></span>

### <span data-ttu-id="1e18f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e18f-111">-DefaultProfile</span></span>
<span data-ttu-id="1e18f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e18f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e18f-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1e18f-113">-EventHub</span></span>
<span data-ttu-id="1e18f-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="1e18f-114">EventHub Name</span></span>

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

### <span data-ttu-id="1e18f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e18f-115">-Name</span></span>
<span data-ttu-id="1e18f-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="1e18f-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="1e18f-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1e18f-117">-Namespace</span></span>
<span data-ttu-id="1e18f-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="1e18f-118">Namespace Name</span></span>

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

### <span data-ttu-id="1e18f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e18f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e18f-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1e18f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="1e18f-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1e18f-121">-UserMetadata</span></span>
<span data-ttu-id="1e18f-122">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1e18f-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="1e18f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e18f-123">-Confirm</span></span>
<span data-ttu-id="1e18f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e18f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e18f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e18f-125">-WhatIf</span></span>
<span data-ttu-id="1e18f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e18f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e18f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e18f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e18f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e18f-128">CommonParameters</span></span>
<span data-ttu-id="1e18f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e18f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e18f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e18f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e18f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e18f-131">INPUTS</span></span>

### <span data-ttu-id="1e18f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e18f-132">System.String</span></span>

## <span data-ttu-id="1e18f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e18f-133">OUTPUTS</span></span>

### <span data-ttu-id="1e18f-134">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="1e18f-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="1e18f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e18f-135">NOTES</span></span>

## <span data-ttu-id="1e18f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e18f-136">RELATED LINKS</span></span>
