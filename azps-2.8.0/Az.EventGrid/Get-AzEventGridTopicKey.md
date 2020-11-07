---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b39f9c3c3c1d72624c612d2743b32d306eefa131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744257"
---
# <span data-ttu-id="d6fec-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d6fec-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="d6fec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6fec-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fec-103">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="d6fec-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="d6fec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6fec-104">SYNTAX</span></span>

### <span data-ttu-id="d6fec-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d6fec-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6fec-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6fec-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6fec-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6fec-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6fec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6fec-108">DESCRIPTION</span></span>
<span data-ttu-id="d6fec-109">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="d6fec-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="d6fec-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6fec-110">EXAMPLES</span></span>

### <span data-ttu-id="d6fec-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6fec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="d6fec-112">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="d6fec-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d6fec-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d6fec-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="d6fec-114">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="d6fec-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d6fec-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6fec-115">PARAMETERS</span></span>

### <span data-ttu-id="d6fec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fec-116">-DefaultProfile</span></span>
<span data-ttu-id="d6fec-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d6fec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6fec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6fec-118">-InputObject</span></span>
<span data-ttu-id="d6fec-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="d6fec-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d6fec-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6fec-120">-Name</span></span>
<span data-ttu-id="d6fec-121">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="d6fec-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="d6fec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fec-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6fec-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d6fec-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6fec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fec-124">-ResourceId</span></span>
<span data-ttu-id="d6fec-125">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="d6fec-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d6fec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fec-126">CommonParameters</span></span>
<span data-ttu-id="d6fec-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6fec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fec-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fec-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6fec-129">INPUTS</span></span>

### <span data-ttu-id="d6fec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6fec-130">System.String</span></span>

### <span data-ttu-id="d6fec-131">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d6fec-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d6fec-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6fec-132">OUTPUTS</span></span>

### <span data-ttu-id="d6fec-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d6fec-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d6fec-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6fec-134">NOTES</span></span>

## <span data-ttu-id="d6fec-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6fec-135">RELATED LINKS</span></span>
