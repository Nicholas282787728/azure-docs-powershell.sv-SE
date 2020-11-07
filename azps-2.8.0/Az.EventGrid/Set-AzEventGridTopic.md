---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: f27533a36314ae2b31cd0055e8cc17027c95016a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744233"
---
# <span data-ttu-id="72909-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="72909-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="72909-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72909-102">SYNOPSIS</span></span>
<span data-ttu-id="72909-103">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="72909-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="72909-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72909-104">SYNTAX</span></span>

### <span data-ttu-id="72909-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72909-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72909-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="72909-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72909-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72909-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72909-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72909-108">DESCRIPTION</span></span>
<span data-ttu-id="72909-109">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="72909-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="72909-110">Det kan användas för att ersätta taggarna i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="72909-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="72909-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72909-111">EXAMPLES</span></span>

### <span data-ttu-id="72909-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72909-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="72909-113">Anger egenskaperna för avsnittet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` för att ersätta taggarna med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="72909-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="72909-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72909-114">PARAMETERS</span></span>

### <span data-ttu-id="72909-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72909-115">-DefaultProfile</span></span>
<span data-ttu-id="72909-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72909-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72909-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72909-117">-InputObject</span></span>
<span data-ttu-id="72909-118">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="72909-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="72909-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="72909-119">-Name</span></span>
<span data-ttu-id="72909-120">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="72909-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="72909-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72909-121">-ResourceGroupName</span></span>
<span data-ttu-id="72909-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="72909-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="72909-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72909-123">-ResourceId</span></span>
<span data-ttu-id="72909-124">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="72909-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="72909-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="72909-125">-Tag</span></span>
<span data-ttu-id="72909-126">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="72909-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="72909-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72909-127">-Confirm</span></span>
<span data-ttu-id="72909-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72909-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72909-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72909-129">-WhatIf</span></span>
<span data-ttu-id="72909-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72909-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72909-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72909-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72909-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72909-132">CommonParameters</span></span>
<span data-ttu-id="72909-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72909-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72909-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72909-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72909-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72909-135">INPUTS</span></span>

### <span data-ttu-id="72909-136">System. String</span><span class="sxs-lookup"><span data-stu-id="72909-136">System.String</span></span>

### <span data-ttu-id="72909-137">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="72909-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="72909-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="72909-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72909-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72909-139">OUTPUTS</span></span>

### <span data-ttu-id="72909-140">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="72909-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="72909-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72909-141">NOTES</span></span>

## <span data-ttu-id="72909-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72909-142">RELATED LINKS</span></span>
