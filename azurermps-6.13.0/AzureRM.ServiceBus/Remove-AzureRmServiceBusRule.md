---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577904"
---
# <span data-ttu-id="b0756-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b0756-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="b0756-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0756-102">SYNOPSIS</span></span>
<span data-ttu-id="b0756-103">Tar bort speficied-regeln för en given prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b0756-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0756-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0756-104">SYNTAX</span></span>

### <span data-ttu-id="b0756-105">RulePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b0756-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0756-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0756-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0756-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0756-107">DESCRIPTION</span></span>
<span data-ttu-id="b0756-108">Cmdleten **Remove-AzureRmServiceBusRule** tar bort regeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="b0756-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="b0756-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0756-109">EXAMPLES</span></span>

### <span data-ttu-id="b0756-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0756-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="b0756-111">Tar bort regeln `SBRule` för prenumeration `SBSubscription` av angivet ämne `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="b0756-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="b0756-112">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="b0756-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="b0756-113">Tar bort regeln som tillhandahålls via $inputobject parametern-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0756-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="b0756-114">Exempel 2,2 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="b0756-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="b0756-115">Exempel 3,1-ResourceId-använder variabel</span><span class="sxs-lookup"><span data-stu-id="b0756-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="b0756-116">Exempel 3,1-ResourceId-använder sträng värde</span><span class="sxs-lookup"><span data-stu-id="b0756-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="b0756-117">Tar bort regeln via ARM-ID i $resourceid/String för parametern-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0756-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="b0756-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0756-118">PARAMETERS</span></span>

### <span data-ttu-id="b0756-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0756-119">-AsJob</span></span>
<span data-ttu-id="b0756-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0756-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0756-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0756-121">-DefaultProfile</span></span>
<span data-ttu-id="b0756-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0756-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0756-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b0756-123">-Force</span></span>
<span data-ttu-id="b0756-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b0756-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b0756-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0756-125">-InputObject</span></span>
<span data-ttu-id="b0756-126">Service Bus regel objekt</span><span class="sxs-lookup"><span data-stu-id="b0756-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0756-127">-Name</span></span>
<span data-ttu-id="b0756-128">Regel namn</span><span class="sxs-lookup"><span data-stu-id="b0756-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b0756-129">-Namespace</span></span>
<span data-ttu-id="b0756-130">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b0756-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0756-131">-PassThru</span></span>
<span data-ttu-id="b0756-132">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="b0756-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b0756-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0756-133">-ResourceGroupName</span></span>
<span data-ttu-id="b0756-134">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b0756-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0756-135">-ResourceId</span></span>
<span data-ttu-id="b0756-136">Resurs-ID för Service Bus-regel</span><span class="sxs-lookup"><span data-stu-id="b0756-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-137">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="b0756-137">-Subscription</span></span>
<span data-ttu-id="b0756-138">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="b0756-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-139">-Ämne</span><span class="sxs-lookup"><span data-stu-id="b0756-139">-Topic</span></span>
<span data-ttu-id="b0756-140">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="b0756-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0756-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0756-141">-Confirm</span></span>
<span data-ttu-id="b0756-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0756-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0756-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0756-143">-WhatIf</span></span>
<span data-ttu-id="b0756-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0756-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0756-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0756-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0756-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0756-146">CommonParameters</span></span>
<span data-ttu-id="b0756-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0756-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0756-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0756-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0756-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0756-149">INPUTS</span></span>

### <span data-ttu-id="b0756-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b0756-150">System.String</span></span>

### <span data-ttu-id="b0756-151">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b0756-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="b0756-152">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0756-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b0756-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0756-153">OUTPUTS</span></span>

### <span data-ttu-id="b0756-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0756-154">System.Boolean</span></span>

## <span data-ttu-id="b0756-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0756-155">NOTES</span></span>

## <span data-ttu-id="b0756-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0756-156">RELATED LINKS</span></span>
