---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586599"
---
# <span data-ttu-id="51fe7-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="51fe7-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="51fe7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="51fe7-103">Återskapar den delade åtkomst-nyckeln för ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="51fe7-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51fe7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51fe7-104">SYNTAX</span></span>

### <span data-ttu-id="51fe7-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51fe7-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51fe7-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51fe7-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51fe7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51fe7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fe7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="51fe7-109">Återskapar den delade åtkomst-nyckeln för ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="51fe7-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="51fe7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="51fe7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51fe7-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="51fe7-112">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of topic \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51fe7-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="51fe7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51fe7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="51fe7-114">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of topic \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51fe7-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="51fe7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51fe7-115">PARAMETERS</span></span>

### <span data-ttu-id="51fe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fe7-116">-DefaultProfile</span></span>
<span data-ttu-id="51fe7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="51fe7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fe7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51fe7-118">-InputObject</span></span>
<span data-ttu-id="51fe7-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="51fe7-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="51fe7-120">-KeyName</span></span>
<span data-ttu-id="51fe7-121">Namnet på den nyckeln som måste återskapas</span><span class="sxs-lookup"><span data-stu-id="51fe7-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fe7-122">-ResourceGroupName</span></span>
<span data-ttu-id="51fe7-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51fe7-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51fe7-124">-ResourceId</span></span>
<span data-ttu-id="51fe7-125">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="51fe7-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="51fe7-126">-TopicName</span></span>
<span data-ttu-id="51fe7-127">Namnet på ämnet.</span><span class="sxs-lookup"><span data-stu-id="51fe7-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51fe7-128">-Confirm</span></span>
<span data-ttu-id="51fe7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51fe7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fe7-130">-WhatIf</span></span>
<span data-ttu-id="51fe7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51fe7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fe7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51fe7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fe7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fe7-133">CommonParameters</span></span>
<span data-ttu-id="51fe7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51fe7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fe7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fe7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fe7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51fe7-136">INPUTS</span></span>

### <span data-ttu-id="51fe7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="51fe7-137">System.String</span></span>

## <span data-ttu-id="51fe7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51fe7-138">OUTPUTS</span></span>

### <span data-ttu-id="51fe7-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="51fe7-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="51fe7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51fe7-140">NOTES</span></span>

## <span data-ttu-id="51fe7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51fe7-141">RELATED LINKS</span></span>

