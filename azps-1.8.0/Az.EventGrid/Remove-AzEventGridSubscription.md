---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754096"
---
# <span data-ttu-id="335db-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="335db-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="335db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="335db-102">SYNOPSIS</span></span>
<span data-ttu-id="335db-103">Tar bort en händelse prenumeration för ett Azure Event Grid-evenemang.</span><span class="sxs-lookup"><span data-stu-id="335db-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="335db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="335db-104">SYNTAX</span></span>

### <span data-ttu-id="335db-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="335db-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335db-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="335db-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335db-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="335db-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335db-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="335db-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="335db-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="335db-109">DESCRIPTION</span></span>
<span data-ttu-id="335db-110">Tar bort en händelse prenumeration i Azure Events Grid-avsnitt, en resurs, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335db-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="335db-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="335db-111">EXAMPLES</span></span>

### <span data-ttu-id="335db-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="335db-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="335db-113">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="335db-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="335db-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="335db-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="335db-115">Tar bort \` EventSubscription1 för händelser \` till en resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="335db-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="335db-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="335db-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="335db-117">Tar bort \` EventSubscription1 för händelser \` till standard Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="335db-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="335db-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="335db-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="335db-119">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett namn område i en händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="335db-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="335db-120">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="335db-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="335db-121">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="335db-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="335db-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="335db-122">PARAMETERS</span></span>

### <span data-ttu-id="335db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335db-123">-DefaultProfile</span></span>
<span data-ttu-id="335db-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="335db-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="335db-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="335db-125">-EventSubscriptionName</span></span>
<span data-ttu-id="335db-126">Namnet på den händelse prenumeration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="335db-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335db-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="335db-127">-InputObject</span></span>
<span data-ttu-id="335db-128">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="335db-128">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="335db-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="335db-129">-PassThru</span></span>
<span data-ttu-id="335db-130">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="335db-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="335db-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="335db-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="335db-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335db-132">-ResourceGroupName</span></span>
<span data-ttu-id="335db-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="335db-133">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335db-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="335db-134">-ResourceId</span></span>
<span data-ttu-id="335db-135">Identifierare för den resurs vars händelse prenumeration måste tas bort.</span><span class="sxs-lookup"><span data-stu-id="335db-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="335db-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="335db-136">-TopicName</span></span>
<span data-ttu-id="335db-137">Avsnitts namn i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="335db-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="335db-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="335db-138">-Confirm</span></span>
<span data-ttu-id="335db-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="335db-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335db-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335db-140">-WhatIf</span></span>
<span data-ttu-id="335db-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="335db-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335db-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="335db-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335db-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335db-143">CommonParameters</span></span>
<span data-ttu-id="335db-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335db-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335db-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335db-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335db-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="335db-146">INPUTS</span></span>

### <span data-ttu-id="335db-147">System. String</span><span class="sxs-lookup"><span data-stu-id="335db-147">System.String</span></span>

### <span data-ttu-id="335db-148">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="335db-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="335db-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="335db-149">OUTPUTS</span></span>

### <span data-ttu-id="335db-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="335db-150">System.Boolean</span></span>

## <span data-ttu-id="335db-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="335db-151">NOTES</span></span>

## <span data-ttu-id="335db-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="335db-152">RELATED LINKS</span></span>
