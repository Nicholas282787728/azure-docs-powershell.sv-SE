---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758445"
---
# <span data-ttu-id="3d6a8-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3d6a8-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="3d6a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6a8-103">Hämtar information om ett ämne i händelse rutnätet eller hämtar en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d6a8-104">SYNTAX</span></span>

### <span data-ttu-id="3d6a8-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d6a8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d6a8-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6a8-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d6a8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6a8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6a8-109">Get-AzureRmEventGridTopic-cmdleten får information om ett visst ämne i händelse rutnät, eller en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="3d6a8-110">Om ämnets namn är angivet returneras informationen om ett avsnitt med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="3d6a8-111">Om ämnets namn inte anges returneras en lista med avsnitt.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="3d6a8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d6a8-112">EXAMPLES</span></span>

### <span data-ttu-id="3d6a8-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d6a8-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3d6a8-114">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3d6a8-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3d6a8-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d6a8-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="3d6a8-116">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3d6a8-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3d6a8-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3d6a8-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="3d6a8-118">Lista alla ämnen i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3d6a8-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3d6a8-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3d6a8-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="3d6a8-120">Lista alla ämnen för händelse rutnät i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="3d6a8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d6a8-121">PARAMETERS</span></span>

### <span data-ttu-id="3d6a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6a8-122">-DefaultProfile</span></span>
<span data-ttu-id="3d6a8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d6a8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d6a8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d6a8-124">-Name</span></span>
<span data-ttu-id="3d6a8-125">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-125">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d6a8-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="3d6a8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d6a8-128">-ResourceId</span></span>
<span data-ttu-id="3d6a8-129">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="3d6a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6a8-130">CommonParameters</span></span>
<span data-ttu-id="3d6a8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6a8-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6a8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6a8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d6a8-133">INPUTS</span></span>

### <span data-ttu-id="3d6a8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6a8-134">System.String</span></span>
<span data-ttu-id="3d6a8-135">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3d6a8-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="3d6a8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d6a8-136">OUTPUTS</span></span>

### <span data-ttu-id="3d6a8-137">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3d6a8-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="3d6a8-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. commands. EventGrid, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3d6a8-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3d6a8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d6a8-139">NOTES</span></span>

## <span data-ttu-id="3d6a8-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d6a8-140">RELATED LINKS</span></span>

