---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: e9bb71d58627035d023b6fdc18fe4e515e728a7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919192"
---
# <span data-ttu-id="b856b-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b856b-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="b856b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b856b-102">SYNOPSIS</span></span>
<span data-ttu-id="b856b-103">Tar bort den angivna regeln för en given prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b856b-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="b856b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b856b-104">SYNTAX</span></span>

### <span data-ttu-id="b856b-105">RulePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b856b-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b856b-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b856b-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b856b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b856b-107">DESCRIPTION</span></span>
<span data-ttu-id="b856b-108">Cmdleten **Remove-AzServiceBusRule** tar bort regeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="b856b-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="b856b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b856b-109">EXAMPLES</span></span>

### <span data-ttu-id="b856b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b856b-110">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="b856b-111">Tar bort regeln `SBRule` för prenumeration `SBSubscription` av angivet ämne `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="b856b-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="b856b-112">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="b856b-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="b856b-113">Tar bort regeln som tillhandahålls via $inputobject parametern-InputObject</span><span class="sxs-lookup"><span data-stu-id="b856b-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="b856b-114">Exempel 2,2 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="b856b-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="b856b-115">Exempel 3,1-ResourceId-använder variabel</span><span class="sxs-lookup"><span data-stu-id="b856b-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="b856b-116">Exempel 3,1-ResourceId-använder sträng värde</span><span class="sxs-lookup"><span data-stu-id="b856b-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="b856b-117">Tar bort regeln via ARM-ID i $resourceid/String för parametern-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b856b-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="b856b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b856b-118">PARAMETERS</span></span>

### <span data-ttu-id="b856b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b856b-119">-AsJob</span></span>
<span data-ttu-id="b856b-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b856b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b856b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b856b-121">-DefaultProfile</span></span>
<span data-ttu-id="b856b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b856b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b856b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b856b-123">-Force</span></span>
<span data-ttu-id="b856b-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b856b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b856b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b856b-125">-InputObject</span></span>
<span data-ttu-id="b856b-126">Service Bus regel objekt</span><span class="sxs-lookup"><span data-stu-id="b856b-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="b856b-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="b856b-127">-Name</span></span>
<span data-ttu-id="b856b-128">Regel namn</span><span class="sxs-lookup"><span data-stu-id="b856b-128">Rule Name</span></span>

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

### <span data-ttu-id="b856b-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b856b-129">-Namespace</span></span>
<span data-ttu-id="b856b-130">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b856b-130">Namespace Name</span></span>

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

### <span data-ttu-id="b856b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b856b-131">-PassThru</span></span>
<span data-ttu-id="b856b-132">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="b856b-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b856b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b856b-133">-ResourceGroupName</span></span>
<span data-ttu-id="b856b-134">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b856b-134">The name of the resource group</span></span>

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

### <span data-ttu-id="b856b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b856b-135">-ResourceId</span></span>
<span data-ttu-id="b856b-136">Resurs-ID för Service Bus-regel</span><span class="sxs-lookup"><span data-stu-id="b856b-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="b856b-137">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="b856b-137">-Subscription</span></span>
<span data-ttu-id="b856b-138">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="b856b-138">Subscription Name</span></span>

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

### <span data-ttu-id="b856b-139">-Ämne</span><span class="sxs-lookup"><span data-stu-id="b856b-139">-Topic</span></span>
<span data-ttu-id="b856b-140">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="b856b-140">Topic Name</span></span>

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

### <span data-ttu-id="b856b-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b856b-141">-Confirm</span></span>
<span data-ttu-id="b856b-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b856b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b856b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b856b-143">-WhatIf</span></span>
<span data-ttu-id="b856b-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b856b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b856b-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b856b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b856b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b856b-146">CommonParameters</span></span>
<span data-ttu-id="b856b-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b856b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b856b-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b856b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b856b-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b856b-149">INPUTS</span></span>

### <span data-ttu-id="b856b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b856b-150">System.String</span></span>

### <span data-ttu-id="b856b-151">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b856b-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b856b-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b856b-152">OUTPUTS</span></span>

### <span data-ttu-id="b856b-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b856b-153">System.Boolean</span></span>

## <span data-ttu-id="b856b-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b856b-154">NOTES</span></span>

## <span data-ttu-id="b856b-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b856b-155">RELATED LINKS</span></span>
