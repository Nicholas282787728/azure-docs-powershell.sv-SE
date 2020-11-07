---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8532e8411f474f769a4e9686ef89bf499f4f0272
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754095"
---
# <span data-ttu-id="6f8c9-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="6f8c9-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="6f8c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8c9-103">Återskapar den delade åtkomst-nyckeln för ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6f8c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f8c9-104">SYNTAX</span></span>

### <span data-ttu-id="6f8c9-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f8c9-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8c9-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8c9-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8c9-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8c9-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8c9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f8c9-108">DESCRIPTION</span></span>
<span data-ttu-id="6f8c9-109">Återskapar den delade åtkomst-nyckeln för ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6f8c9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-110">EXAMPLES</span></span>

### <span data-ttu-id="6f8c9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f8c9-111">Example 1</span></span>
```
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="6f8c9-112">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of topic \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6f8c9-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6f8c9-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6f8c9-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="6f8c9-114">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of topic \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6f8c9-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6f8c9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f8c9-115">PARAMETERS</span></span>

### <span data-ttu-id="6f8c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8c9-116">-DefaultProfile</span></span>
<span data-ttu-id="6f8c9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f8c9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f8c9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f8c9-118">-InputObject</span></span>
<span data-ttu-id="6f8c9-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6f8c9-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f8c9-120">-KeyName</span></span>
<span data-ttu-id="6f8c9-121">Namnet på den nyckeln som måste återskapas</span><span class="sxs-lookup"><span data-stu-id="6f8c9-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f8c9-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-123">Resource group name.</span></span>

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

### <span data-ttu-id="6f8c9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8c9-124">-ResourceId</span></span>
<span data-ttu-id="6f8c9-125">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="6f8c9-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6f8c9-126">-TopicName</span></span>
<span data-ttu-id="6f8c9-127">Namnet på ämnet.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8c9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f8c9-128">-Confirm</span></span>
<span data-ttu-id="6f8c9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8c9-130">-WhatIf</span></span>
<span data-ttu-id="6f8c9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8c9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8c9-133">CommonParameters</span></span>
<span data-ttu-id="6f8c9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8c9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8c9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-136">INPUTS</span></span>

### <span data-ttu-id="6f8c9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8c9-137">System.String</span></span>

### <span data-ttu-id="6f8c9-138">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="6f8c9-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6f8c9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f8c9-139">OUTPUTS</span></span>

### <span data-ttu-id="6f8c9-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6f8c9-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="6f8c9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f8c9-141">NOTES</span></span>

## <span data-ttu-id="6f8c9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f8c9-142">RELATED LINKS</span></span>
