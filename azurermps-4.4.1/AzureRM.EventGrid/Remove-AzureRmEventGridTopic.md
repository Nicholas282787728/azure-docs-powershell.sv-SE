---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758090"
---
# <span data-ttu-id="06a22-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="06a22-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="06a22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06a22-102">SYNOPSIS</span></span>
<span data-ttu-id="06a22-103">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="06a22-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06a22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06a22-104">SYNTAX</span></span>

### <span data-ttu-id="06a22-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="06a22-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a22-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="06a22-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a22-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06a22-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a22-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06a22-108">DESCRIPTION</span></span>
<span data-ttu-id="06a22-109">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="06a22-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="06a22-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06a22-110">EXAMPLES</span></span>

### <span data-ttu-id="06a22-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06a22-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="06a22-112">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="06a22-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="06a22-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="06a22-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="06a22-114">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="06a22-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="06a22-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06a22-115">PARAMETERS</span></span>

### <span data-ttu-id="06a22-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a22-116">-InputObject</span></span>
<span data-ttu-id="06a22-117">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="06a22-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="06a22-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="06a22-118">-Name</span></span>
<span data-ttu-id="06a22-119">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="06a22-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="06a22-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06a22-120">-PassThru</span></span>
<span data-ttu-id="06a22-121">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="06a22-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="06a22-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="06a22-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a22-123">-ResourceGroupName</span></span>
<span data-ttu-id="06a22-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="06a22-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="06a22-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06a22-125">-ResourceId</span></span>
<span data-ttu-id="06a22-126">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="06a22-126">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a22-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06a22-127">-Confirm</span></span>
<span data-ttu-id="06a22-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06a22-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a22-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a22-129">-WhatIf</span></span>
<span data-ttu-id="06a22-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06a22-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a22-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06a22-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a22-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a22-132">-DefaultProfile</span></span>
<span data-ttu-id="06a22-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06a22-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a22-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a22-134">CommonParameters</span></span>
<span data-ttu-id="06a22-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a22-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a22-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a22-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a22-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06a22-137">INPUTS</span></span>

### <span data-ttu-id="06a22-138">System. String</span><span class="sxs-lookup"><span data-stu-id="06a22-138">System.String</span></span>
<span data-ttu-id="06a22-139">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="06a22-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="06a22-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06a22-140">OUTPUTS</span></span>

### <span data-ttu-id="06a22-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="06a22-141">System.Object</span></span>

## <span data-ttu-id="06a22-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06a22-142">NOTES</span></span>

## <span data-ttu-id="06a22-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06a22-143">RELATED LINKS</span></span>

