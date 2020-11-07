---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 8bd28b3bbe043663a451b235abf46c3a42e235e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757892"
---
# <span data-ttu-id="311a9-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="311a9-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="311a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="311a9-102">SYNOPSIS</span></span>
<span data-ttu-id="311a9-103">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="311a9-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="311a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="311a9-104">SYNTAX</span></span>

### <span data-ttu-id="311a9-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="311a9-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="311a9-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311a9-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="311a9-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="311a9-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="311a9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="311a9-108">DESCRIPTION</span></span>
<span data-ttu-id="311a9-109">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="311a9-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="311a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="311a9-110">EXAMPLES</span></span>

### <span data-ttu-id="311a9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="311a9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="311a9-112">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="311a9-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="311a9-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="311a9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="311a9-114">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="311a9-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="311a9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="311a9-115">PARAMETERS</span></span>

### <span data-ttu-id="311a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311a9-116">-DefaultProfile</span></span>
<span data-ttu-id="311a9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="311a9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="311a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="311a9-118">-InputObject</span></span>
<span data-ttu-id="311a9-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="311a9-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="311a9-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="311a9-120">-Name</span></span>
<span data-ttu-id="311a9-121">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="311a9-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="311a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="311a9-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="311a9-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="311a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="311a9-124">-ResourceId</span></span>
<span data-ttu-id="311a9-125">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="311a9-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="311a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311a9-126">CommonParameters</span></span>
<span data-ttu-id="311a9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311a9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311a9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="311a9-129">INPUTS</span></span>

### <span data-ttu-id="311a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="311a9-130">System.String</span></span>

### <span data-ttu-id="311a9-131">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="311a9-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="311a9-132">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="311a9-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="311a9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="311a9-133">OUTPUTS</span></span>

### <span data-ttu-id="311a9-134">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="311a9-134">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="311a9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="311a9-135">NOTES</span></span>

## <span data-ttu-id="311a9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="311a9-136">RELATED LINKS</span></span>
