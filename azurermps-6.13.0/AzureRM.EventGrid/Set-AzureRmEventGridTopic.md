---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578048"
---
# <span data-ttu-id="a70d0-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a70d0-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="a70d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a70d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a70d0-103">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="a70d0-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a70d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a70d0-104">SYNTAX</span></span>

### <span data-ttu-id="a70d0-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a70d0-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70d0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a70d0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70d0-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a70d0-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a70d0-108">DESCRIPTION</span></span>
<span data-ttu-id="a70d0-109">Anger egenskaperna för ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="a70d0-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="a70d0-110">Det kan användas för att ersätta taggarna i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="a70d0-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="a70d0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a70d0-111">EXAMPLES</span></span>

### <span data-ttu-id="a70d0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a70d0-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a70d0-113">Anger egenskaperna för avsnittet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` för att ersätta taggarna med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="a70d0-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a70d0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a70d0-114">PARAMETERS</span></span>

### <span data-ttu-id="a70d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70d0-115">-DefaultProfile</span></span>
<span data-ttu-id="a70d0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a70d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a70d0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a70d0-117">-InputObject</span></span>
<span data-ttu-id="a70d0-118">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="a70d0-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a70d0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a70d0-119">-Name</span></span>
<span data-ttu-id="a70d0-120">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="a70d0-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a70d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="a70d0-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a70d0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="a70d0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a70d0-123">-ResourceId</span></span>
<span data-ttu-id="a70d0-124">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a70d0-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="a70d0-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a70d0-125">-Tag</span></span>
<span data-ttu-id="a70d0-126">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="a70d0-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70d0-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a70d0-127">-Confirm</span></span>
<span data-ttu-id="a70d0-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a70d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70d0-129">-WhatIf</span></span>
<span data-ttu-id="a70d0-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a70d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70d0-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a70d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70d0-132">CommonParameters</span></span>
<span data-ttu-id="a70d0-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70d0-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70d0-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a70d0-135">INPUTS</span></span>

### <span data-ttu-id="a70d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a70d0-136">System.String</span></span>

### <span data-ttu-id="a70d0-137">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a70d0-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="a70d0-138">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a70d0-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a70d0-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a70d0-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a70d0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a70d0-140">OUTPUTS</span></span>

### <span data-ttu-id="a70d0-141">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a70d0-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a70d0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a70d0-142">NOTES</span></span>

## <span data-ttu-id="a70d0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a70d0-143">RELATED LINKS</span></span>
