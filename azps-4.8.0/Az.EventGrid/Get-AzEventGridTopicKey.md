---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102869"
---
# <span data-ttu-id="5c8a0-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="5c8a0-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="5c8a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8a0-103">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5c8a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c8a0-104">SYNTAX</span></span>

### <span data-ttu-id="5c8a0-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5c8a0-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8a0-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c8a0-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c8a0-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c8a0-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c8a0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c8a0-108">DESCRIPTION</span></span>
<span data-ttu-id="5c8a0-109">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5c8a0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c8a0-110">EXAMPLES</span></span>

### <span data-ttu-id="5c8a0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c8a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5c8a0-112">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="5c8a0-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5c8a0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5c8a0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="5c8a0-114">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="5c8a0-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5c8a0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c8a0-115">PARAMETERS</span></span>

### <span data-ttu-id="5c8a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8a0-116">-DefaultProfile</span></span>
<span data-ttu-id="5c8a0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5c8a0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c8a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c8a0-118">-InputObject</span></span>
<span data-ttu-id="5c8a0-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5c8a0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c8a0-120">-Name</span></span>
<span data-ttu-id="5c8a0-121">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="5c8a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c8a0-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c8a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8a0-124">-ResourceId</span></span>
<span data-ttu-id="5c8a0-125">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5c8a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8a0-126">CommonParameters</span></span>
<span data-ttu-id="5c8a0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8a0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c8a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8a0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c8a0-129">INPUTS</span></span>

### <span data-ttu-id="5c8a0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c8a0-130">System.String</span></span>

### <span data-ttu-id="5c8a0-131">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5c8a0-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5c8a0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c8a0-132">OUTPUTS</span></span>

### <span data-ttu-id="5c8a0-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5c8a0-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="5c8a0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c8a0-134">NOTES</span></span>

## <span data-ttu-id="5c8a0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c8a0-135">RELATED LINKS</span></span>