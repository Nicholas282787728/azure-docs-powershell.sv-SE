---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270669"
---
# <span data-ttu-id="fe842-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fe842-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="fe842-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe842-102">SYNOPSIS</span></span>
<span data-ttu-id="fe842-103">Uppdaterar den angivna konsument gruppen för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="fe842-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="fe842-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe842-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe842-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe842-105">DESCRIPTION</span></span>
<span data-ttu-id="fe842-106">Den Set-AzEventHubConsumerGroup cmdleten uppdaterar den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="fe842-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="fe842-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe842-107">EXAMPLES</span></span>

### <span data-ttu-id="fe842-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe842-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="fe842-109">Anger användarnas metadata för konsument gruppen \` MyConsumerGroupName \` till "testar".</span><span class="sxs-lookup"><span data-stu-id="fe842-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="fe842-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe842-110">PARAMETERS</span></span>

### <span data-ttu-id="fe842-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe842-111">-DefaultProfile</span></span>
<span data-ttu-id="fe842-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe842-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe842-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fe842-113">-EventHub</span></span>
<span data-ttu-id="fe842-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="fe842-114">EventHub Name</span></span>

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

### <span data-ttu-id="fe842-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe842-115">-Name</span></span>
<span data-ttu-id="fe842-116">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="fe842-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="fe842-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fe842-117">-Namespace</span></span>
<span data-ttu-id="fe842-118">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="fe842-118">Namespace Name</span></span>

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

### <span data-ttu-id="fe842-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe842-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe842-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fe842-120">Resource Group Name</span></span>

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

### <span data-ttu-id="fe842-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fe842-121">-UserMetadata</span></span>
<span data-ttu-id="fe842-122">Användarens metadata för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fe842-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="fe842-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe842-123">-Confirm</span></span>
<span data-ttu-id="fe842-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe842-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe842-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe842-125">-WhatIf</span></span>
<span data-ttu-id="fe842-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe842-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe842-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe842-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe842-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe842-128">CommonParameters</span></span>
<span data-ttu-id="fe842-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe842-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe842-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe842-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe842-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe842-131">INPUTS</span></span>

### <span data-ttu-id="fe842-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe842-132">System.String</span></span>

## <span data-ttu-id="fe842-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe842-133">OUTPUTS</span></span>

### <span data-ttu-id="fe842-134">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="fe842-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="fe842-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe842-135">NOTES</span></span>

## <span data-ttu-id="fe842-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe842-136">RELATED LINKS</span></span>