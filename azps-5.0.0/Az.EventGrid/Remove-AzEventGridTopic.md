---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270686"
---
# <span data-ttu-id="f7aa6-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="f7aa6-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="f7aa6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aa6-103">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="f7aa6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7aa6-104">SYNTAX</span></span>

### <span data-ttu-id="f7aa6-105">TopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f7aa6-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7aa6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7aa6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7aa6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7aa6-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7aa6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7aa6-108">DESCRIPTION</span></span>
<span data-ttu-id="f7aa6-109">Tar bort ett avsnitt i ett Azure-evenemang.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="f7aa6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7aa6-110">EXAMPLES</span></span>

### <span data-ttu-id="f7aa6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7aa6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="f7aa6-112">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="f7aa6-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f7aa6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f7aa6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="f7aa6-114">Tar bort avsnittet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="f7aa6-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f7aa6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7aa6-115">PARAMETERS</span></span>

### <span data-ttu-id="f7aa6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7aa6-116">-DefaultProfile</span></span>
<span data-ttu-id="f7aa6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f7aa6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7aa6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7aa6-118">-InputObject</span></span>
<span data-ttu-id="f7aa6-119">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f7aa6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7aa6-120">-Name</span></span>
<span data-ttu-id="f7aa6-121">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f7aa6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7aa6-122">-PassThru</span></span>
<span data-ttu-id="f7aa6-123">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="f7aa6-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7aa6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7aa6-125">-ResourceGroupName</span></span>
<span data-ttu-id="f7aa6-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7aa6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7aa6-127">-ResourceId</span></span>
<span data-ttu-id="f7aa6-128">EventGrid-ämne ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="f7aa6-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7aa6-129">-Confirm</span></span>
<span data-ttu-id="f7aa6-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7aa6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7aa6-131">-WhatIf</span></span>
<span data-ttu-id="f7aa6-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7aa6-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7aa6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aa6-134">CommonParameters</span></span>
<span data-ttu-id="f7aa6-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7aa6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aa6-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7aa6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aa6-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7aa6-137">INPUTS</span></span>

### <span data-ttu-id="f7aa6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f7aa6-138">System.String</span></span>

### <span data-ttu-id="f7aa6-139">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f7aa6-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f7aa6-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7aa6-140">OUTPUTS</span></span>

### <span data-ttu-id="f7aa6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7aa6-141">System.Boolean</span></span>

## <span data-ttu-id="f7aa6-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7aa6-142">NOTES</span></span>

## <span data-ttu-id="f7aa6-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7aa6-143">RELATED LINKS</span></span>
