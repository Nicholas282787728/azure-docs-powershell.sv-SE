---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: a20262e1414b8f747e638f22283aed26b5483896
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578060"
---
# <span data-ttu-id="0ad41-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="0ad41-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="0ad41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ad41-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad41-103">Skapar ett nytt avsnitt i ett Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="0ad41-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ad41-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ad41-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad41-106">Skapar ett nytt avsnitt i ett Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="0ad41-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="0ad41-107">När du har skapat avsnittet kan ett program publicera händelser till Avsnittets slut punkt.</span><span class="sxs-lookup"><span data-stu-id="0ad41-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="0ad41-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ad41-108">EXAMPLES</span></span>

### <span data-ttu-id="0ad41-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ad41-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="0ad41-110">Skapar ett ämne \` \` för Ämne1 på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0ad41-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0ad41-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0ad41-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="0ad41-112">Skapar ett ämne \` \` för Ämne1 på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="0ad41-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="0ad41-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ad41-113">PARAMETERS</span></span>

### <span data-ttu-id="0ad41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad41-114">-DefaultProfile</span></span>
<span data-ttu-id="0ad41-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0ad41-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ad41-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="0ad41-116">-Location</span></span>
<span data-ttu-id="0ad41-117">Plats för ämnet</span><span class="sxs-lookup"><span data-stu-id="0ad41-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad41-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ad41-118">-Name</span></span>
<span data-ttu-id="0ad41-119">Namnet på ämnet.</span><span class="sxs-lookup"><span data-stu-id="0ad41-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad41-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ad41-121">Resurs gruppen där ämnet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0ad41-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad41-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0ad41-122">-Tag</span></span>
<span data-ttu-id="0ad41-123">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="0ad41-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad41-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ad41-124">-Confirm</span></span>
<span data-ttu-id="0ad41-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ad41-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad41-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad41-126">-WhatIf</span></span>
<span data-ttu-id="0ad41-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ad41-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad41-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ad41-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad41-129">CommonParameters</span></span>
<span data-ttu-id="0ad41-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad41-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad41-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad41-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ad41-132">INPUTS</span></span>

### <span data-ttu-id="0ad41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad41-133">System.String</span></span>

### <span data-ttu-id="0ad41-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0ad41-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ad41-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ad41-135">OUTPUTS</span></span>

### <span data-ttu-id="0ad41-136">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0ad41-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0ad41-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ad41-137">NOTES</span></span>

## <span data-ttu-id="0ad41-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ad41-138">RELATED LINKS</span></span>
