---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: a6f821f094594fb00863f5dce2134f6702cfa8e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583172"
---
# <span data-ttu-id="ddcc5-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ddcc5-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="ddcc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcc5-103">Hämtar information om en händelse prenumeration eller hämtar en lista över alla händelse prenumerationer i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddcc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddcc5-104">SYNTAX</span></span>

### <span data-ttu-id="ddcc5-105">EventSubscriptionTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ddcc5-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddcc5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddcc5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddcc5-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddcc5-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddcc5-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ddcc5-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddcc5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddcc5-109">DESCRIPTION</span></span>
<span data-ttu-id="ddcc5-110">Get-AzureRmEventGridSubscription-cmdleten får antingen information om ett angivet abonnemang för händelse rutnät eller en lista över alla prenumerationer i det aktuella Azure-abonnemanget eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="ddcc5-111">Om händelse prenumerationens namn anges returneras informationen om ett enskilt rutnäts abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="ddcc5-112">Om händelse prenumerationens namn inte anges returneras en lista över alla händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="ddcc5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddcc5-113">EXAMPLES</span></span>

### <span data-ttu-id="ddcc5-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddcc5-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ddcc5-115">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ddcc5-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ddcc5-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="ddcc5-117">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` , inklusive fullständig slut punkts-URL om det är en webhook-baserad händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="ddcc5-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ddcc5-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="ddcc5-119">Få en lista över alla händelse prenumerationer som har skapats för ämnet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ddcc5-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ddcc5-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ddcc5-121">Hämtar information om händelse prenumerations \` EventSubscription1 \` som har skapats för resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ddcc5-122">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="ddcc5-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ddcc5-123">Hämtar information om \` EventSubscription1 som \` skapats för den valda Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="ddcc5-124">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="ddcc5-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ddcc5-125">Hämtar listan över alla globala händelse prenumerationer som skapas under resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ddcc5-126">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="ddcc5-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="ddcc5-127">Hämtar listan över alla globala händelse prenumerationer som har skapats under det markerade Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="ddcc5-128">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="ddcc5-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="ddcc5-129">Hämtar listan över alla regionala händelse prenumerationer som skapats under resurs grupp \` MyResourceGroupName \` på den angivna platsen \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="ddcc5-130">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="ddcc5-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="ddcc5-131">Hämtar listan över alla händelse prenumerationer som har skapats för det angivna EventHub-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="ddcc5-132">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="ddcc5-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="ddcc5-133">Hämtar listan över alla händelse prenumerationer som har skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="ddcc5-134">Exempel 11</span><span class="sxs-lookup"><span data-stu-id="ddcc5-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ddcc5-135">Hämtar listan över alla händelse prenumerationer som har skapats för den specifika resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="ddcc5-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddcc5-136">PARAMETERS</span></span>

### <span data-ttu-id="ddcc5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcc5-137">-DefaultProfile</span></span>
<span data-ttu-id="ddcc5-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ddcc5-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ddcc5-139">-EventSubscriptionName</span></span>
<span data-ttu-id="ddcc5-140">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="ddcc5-140">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ddcc5-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="ddcc5-142">Ange fullständig slut punkts-URL för händelse prenumerationens destination.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddcc5-143">-InputObject</span></span>
<span data-ttu-id="ddcc5-144">EventGrid händelse prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-144">EventGrid Event Subscription object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="ddcc5-145">-Location</span></span>
<span data-ttu-id="ddcc5-146">Plats</span><span class="sxs-lookup"><span data-stu-id="ddcc5-146">Location</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddcc5-147">-ResourceGroupName</span></span>
<span data-ttu-id="ddcc5-148">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-148">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddcc5-149">-ResourceId</span></span>
<span data-ttu-id="ddcc5-150">Identifierare för den resurs som händelse prenumerationer har skapats för.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ddcc5-151">-TopicName</span></span>
<span data-ttu-id="ddcc5-152">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-152">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="ddcc5-153">-TopicTypeName</span></span>
<span data-ttu-id="ddcc5-154">TopicType namn</span><span class="sxs-lookup"><span data-stu-id="ddcc5-154">TopicType name</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcc5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcc5-155">CommonParameters</span></span>
<span data-ttu-id="ddcc5-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcc5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcc5-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcc5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcc5-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddcc5-158">INPUTS</span></span>

### <span data-ttu-id="ddcc5-159">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcc5-159">System.String</span></span>
<span data-ttu-id="ddcc5-160">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription system. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddcc5-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ddcc5-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddcc5-161">OUTPUTS</span></span>

### <span data-ttu-id="ddcc5-162">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ddcc5-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="ddcc5-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventGrid. Models. PSEventSubscriptionListInstance, Microsoft. Azure. commands. EventGrid, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddcc5-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ddcc5-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddcc5-164">NOTES</span></span>

## <span data-ttu-id="ddcc5-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddcc5-165">RELATED LINKS</span></span>

