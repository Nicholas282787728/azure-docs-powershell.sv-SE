---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420363"
---
# <span data-ttu-id="bf327-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bf327-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="bf327-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf327-102">SYNOPSIS</span></span>
<span data-ttu-id="bf327-103">Tar bort ett avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="bf327-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="bf327-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf327-104">SYNTAX</span></span>

### <span data-ttu-id="bf327-105">DomainTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bf327-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf327-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf327-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf327-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf327-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf327-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf327-108">DESCRIPTION</span></span>
<span data-ttu-id="bf327-109">Tar bort ett avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="bf327-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="bf327-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf327-110">EXAMPLES</span></span>

### <span data-ttu-id="bf327-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf327-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="bf327-112">Tar bort avsnittet händelse rutnät Domain \` Ämne1 \` under domän \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="bf327-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bf327-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bf327-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="bf327-114">Tar bort avsnittet händelse rutnät Domain \` Ämne1 \` under domän \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="bf327-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="bf327-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf327-115">PARAMETERS</span></span>

### <span data-ttu-id="bf327-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf327-116">-DefaultProfile</span></span>
<span data-ttu-id="bf327-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf327-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf327-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="bf327-118">-DomainName</span></span>
<span data-ttu-id="bf327-119">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="bf327-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf327-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf327-120">-InputObject</span></span>
<span data-ttu-id="bf327-121">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="bf327-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf327-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf327-122">-Name</span></span>
<span data-ttu-id="bf327-123">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="bf327-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf327-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf327-124">-PassThru</span></span>
<span data-ttu-id="bf327-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bf327-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bf327-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf327-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf327-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf327-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf327-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf327-128">-ResourceId</span></span>
<span data-ttu-id="bf327-129">Resurs-ID som representerar avsnittet händelse rutnät Domain.</span><span class="sxs-lookup"><span data-stu-id="bf327-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf327-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf327-130">-Confirm</span></span>
<span data-ttu-id="bf327-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf327-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf327-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf327-132">-WhatIf</span></span>
<span data-ttu-id="bf327-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf327-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf327-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf327-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf327-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf327-135">CommonParameters</span></span>
<span data-ttu-id="bf327-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf327-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf327-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf327-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf327-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf327-138">INPUTS</span></span>

### <span data-ttu-id="bf327-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bf327-139">System.String</span></span>

### <span data-ttu-id="bf327-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bf327-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="bf327-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf327-141">OUTPUTS</span></span>

### <span data-ttu-id="bf327-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf327-142">System.Boolean</span></span>

## <span data-ttu-id="bf327-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf327-143">NOTES</span></span>

## <span data-ttu-id="bf327-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf327-144">RELATED LINKS</span></span>
