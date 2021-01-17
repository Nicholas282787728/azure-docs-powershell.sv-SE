---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426187"
---
# <span data-ttu-id="358a3-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="358a3-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="358a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="358a3-102">SYNOPSIS</span></span>
<span data-ttu-id="358a3-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="358a3-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="358a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="358a3-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="358a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="358a3-105">DESCRIPTION</span></span>
<span data-ttu-id="358a3-106">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="358a3-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="358a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="358a3-107">EXAMPLES</span></span>

### <span data-ttu-id="358a3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="358a3-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="358a3-109">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="358a3-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="358a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="358a3-110">PARAMETERS</span></span>

### <span data-ttu-id="358a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358a3-111">-DefaultProfile</span></span>
<span data-ttu-id="358a3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="358a3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358a3-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="358a3-113">-EventHub</span></span>
<span data-ttu-id="358a3-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="358a3-114">EventHub Name</span></span>

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

### <span data-ttu-id="358a3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="358a3-115">-Name</span></span>
<span data-ttu-id="358a3-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="358a3-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="358a3-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="358a3-117">-Namespace</span></span>
<span data-ttu-id="358a3-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="358a3-118">Namespace Name</span></span>

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

### <span data-ttu-id="358a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="358a3-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="358a3-120">Resource Group Name</span></span>

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

### <span data-ttu-id="358a3-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="358a3-121">-UserMetadata</span></span>
<span data-ttu-id="358a3-122">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="358a3-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="358a3-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="358a3-123">-Confirm</span></span>
<span data-ttu-id="358a3-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="358a3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358a3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358a3-125">-WhatIf</span></span>
<span data-ttu-id="358a3-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="358a3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358a3-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="358a3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358a3-128">CommonParameters</span></span>
<span data-ttu-id="358a3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358a3-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358a3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358a3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="358a3-131">INPUTS</span></span>

### <span data-ttu-id="358a3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="358a3-132">System.String</span></span>

## <span data-ttu-id="358a3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="358a3-133">OUTPUTS</span></span>

### <span data-ttu-id="358a3-134">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="358a3-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="358a3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="358a3-135">NOTES</span></span>

## <span data-ttu-id="358a3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="358a3-136">RELATED LINKS</span></span>
