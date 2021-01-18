---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525489"
---
# <span data-ttu-id="6df27-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="6df27-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="6df27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6df27-102">SYNOPSIS</span></span>
<span data-ttu-id="6df27-103">Tar bort abonnemanget till ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="6df27-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6df27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6df27-104">SYNTAX</span></span>

### <span data-ttu-id="6df27-105">SubscriptionPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6df27-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6df27-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6df27-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df27-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6df27-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df27-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6df27-108">DESCRIPTION</span></span>
<span data-ttu-id="6df27-109">Cmdleten **Remove-AzServiceBusSubscription** tar bort prenumerationen på ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="6df27-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6df27-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6df27-110">EXAMPLES</span></span>

### <span data-ttu-id="6df27-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6df27-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="6df27-112">Tar bort abonnemanget `SB-TopicSubscription-Example1` till avsnittet `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6df27-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6df27-113">Exempel 2: InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="6df27-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="6df27-114">Exempel 3: InputObject-använder rör:</span><span class="sxs-lookup"><span data-stu-id="6df27-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="6df27-115">Exempel 4: ResourceId-använder variabel:</span><span class="sxs-lookup"><span data-stu-id="6df27-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="6df27-116">Exempel 5: ResourceId-använder sträng värde:</span><span class="sxs-lookup"><span data-stu-id="6df27-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="6df27-117">Tar bort prenumerationen via ARM-ID i $resourceid/String för parametern-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df27-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="6df27-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6df27-118">PARAMETERS</span></span>

### <span data-ttu-id="6df27-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6df27-119">-AsJob</span></span>
<span data-ttu-id="6df27-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6df27-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6df27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df27-121">-DefaultProfile</span></span>
<span data-ttu-id="6df27-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6df27-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df27-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6df27-123">-InputObject</span></span>
<span data-ttu-id="6df27-124">Service Bus abonnemang-objekt</span><span class="sxs-lookup"><span data-stu-id="6df27-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6df27-125">-Name</span></span>
<span data-ttu-id="6df27-126">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="6df27-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6df27-127">-Namespace</span></span>
<span data-ttu-id="6df27-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="6df27-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6df27-129">-PassThru</span></span>
<span data-ttu-id="6df27-130">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="6df27-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6df27-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df27-131">-ResourceGroupName</span></span>
<span data-ttu-id="6df27-132">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6df27-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df27-133">-ResourceId</span></span>
<span data-ttu-id="6df27-134">Resurs-ID för Service Bus-prenumeration</span><span class="sxs-lookup"><span data-stu-id="6df27-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-135">-Ämne</span><span class="sxs-lookup"><span data-stu-id="6df27-135">-Topic</span></span>
<span data-ttu-id="6df27-136">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="6df27-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df27-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6df27-137">-Confirm</span></span>
<span data-ttu-id="6df27-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6df27-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df27-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df27-139">-WhatIf</span></span>
<span data-ttu-id="6df27-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6df27-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df27-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6df27-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df27-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df27-142">CommonParameters</span></span>
<span data-ttu-id="6df27-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df27-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df27-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df27-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df27-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6df27-145">INPUTS</span></span>

### <span data-ttu-id="6df27-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6df27-146">System.String</span></span>

### <span data-ttu-id="6df27-147">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="6df27-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="6df27-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6df27-148">OUTPUTS</span></span>

### <span data-ttu-id="6df27-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6df27-149">System.Boolean</span></span>

## <span data-ttu-id="6df27-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6df27-150">NOTES</span></span>

## <span data-ttu-id="6df27-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6df27-151">RELATED LINKS</span></span>
