---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270684"
---
# <span data-ttu-id="eba1a-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="eba1a-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="eba1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eba1a-102">SYNOPSIS</span></span>
<span data-ttu-id="eba1a-103">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="eba1a-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="eba1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eba1a-104">SYNTAX</span></span>

### <span data-ttu-id="eba1a-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="eba1a-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba1a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eba1a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eba1a-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eba1a-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eba1a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eba1a-108">DESCRIPTION</span></span>
<span data-ttu-id="eba1a-109">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="eba1a-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="eba1a-110">Det kan användas för att ersätta taggarna i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="eba1a-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="eba1a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eba1a-111">EXAMPLES</span></span>

### <span data-ttu-id="eba1a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eba1a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="eba1a-113">Anger egenskaperna för avsnittet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` för att ersätta taggarna med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="eba1a-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="eba1a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eba1a-114">PARAMETERS</span></span>

### <span data-ttu-id="eba1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba1a-115">-DefaultProfile</span></span>
<span data-ttu-id="eba1a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eba1a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eba1a-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="eba1a-117">-InboundIpRule</span></span>
<span data-ttu-id="eba1a-118">Hash-adress som representerar listan med regler för inkommande IP.</span><span class="sxs-lookup"><span data-stu-id="eba1a-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="eba1a-119">Varje regel anger IP-adressen i CIDR-notation, till exempel 10.0.0.0/8 tillsammans med motsvarande åtgärd som ska utföras baserat på matchningen eller ingen matchning av IpMask.</span><span class="sxs-lookup"><span data-stu-id="eba1a-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="eba1a-120">Möjliga åtgärds värden inkluderar endast Tillåt</span><span class="sxs-lookup"><span data-stu-id="eba1a-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eba1a-121">-InputObject</span></span>
<span data-ttu-id="eba1a-122">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="eba1a-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="eba1a-123">-Name</span></span>
<span data-ttu-id="eba1a-124">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="eba1a-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="eba1a-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="eba1a-126">Det här avgör om trafik tillåts via offentliga nätverk.</span><span class="sxs-lookup"><span data-stu-id="eba1a-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="eba1a-127">Den är aktive rad som standard.</span><span class="sxs-lookup"><span data-stu-id="eba1a-127">By default it is enabled.</span></span> <span data-ttu-id="eba1a-128">Du kan ytterligare begränsa till specifika IP-adresser genom att konfigurera InboundIpRule-parametrar.</span><span class="sxs-lookup"><span data-stu-id="eba1a-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="eba1a-129">Tillåtna värden är inaktiverade och aktiverade.</span><span class="sxs-lookup"><span data-stu-id="eba1a-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba1a-130">-ResourceGroupName</span></span>
<span data-ttu-id="eba1a-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="eba1a-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eba1a-132">-ResourceId</span></span>
<span data-ttu-id="eba1a-133">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="eba1a-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="eba1a-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eba1a-134">-Tag</span></span>
<span data-ttu-id="eba1a-135">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="eba1a-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba1a-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eba1a-136">-Confirm</span></span>
<span data-ttu-id="eba1a-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eba1a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba1a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba1a-138">-WhatIf</span></span>
<span data-ttu-id="eba1a-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eba1a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba1a-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eba1a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba1a-141">CommonParameters</span></span>
<span data-ttu-id="eba1a-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba1a-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba1a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba1a-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eba1a-144">INPUTS</span></span>

### <span data-ttu-id="eba1a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="eba1a-145">System.String</span></span>

### <span data-ttu-id="eba1a-146">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="eba1a-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="eba1a-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="eba1a-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eba1a-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eba1a-148">OUTPUTS</span></span>

### <span data-ttu-id="eba1a-149">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="eba1a-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="eba1a-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eba1a-150">NOTES</span></span>

## <span data-ttu-id="eba1a-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eba1a-151">RELATED LINKS</span></span>
