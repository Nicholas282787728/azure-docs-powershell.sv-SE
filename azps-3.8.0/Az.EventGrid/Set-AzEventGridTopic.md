---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088659"
---
# <span data-ttu-id="8b4e6-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8b4e6-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="8b4e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4e6-103">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="8b4e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b4e6-104">SYNTAX</span></span>

### <span data-ttu-id="8b4e6-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b4e6-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4e6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4e6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4e6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4e6-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4e6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b4e6-108">DESCRIPTION</span></span>
<span data-ttu-id="8b4e6-109">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="8b4e6-110">Det kan användas för att ersätta taggarna i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="8b4e6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b4e6-111">EXAMPLES</span></span>

### <span data-ttu-id="8b4e6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b4e6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="8b4e6-113">Anger egenskaperna för avsnittet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` för att ersätta taggarna med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="8b4e6-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="8b4e6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b4e6-114">PARAMETERS</span></span>

### <span data-ttu-id="8b4e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4e6-115">-DefaultProfile</span></span>
<span data-ttu-id="8b4e6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8b4e6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b4e6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b4e6-117">-InputObject</span></span>
<span data-ttu-id="8b4e6-118">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8b4e6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b4e6-119">-Name</span></span>
<span data-ttu-id="8b4e6-120">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="8b4e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b4e6-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b4e6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b4e6-123">-ResourceId</span></span>
<span data-ttu-id="8b4e6-124">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="8b4e6-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8b4e6-125">-Tag</span></span>
<span data-ttu-id="8b4e6-126">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="8b4e6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b4e6-127">-Confirm</span></span>
<span data-ttu-id="8b4e6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4e6-129">-WhatIf</span></span>
<span data-ttu-id="8b4e6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4e6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4e6-132">CommonParameters</span></span>
<span data-ttu-id="8b4e6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4e6-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4e6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4e6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b4e6-135">INPUTS</span></span>

### <span data-ttu-id="8b4e6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8b4e6-136">System.String</span></span>

### <span data-ttu-id="8b4e6-137">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8b4e6-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8b4e6-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8b4e6-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b4e6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b4e6-139">OUTPUTS</span></span>

### <span data-ttu-id="8b4e6-140">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8b4e6-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8b4e6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b4e6-141">NOTES</span></span>

## <span data-ttu-id="8b4e6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b4e6-142">RELATED LINKS</span></span>
