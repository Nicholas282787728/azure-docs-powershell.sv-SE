---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758092"
---
# <span data-ttu-id="3b3e6-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="3b3e6-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="3b3e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3e6-103">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b3e6-104">SYNTAX</span></span>

### <span data-ttu-id="3b3e6-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3b3e6-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b3e6-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b3e6-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3e6-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b3e6-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3e6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b3e6-108">DESCRIPTION</span></span>
<span data-ttu-id="3b3e6-109">Hämtar de delade åtkomst nycklarna som används för att publicera händelser i ett ämne i händelse rutnätet.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="3b3e6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b3e6-110">EXAMPLES</span></span>

### <span data-ttu-id="3b3e6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b3e6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3b3e6-112">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="3b3e6-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3b3e6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3b3e6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="3b3e6-114">Hämtar de delade snabb tangenterna i avsnittet \` Ämne1 \` i MyResourceGroupName i resurs \` gruppen \` .</span><span class="sxs-lookup"><span data-stu-id="3b3e6-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3b3e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b3e6-115">PARAMETERS</span></span>

### <span data-ttu-id="3b3e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b3e6-116">-InputObject</span></span>
<span data-ttu-id="3b3e6-117">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="3b3e6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b3e6-118">-Name</span></span>
<span data-ttu-id="3b3e6-119">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="3b3e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b3e6-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="3b3e6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3e6-122">-ResourceId</span></span>
<span data-ttu-id="3b3e6-123">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="3b3e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3e6-124">-DefaultProfile</span></span>
<span data-ttu-id="3b3e6-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3e6-126">CommonParameters</span></span>
<span data-ttu-id="3b3e6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3e6-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3e6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3e6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b3e6-129">INPUTS</span></span>

### <span data-ttu-id="3b3e6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3e6-130">System.String</span></span>

## <span data-ttu-id="3b3e6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b3e6-131">OUTPUTS</span></span>

### <span data-ttu-id="3b3e6-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3b3e6-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="3b3e6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b3e6-133">NOTES</span></span>

## <span data-ttu-id="3b3e6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b3e6-134">RELATED LINKS</span></span>

