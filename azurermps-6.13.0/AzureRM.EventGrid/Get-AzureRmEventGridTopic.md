---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 2d18e923e14caf4c0048575465e9f52fb14596f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573974"
---
# <span data-ttu-id="3e555-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3e555-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="3e555-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e555-102">SYNOPSIS</span></span>
<span data-ttu-id="3e555-103">Hämtar information om ett ämne i händelse rutnätet eller hämtar en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e555-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e555-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e555-104">SYNTAX</span></span>

### <span data-ttu-id="3e555-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3e555-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e555-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e555-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e555-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e555-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e555-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e555-108">DESCRIPTION</span></span>
<span data-ttu-id="3e555-109">Get-AzureRmEventGridTopic-cmdleten får information om ett visst ämne i händelse rutnät, eller en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e555-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="3e555-110">Om ämnets namn är angivet returneras informationen om ett avsnitt med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="3e555-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="3e555-111">Om ämnets namn inte anges returneras en lista med avsnitt.</span><span class="sxs-lookup"><span data-stu-id="3e555-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="3e555-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e555-112">EXAMPLES</span></span>

### <span data-ttu-id="3e555-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e555-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3e555-114">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3e555-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3e555-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3e555-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="3e555-116">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3e555-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3e555-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3e555-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="3e555-118">Lista alla ämnen i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="3e555-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3e555-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3e555-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="3e555-120">Lista alla ämnen för händelse rutnät i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3e555-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="3e555-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e555-121">PARAMETERS</span></span>

### <span data-ttu-id="3e555-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e555-122">-DefaultProfile</span></span>
<span data-ttu-id="3e555-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3e555-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e555-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e555-124">-Name</span></span>
<span data-ttu-id="3e555-125">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="3e555-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="3e555-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e555-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e555-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3e555-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="3e555-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e555-128">-ResourceId</span></span>
<span data-ttu-id="3e555-129">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="3e555-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="3e555-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e555-130">CommonParameters</span></span>
<span data-ttu-id="3e555-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e555-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e555-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e555-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e555-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e555-133">INPUTS</span></span>

### <span data-ttu-id="3e555-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e555-134">System.String</span></span>

## <span data-ttu-id="3e555-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e555-135">OUTPUTS</span></span>

### <span data-ttu-id="3e555-136">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3e555-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="3e555-137">Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="3e555-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="3e555-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e555-138">NOTES</span></span>

## <span data-ttu-id="3e555-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e555-139">RELATED LINKS</span></span>
