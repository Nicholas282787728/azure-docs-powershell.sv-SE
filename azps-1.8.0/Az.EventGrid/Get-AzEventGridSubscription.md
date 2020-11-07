---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754110"
---
# <span data-ttu-id="0578d-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0578d-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="0578d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0578d-102">SYNOPSIS</span></span>
<span data-ttu-id="0578d-103">Hämtar information om en händelse prenumeration eller hämtar en lista över alla händelse prenumerationer i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0578d-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="0578d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0578d-104">SYNTAX</span></span>

### <span data-ttu-id="0578d-105">EventSubscriptionTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0578d-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0578d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0578d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0578d-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0578d-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0578d-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0578d-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0578d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0578d-109">DESCRIPTION</span></span>
<span data-ttu-id="0578d-110">Get-AzEventGridSubscription-cmdleten får antingen information om ett angivet abonnemang för händelse rutnät eller en lista över alla prenumerationer i det aktuella Azure-abonnemanget eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0578d-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="0578d-111">Om händelse prenumerationens namn anges returneras informationen om ett enskilt rutnäts abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0578d-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="0578d-112">Om händelse prenumerationens namn inte anges returneras en lista över alla händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0578d-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="0578d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0578d-113">EXAMPLES</span></span>

### <span data-ttu-id="0578d-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0578d-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0578d-115">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0578d-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0578d-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0578d-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="0578d-117">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` , inklusive fullständig slut punkts-URL om det är en webhook-baserad händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0578d-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="0578d-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0578d-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="0578d-119">Få en lista över alla händelse prenumerationer som har skapats för ämnet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0578d-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0578d-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="0578d-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0578d-121">Hämtar information om händelse prenumerations \` EventSubscription1 \` som har skapats för resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0578d-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0578d-122">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="0578d-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0578d-123">Hämtar information om \` EventSubscription1 som \` skapats för den valda Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0578d-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="0578d-124">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="0578d-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="0578d-125">Hämtar listan över alla globala händelse prenumerationer som skapas under resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0578d-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0578d-126">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="0578d-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="0578d-127">Hämtar listan över alla globala händelse prenumerationer som har skapats under det markerade Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0578d-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="0578d-128">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="0578d-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="0578d-129">Hämtar listan över alla regionala händelse prenumerationer som skapats under resurs grupp \` MyResourceGroupName \` på den angivna platsen \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="0578d-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="0578d-130">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="0578d-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="0578d-131">Hämtar listan över alla händelse prenumerationer som har skapats för det angivna EventHub-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="0578d-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="0578d-132">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="0578d-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="0578d-133">Hämtar listan över alla händelse prenumerationer som har skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="0578d-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="0578d-134">Exempel 11</span><span class="sxs-lookup"><span data-stu-id="0578d-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="0578d-135">Hämtar listan över alla händelse prenumerationer som har skapats för den specifika resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0578d-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="0578d-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0578d-136">PARAMETERS</span></span>

### <span data-ttu-id="0578d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0578d-137">-DefaultProfile</span></span>
<span data-ttu-id="0578d-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0578d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0578d-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0578d-139">-EventSubscriptionName</span></span>
<span data-ttu-id="0578d-140">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="0578d-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="0578d-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="0578d-142">Ange fullständig slut punkts-URL för händelse prenumerationens destination.</span><span class="sxs-lookup"><span data-stu-id="0578d-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0578d-143">-InputObject</span></span>
<span data-ttu-id="0578d-144">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="0578d-144">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0578d-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="0578d-145">-Location</span></span>
<span data-ttu-id="0578d-146">Plats</span><span class="sxs-lookup"><span data-stu-id="0578d-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0578d-147">-ResourceGroupName</span></span>
<span data-ttu-id="0578d-148">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0578d-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0578d-149">-ResourceId</span></span>
<span data-ttu-id="0578d-150">Identifierare för den resurs som händelse prenumerationer har skapats för.</span><span class="sxs-lookup"><span data-stu-id="0578d-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0578d-151">-TopicName</span></span>
<span data-ttu-id="0578d-152">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="0578d-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="0578d-153">-TopicTypeName</span></span>
<span data-ttu-id="0578d-154">TopicType namn</span><span class="sxs-lookup"><span data-stu-id="0578d-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0578d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0578d-155">CommonParameters</span></span>
<span data-ttu-id="0578d-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0578d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0578d-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0578d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0578d-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0578d-158">INPUTS</span></span>

### <span data-ttu-id="0578d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="0578d-159">System.String</span></span>

### <span data-ttu-id="0578d-160">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0578d-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0578d-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0578d-161">OUTPUTS</span></span>

### <span data-ttu-id="0578d-162">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0578d-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0578d-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0578d-163">NOTES</span></span>

## <span data-ttu-id="0578d-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0578d-164">RELATED LINKS</span></span>
