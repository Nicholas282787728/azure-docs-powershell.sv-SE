---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: d4443cf25790d74617a02b048ce31296e451cf95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922874"
---
# <span data-ttu-id="f1bc9-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f1bc9-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="f1bc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bc9-103">Tar bort den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="f1bc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1bc9-104">SYNTAX</span></span>

### <span data-ttu-id="f1bc9-105">ConsumergroupPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1bc9-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1bc9-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f1bc9-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1bc9-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1bc9-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1bc9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="f1bc9-109">Remove-AzEventHubConsumerGroup-cmdleten tar bort och tar bort den angivna konsument gruppen från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="f1bc9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="f1bc9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1bc9-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="f1bc9-112">Tar bort gruppen konsument \` MyConsumerGroupName \` från \` MyEventHubName med \` \` MyNamespaceName- \` namnområdet.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="f1bc9-113">Exempel 2,1 – InputObject – använder variabel</span><span class="sxs-lookup"><span data-stu-id="f1bc9-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="f1bc9-114">Exempel 2,2 – InputObject – använder rör</span><span class="sxs-lookup"><span data-stu-id="f1bc9-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="f1bc9-115">Exempel 3,1-ResourceId med variabel</span><span class="sxs-lookup"><span data-stu-id="f1bc9-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="f1bc9-116">Exempel 3,2-ResourceId med sträng</span><span class="sxs-lookup"><span data-stu-id="f1bc9-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="f1bc9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1bc9-117">PARAMETERS</span></span>

### <span data-ttu-id="f1bc9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1bc9-118">-AsJob</span></span>
<span data-ttu-id="f1bc9-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f1bc9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1bc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1bc9-120">-DefaultProfile</span></span>
<span data-ttu-id="f1bc9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1bc9-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f1bc9-122">-EventHub</span></span>
<span data-ttu-id="f1bc9-123">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="f1bc9-123">EventHub Name</span></span>

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

### <span data-ttu-id="f1bc9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1bc9-124">-InputObject</span></span>
<span data-ttu-id="f1bc9-125">ConsumerGroup-objekt</span><span class="sxs-lookup"><span data-stu-id="f1bc9-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="f1bc9-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1bc9-126">-Name</span></span>
<span data-ttu-id="f1bc9-127">ConsumerGroup namn</span><span class="sxs-lookup"><span data-stu-id="f1bc9-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="f1bc9-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f1bc9-128">-Namespace</span></span>
<span data-ttu-id="f1bc9-129">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="f1bc9-129">Namespace Name</span></span>

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

### <span data-ttu-id="f1bc9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1bc9-130">-PassThru</span></span>
<span data-ttu-id="f1bc9-131">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f1bc9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bc9-132">-ResourceGroupName</span></span>
<span data-ttu-id="f1bc9-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f1bc9-133">Resource Group Name</span></span>

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

### <span data-ttu-id="f1bc9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1bc9-134">-ResourceId</span></span>
<span data-ttu-id="f1bc9-135">Resurs-ID för ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f1bc9-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="f1bc9-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1bc9-136">-Confirm</span></span>
<span data-ttu-id="f1bc9-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1bc9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1bc9-138">-WhatIf</span></span>
<span data-ttu-id="f1bc9-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1bc9-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1bc9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bc9-141">CommonParameters</span></span>
<span data-ttu-id="f1bc9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1bc9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bc9-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1bc9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bc9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1bc9-144">INPUTS</span></span>

### <span data-ttu-id="f1bc9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f1bc9-145">System.String</span></span>

### <span data-ttu-id="f1bc9-146">Microsoft. Azure. commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="f1bc9-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="f1bc9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1bc9-147">OUTPUTS</span></span>

### <span data-ttu-id="f1bc9-148">System. Void</span><span class="sxs-lookup"><span data-stu-id="f1bc9-148">System.Void</span></span>

## <span data-ttu-id="f1bc9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1bc9-149">NOTES</span></span>

## <span data-ttu-id="f1bc9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1bc9-150">RELATED LINKS</span></span>
