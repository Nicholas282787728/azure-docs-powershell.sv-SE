---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520799"
---
# <span data-ttu-id="785cf-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="785cf-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="785cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="785cf-102">SYNOPSIS</span></span>
<span data-ttu-id="785cf-103">Tar bort en händelse prenumeration för ett Azure Event Grid-evenemang.</span><span class="sxs-lookup"><span data-stu-id="785cf-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="785cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="785cf-104">SYNTAX</span></span>

### <span data-ttu-id="785cf-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="785cf-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="785cf-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cf-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cf-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="785cf-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="785cf-114">DESCRIPTION</span></span>
<span data-ttu-id="785cf-115">Tar bort en händelse prenumeration i Azure Events Grid-avsnitt, en resurs, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="785cf-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="785cf-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="785cf-116">EXAMPLES</span></span>

### <span data-ttu-id="785cf-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="785cf-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="785cf-118">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="785cf-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="785cf-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="785cf-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="785cf-120">Tar bort \` EventSubscription1 för händelser \` till en resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="785cf-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="785cf-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="785cf-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="785cf-122">Tar bort \` EventSubscription1 för händelser \` till standard Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="785cf-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="785cf-123">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="785cf-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="785cf-124">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett namn område i en händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="785cf-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="785cf-125">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="785cf-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="785cf-126">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="785cf-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="785cf-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="785cf-127">PARAMETERS</span></span>

### <span data-ttu-id="785cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785cf-128">-DefaultProfile</span></span>
<span data-ttu-id="785cf-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="785cf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="785cf-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="785cf-130">-DomainInputObject</span></span>
<span data-ttu-id="785cf-131">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="785cf-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-132">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="785cf-132">-DomainName</span></span>
<span data-ttu-id="785cf-133">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="785cf-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="785cf-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="785cf-135">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="785cf-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="785cf-136">-DomainTopicName</span></span>
<span data-ttu-id="785cf-137">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="785cf-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="785cf-138">-EventSubscriptionName</span></span>
<span data-ttu-id="785cf-139">Namnet på den händelse prenumeration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="785cf-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="785cf-140">-InputObject</span></span>
<span data-ttu-id="785cf-141">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="785cf-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="785cf-142">-PassThru</span></span>
<span data-ttu-id="785cf-143">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="785cf-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="785cf-144">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="785cf-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="785cf-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785cf-145">-ResourceGroupName</span></span>
<span data-ttu-id="785cf-146">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="785cf-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="785cf-147">-ResourceId</span></span>
<span data-ttu-id="785cf-148">Identifierare för den resurs vars händelse prenumeration måste tas bort.</span><span class="sxs-lookup"><span data-stu-id="785cf-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="785cf-149">-TopicName</span></span>
<span data-ttu-id="785cf-150">Avsnitts namn i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="785cf-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785cf-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="785cf-151">-Confirm</span></span>
<span data-ttu-id="785cf-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="785cf-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="785cf-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="785cf-153">-WhatIf</span></span>
<span data-ttu-id="785cf-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="785cf-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="785cf-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="785cf-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="785cf-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785cf-156">CommonParameters</span></span>
<span data-ttu-id="785cf-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785cf-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785cf-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="785cf-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785cf-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="785cf-159">INPUTS</span></span>

### <span data-ttu-id="785cf-160">System. String</span><span class="sxs-lookup"><span data-stu-id="785cf-160">System.String</span></span>

### <span data-ttu-id="785cf-161">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="785cf-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="785cf-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="785cf-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="785cf-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="785cf-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="785cf-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="785cf-164">OUTPUTS</span></span>

### <span data-ttu-id="785cf-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="785cf-165">System.Boolean</span></span>

## <span data-ttu-id="785cf-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="785cf-166">NOTES</span></span>

## <span data-ttu-id="785cf-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="785cf-167">RELATED LINKS</span></span>
