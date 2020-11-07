---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 1922d399cf4b7c4fe1295f9a19409094ab5676c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754099"
---
# <span data-ttu-id="578b2-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="578b2-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="578b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="578b2-102">SYNOPSIS</span></span>
<span data-ttu-id="578b2-103">Skapar ett nytt avsnitt i ett Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="578b2-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="578b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="578b2-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="578b2-105">DESCRIPTION</span></span>
<span data-ttu-id="578b2-106">Skapar ett nytt avsnitt i ett Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="578b2-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="578b2-107">När du har skapat avsnittet kan ett program publicera händelser till Avsnittets slut punkt.</span><span class="sxs-lookup"><span data-stu-id="578b2-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="578b2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="578b2-108">EXAMPLES</span></span>

### <span data-ttu-id="578b2-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="578b2-109">Example 1</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="578b2-110">Skapar ett ämne \` \` för Ämne1 på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="578b2-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="578b2-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="578b2-111">Example 2</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="578b2-112">Skapar ett ämne \` \` för Ämne1 på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="578b2-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="578b2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="578b2-113">PARAMETERS</span></span>

### <span data-ttu-id="578b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578b2-114">-DefaultProfile</span></span>
<span data-ttu-id="578b2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="578b2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="578b2-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="578b2-116">-Location</span></span>
<span data-ttu-id="578b2-117">Plats för ämnet</span><span class="sxs-lookup"><span data-stu-id="578b2-117">The location of the topic</span></span>

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

### <span data-ttu-id="578b2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="578b2-118">-Name</span></span>
<span data-ttu-id="578b2-119">Namnet på ämnet.</span><span class="sxs-lookup"><span data-stu-id="578b2-119">The name of the topic.</span></span>

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

### <span data-ttu-id="578b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="578b2-121">Resurs gruppen där ämnet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="578b2-121">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="578b2-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="578b2-122">-Tag</span></span>
<span data-ttu-id="578b2-123">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="578b2-123">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="578b2-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="578b2-124">-Confirm</span></span>
<span data-ttu-id="578b2-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="578b2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578b2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578b2-126">-WhatIf</span></span>
<span data-ttu-id="578b2-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="578b2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578b2-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="578b2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578b2-129">CommonParameters</span></span>
<span data-ttu-id="578b2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578b2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578b2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578b2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="578b2-132">INPUTS</span></span>

### <span data-ttu-id="578b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="578b2-133">System.String</span></span>

### <span data-ttu-id="578b2-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="578b2-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="578b2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="578b2-135">OUTPUTS</span></span>

### <span data-ttu-id="578b2-136">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="578b2-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="578b2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="578b2-137">NOTES</span></span>

## <span data-ttu-id="578b2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="578b2-138">RELATED LINKS</span></span>
