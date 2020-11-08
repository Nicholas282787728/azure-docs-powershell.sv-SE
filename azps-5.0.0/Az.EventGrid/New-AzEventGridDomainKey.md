---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271938"
---
# <span data-ttu-id="a2b97-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a2b97-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="a2b97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2b97-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b97-103">Återskapar den delade åtkomst-nyckeln för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a2b97-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="a2b97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2b97-104">SYNTAX</span></span>

### <span data-ttu-id="a2b97-105">DomainNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a2b97-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b97-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2b97-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b97-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2b97-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b97-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2b97-108">DESCRIPTION</span></span>
<span data-ttu-id="a2b97-109">Återskapar den delade åtkomst-nyckeln för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="a2b97-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="a2b97-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2b97-110">EXAMPLES</span></span>

### <span data-ttu-id="a2b97-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2b97-111">Example 1</span></span>

<span data-ttu-id="a2b97-112">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of Event rutmönster Domain \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a2b97-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="a2b97-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a2b97-113">Example 2</span></span>

<span data-ttu-id="a2b97-114">Återskapa nyckeln som motsvarar nyckeln \' KEY1 ' \ of Event rutmönster Domain \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a2b97-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="a2b97-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a2b97-115">Example 3</span></span>

<span data-ttu-id="a2b97-116">Återskapa nyckeln som motsvarar nyckeln \' key2 ' \ of Event rutmönster Domain \` domain1 \` i resurs gruppen \` MyResourceGroupName \` med dess fullständiga resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a2b97-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="a2b97-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2b97-117">PARAMETERS</span></span>

### <span data-ttu-id="a2b97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b97-118">-DefaultProfile</span></span>
<span data-ttu-id="a2b97-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b97-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2b97-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a2b97-120">-DomainInputObject</span></span>
<span data-ttu-id="a2b97-121">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a2b97-121">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b97-122">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="a2b97-122">-DomainName</span></span>
<span data-ttu-id="a2b97-123">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="a2b97-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b97-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="a2b97-124">-DomainResourceId</span></span>
<span data-ttu-id="a2b97-125">Resurs-ID som representerar händelse rutnäts domänen.</span><span class="sxs-lookup"><span data-stu-id="a2b97-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="a2b97-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2b97-126">-Name</span></span>
<span data-ttu-id="a2b97-127">Namnet på den nyckeln som måste återskapas</span><span class="sxs-lookup"><span data-stu-id="a2b97-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b97-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2b97-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a2b97-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b97-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2b97-130">-Confirm</span></span>
<span data-ttu-id="a2b97-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2b97-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b97-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b97-132">-WhatIf</span></span>
<span data-ttu-id="a2b97-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2b97-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b97-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2b97-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b97-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b97-135">CommonParameters</span></span>
<span data-ttu-id="a2b97-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b97-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b97-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2b97-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b97-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2b97-138">INPUTS</span></span>

### <span data-ttu-id="a2b97-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b97-139">System.String</span></span>

### <span data-ttu-id="a2b97-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a2b97-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="a2b97-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2b97-141">OUTPUTS</span></span>

### <span data-ttu-id="a2b97-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a2b97-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="a2b97-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2b97-143">NOTES</span></span>

## <span data-ttu-id="a2b97-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2b97-144">RELATED LINKS</span></span>
