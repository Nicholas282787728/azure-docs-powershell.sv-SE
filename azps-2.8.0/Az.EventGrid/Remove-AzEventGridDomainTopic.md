---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 04bed413aca213a558ab1e0afaf5e6badcf238c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744240"
---
# <span data-ttu-id="6be94-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6be94-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="6be94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6be94-102">SYNOPSIS</span></span>
<span data-ttu-id="6be94-103">Tar bort ett avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="6be94-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="6be94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6be94-104">SYNTAX</span></span>

### <span data-ttu-id="6be94-105">DomainTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6be94-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6be94-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="6be94-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6be94-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6be94-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6be94-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6be94-108">DESCRIPTION</span></span>
<span data-ttu-id="6be94-109">Tar bort ett avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="6be94-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="6be94-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6be94-110">EXAMPLES</span></span>

### <span data-ttu-id="6be94-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6be94-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="6be94-112">Tar bort avsnittet händelse rutnät Domain \` Ämne1 \` under domän \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6be94-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6be94-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6be94-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="6be94-114">Tar bort avsnittet händelse rutnät Domain \` Ämne1 \` under domän \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6be94-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6be94-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6be94-115">PARAMETERS</span></span>

### <span data-ttu-id="6be94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be94-116">-DefaultProfile</span></span>
<span data-ttu-id="6be94-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6be94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be94-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="6be94-118">-DomainName</span></span>
<span data-ttu-id="6be94-119">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="6be94-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="6be94-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6be94-120">-InputObject</span></span>
<span data-ttu-id="6be94-121">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="6be94-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="6be94-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6be94-122">-Name</span></span>
<span data-ttu-id="6be94-123">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="6be94-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="6be94-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6be94-124">-PassThru</span></span>
<span data-ttu-id="6be94-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6be94-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6be94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be94-126">-ResourceGroupName</span></span>
<span data-ttu-id="6be94-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6be94-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6be94-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6be94-128">-ResourceId</span></span>
<span data-ttu-id="6be94-129">Resurs-ID som representerar avsnittet händelse rutnät Domain.</span><span class="sxs-lookup"><span data-stu-id="6be94-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="6be94-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6be94-130">-Confirm</span></span>
<span data-ttu-id="6be94-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6be94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be94-132">-WhatIf</span></span>
<span data-ttu-id="6be94-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6be94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be94-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6be94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be94-135">CommonParameters</span></span>
<span data-ttu-id="6be94-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be94-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be94-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be94-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6be94-138">INPUTS</span></span>

### <span data-ttu-id="6be94-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6be94-139">System.String</span></span>

### <span data-ttu-id="6be94-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6be94-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="6be94-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6be94-141">OUTPUTS</span></span>

### <span data-ttu-id="6be94-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6be94-142">System.Boolean</span></span>

## <span data-ttu-id="6be94-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6be94-143">NOTES</span></span>

## <span data-ttu-id="6be94-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6be94-144">RELATED LINKS</span></span>
