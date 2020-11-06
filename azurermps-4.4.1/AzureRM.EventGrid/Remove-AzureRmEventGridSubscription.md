---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585628"
---
# <span data-ttu-id="05b58-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="05b58-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="05b58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05b58-102">SYNOPSIS</span></span>
<span data-ttu-id="05b58-103">Tar bort en händelse prenumeration för ett Azure Event Grid-evenemang.</span><span class="sxs-lookup"><span data-stu-id="05b58-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05b58-104">SYNTAX</span></span>

### <span data-ttu-id="05b58-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="05b58-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b58-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b58-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b58-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05b58-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b58-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b58-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05b58-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05b58-109">DESCRIPTION</span></span>
<span data-ttu-id="05b58-110">Tar bort en händelse prenumeration i Azure Events Grid-avsnitt, en resurs, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="05b58-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="05b58-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05b58-111">EXAMPLES</span></span>

### <span data-ttu-id="05b58-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05b58-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05b58-113">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="05b58-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="05b58-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="05b58-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05b58-115">Tar bort \` EventSubscription1 för händelser \` till en resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="05b58-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="05b58-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="05b58-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05b58-117">Tar bort \` EventSubscription1 för händelser \` till standard Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="05b58-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="05b58-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="05b58-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05b58-119">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett namn område i en händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="05b58-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="05b58-120">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="05b58-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05b58-121">Tar bort händelse abonnemanget \` EventSubscription1 \` till ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="05b58-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="05b58-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05b58-122">PARAMETERS</span></span>

### <span data-ttu-id="05b58-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="05b58-123">-EventSubscriptionName</span></span>
<span data-ttu-id="05b58-124">Namnet på den händelse prenumeration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="05b58-124">Name of the event subscription that needs to be removed.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b58-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05b58-125">-InputObject</span></span>
<span data-ttu-id="05b58-126">EventGrid EventSubscription-objekt.</span><span class="sxs-lookup"><span data-stu-id="05b58-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05b58-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05b58-127">-PassThru</span></span>
<span data-ttu-id="05b58-128">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="05b58-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="05b58-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="05b58-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05b58-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b58-130">-ResourceGroupName</span></span>
<span data-ttu-id="05b58-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="05b58-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="05b58-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05b58-132">-ResourceId</span></span>
<span data-ttu-id="05b58-133">Identifierare för den resurs vars händelse prenumeration måste tas bort.</span><span class="sxs-lookup"><span data-stu-id="05b58-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="05b58-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="05b58-134">-TopicName</span></span>
<span data-ttu-id="05b58-135">Avsnitts namn i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="05b58-135">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="05b58-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05b58-136">-Confirm</span></span>
<span data-ttu-id="05b58-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05b58-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b58-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b58-138">-WhatIf</span></span>
<span data-ttu-id="05b58-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05b58-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b58-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05b58-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b58-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b58-141">-DefaultProfile</span></span>
<span data-ttu-id="05b58-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05b58-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05b58-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b58-143">CommonParameters</span></span>
<span data-ttu-id="05b58-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b58-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b58-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b58-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b58-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05b58-146">INPUTS</span></span>

### <span data-ttu-id="05b58-147">System. String</span><span class="sxs-lookup"><span data-stu-id="05b58-147">System.String</span></span>
<span data-ttu-id="05b58-148">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="05b58-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="05b58-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05b58-149">OUTPUTS</span></span>

### <span data-ttu-id="05b58-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="05b58-150">System.Object</span></span>

## <span data-ttu-id="05b58-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05b58-151">NOTES</span></span>

## <span data-ttu-id="05b58-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05b58-152">RELATED LINKS</span></span>

