---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: d853d5d4659e41c9696ab87c3f9ab8b58c240044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578051"
---
# <span data-ttu-id="ab4a7-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ab4a7-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="ab4a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4a7-103">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab4a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab4a7-104">SYNTAX</span></span>

### <span data-ttu-id="ab4a7-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ab4a7-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab4a7-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab4a7-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab4a7-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab4a7-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab4a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab4a7-108">DESCRIPTION</span></span>
<span data-ttu-id="ab4a7-109">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ab4a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab4a7-110">EXAMPLES</span></span>

### <span data-ttu-id="ab4a7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab4a7-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="ab4a7-112">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="ab4a7-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ab4a7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ab4a7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="ab4a7-114">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="ab4a7-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ab4a7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab4a7-115">PARAMETERS</span></span>

### <span data-ttu-id="ab4a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4a7-116">-DefaultProfile</span></span>
<span data-ttu-id="ab4a7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab4a7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab4a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab4a7-118">-InputObject</span></span>
<span data-ttu-id="ab4a7-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ab4a7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab4a7-120">-Name</span></span>
<span data-ttu-id="ab4a7-121">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ab4a7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab4a7-122">-PassThru</span></span>
<span data-ttu-id="ab4a7-123">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ab4a7-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab4a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab4a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab4a7-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ab4a7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab4a7-127">-ResourceId</span></span>
<span data-ttu-id="ab4a7-128">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="ab4a7-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab4a7-129">-Confirm</span></span>
<span data-ttu-id="ab4a7-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab4a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4a7-131">-WhatIf</span></span>
<span data-ttu-id="ab4a7-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab4a7-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab4a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4a7-134">CommonParameters</span></span>
<span data-ttu-id="ab4a7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4a7-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4a7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4a7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab4a7-137">INPUTS</span></span>

### <span data-ttu-id="ab4a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ab4a7-138">System.String</span></span>

### <span data-ttu-id="ab4a7-139">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ab4a7-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="ab4a7-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab4a7-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ab4a7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab4a7-141">OUTPUTS</span></span>

### <span data-ttu-id="ab4a7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab4a7-142">System.Boolean</span></span>

## <span data-ttu-id="ab4a7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab4a7-143">NOTES</span></span>

## <span data-ttu-id="ab4a7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab4a7-144">RELATED LINKS</span></span>