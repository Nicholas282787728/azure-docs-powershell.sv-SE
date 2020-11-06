---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577041"
---
# <span data-ttu-id="b8d95-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b8d95-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="b8d95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8d95-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d95-103">Tar bort den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="b8d95-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8d95-104">SYNTAX</span></span>

### <span data-ttu-id="b8d95-105">ConsumergroupPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b8d95-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8d95-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8d95-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8d95-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d95-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d95-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8d95-108">DESCRIPTION</span></span>
<span data-ttu-id="b8d95-109">Remove-AzureRmEventHubConsumerGroup-cmdleten tar bort och tar bort den angivna konsument gruppen från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="b8d95-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="b8d95-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8d95-110">EXAMPLES</span></span>

### <span data-ttu-id="b8d95-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8d95-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="b8d95-112">Tar bort gruppen konsument \` MyConsumerGroupName \` från \` MyEventHubName med \` \` MyNamespaceName- \` namnområdet.</span><span class="sxs-lookup"><span data-stu-id="b8d95-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="b8d95-113">Exempel 2,1 – InputObject – använder variabel</span><span class="sxs-lookup"><span data-stu-id="b8d95-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="b8d95-114">Exempel 2,2 – InputObject – använder rör</span><span class="sxs-lookup"><span data-stu-id="b8d95-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="b8d95-115">Exempel 3,1-ResourceId med Vairable</span><span class="sxs-lookup"><span data-stu-id="b8d95-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="b8d95-116">Exempel 3,2-ResourceId med sträng</span><span class="sxs-lookup"><span data-stu-id="b8d95-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="b8d95-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8d95-117">PARAMETERS</span></span>

### <span data-ttu-id="b8d95-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8d95-118">-AsJob</span></span>
<span data-ttu-id="b8d95-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b8d95-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d95-120">-DefaultProfile</span></span>
<span data-ttu-id="b8d95-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d95-122">-EventHub</span></span>
<span data-ttu-id="b8d95-123">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d95-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8d95-124">-InputObject</span></span>
<span data-ttu-id="b8d95-125">ConsumerGroup-objekt</span><span class="sxs-lookup"><span data-stu-id="b8d95-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8d95-126">-Name</span></span>
<span data-ttu-id="b8d95-127">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="b8d95-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b8d95-128">-Namespace</span></span>
<span data-ttu-id="b8d95-129">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b8d95-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8d95-130">-PassThru</span></span>
<span data-ttu-id="b8d95-131">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="b8d95-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d95-132">-ResourceGroupName</span></span>
<span data-ttu-id="b8d95-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b8d95-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8d95-134">-ResourceId</span></span>
<span data-ttu-id="b8d95-135">Resurs-ID för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b8d95-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d95-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8d95-136">-Confirm</span></span>
<span data-ttu-id="b8d95-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8d95-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d95-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d95-138">-WhatIf</span></span>
<span data-ttu-id="b8d95-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8d95-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d95-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8d95-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d95-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d95-141">CommonParameters</span></span>
<span data-ttu-id="b8d95-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d95-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d95-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d95-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d95-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8d95-144">INPUTS</span></span>

### <span data-ttu-id="b8d95-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d95-145">System.String</span></span>

### <span data-ttu-id="b8d95-146">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="b8d95-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="b8d95-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8d95-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b8d95-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8d95-148">OUTPUTS</span></span>

### <span data-ttu-id="b8d95-149">System. Void</span><span class="sxs-lookup"><span data-stu-id="b8d95-149">System.Void</span></span>

## <span data-ttu-id="b8d95-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8d95-150">NOTES</span></span>

## <span data-ttu-id="b8d95-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8d95-151">RELATED LINKS</span></span>
