---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261318"
---
# <span data-ttu-id="7f1de-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7f1de-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="7f1de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f1de-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1de-103">Skapar en ny Azure Event-Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7f1de-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="7f1de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f1de-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f1de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f1de-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1de-106">Skapar en ny Azure Event-Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7f1de-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="7f1de-107">När domänen har skapats kan ett program publicera händelser till Avsnittets slut punkt.</span><span class="sxs-lookup"><span data-stu-id="7f1de-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="7f1de-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f1de-108">EXAMPLES</span></span>

### <span data-ttu-id="7f1de-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f1de-109">Example 1</span></span>

<span data-ttu-id="7f1de-110">Skapar en \` domain1 för händelse rutnät \` på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7f1de-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="7f1de-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7f1de-111">Example 2</span></span>

<span data-ttu-id="7f1de-112">Skapar en \` domain1 för händelse rutnät \` på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="7f1de-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="7f1de-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f1de-113">PARAMETERS</span></span>

### <span data-ttu-id="7f1de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1de-114">-DefaultProfile</span></span>
<span data-ttu-id="7f1de-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f1de-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="7f1de-116">-InboundIpRule</span></span>
<span data-ttu-id="7f1de-117">Hash-adress som representerar listan med regler för inkommande IP.</span><span class="sxs-lookup"><span data-stu-id="7f1de-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="7f1de-118">Varje regel anger IP-adressen i CIDR-notation, till exempel 10.0.0.0/8 tillsammans med motsvarande åtgärd som ska utföras baserat på matchningen eller ingen matchning av IpMask.</span><span class="sxs-lookup"><span data-stu-id="7f1de-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="7f1de-119">Möjliga åtgärds värden inkluderar endast Tillåt</span><span class="sxs-lookup"><span data-stu-id="7f1de-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="7f1de-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="7f1de-121">Hash-enhet som representerar fälten för inmatning med standardvärdet i blankstegsavgränsad blank steg = värde format.</span><span class="sxs-lookup"><span data-stu-id="7f1de-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="7f1de-122">Tillåtna namn är: subject, EventType och dataversion.</span><span class="sxs-lookup"><span data-stu-id="7f1de-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="7f1de-123">Detta används när InputSchemaHelp endast är customeventschema.</span><span class="sxs-lookup"><span data-stu-id="7f1de-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="7f1de-124">-InputMappingField</span></span>
<span data-ttu-id="7f1de-125">Hash-fil som representerar fälten för inmatning i blankstegsavgränsad Key = värde format.</span><span class="sxs-lookup"><span data-stu-id="7f1de-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="7f1de-126">Tillåtna namn är: ID, ämne, eventtime, ämne, EventType och dataversion.</span><span class="sxs-lookup"><span data-stu-id="7f1de-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="7f1de-127">Detta används när InputSchemaHelp endast är customeventschema.</span><span class="sxs-lookup"><span data-stu-id="7f1de-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="7f1de-128">-InputSchema</span></span>
<span data-ttu-id="7f1de-129">Schemat för inmatnings händelser för ämnet.</span><span class="sxs-lookup"><span data-stu-id="7f1de-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="7f1de-130">Tillåtna värden är: eventgridschema, customeventschema eller cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="7f1de-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="7f1de-131">Standardvärdet är eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="7f1de-131">Default value is eventgridschema.</span></span> <span data-ttu-id="7f1de-132">Observera att om customeventschema är angivet måste även InputMappingField-och/eller InputMappingDefaultValue-parametrar anges.</span><span class="sxs-lookup"><span data-stu-id="7f1de-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="7f1de-133">-Location</span></span>
<span data-ttu-id="7f1de-134">Domänens plats.</span><span class="sxs-lookup"><span data-stu-id="7f1de-134">The location of the domain.</span></span>

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

### <span data-ttu-id="7f1de-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f1de-135">-Name</span></span>
<span data-ttu-id="7f1de-136">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="7f1de-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7f1de-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="7f1de-138">Det här avgör om trafik tillåts via offentliga nätverk.</span><span class="sxs-lookup"><span data-stu-id="7f1de-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="7f1de-139">Den är aktive rad som standard.</span><span class="sxs-lookup"><span data-stu-id="7f1de-139">By default it is enabled.</span></span> <span data-ttu-id="7f1de-140">Du kan ytterligare begränsa till specifika IP-adresser genom att konfigurera InboundIpRule-parametrar.</span><span class="sxs-lookup"><span data-stu-id="7f1de-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="7f1de-141">Tillåtna värden är inaktiverade och aktiverade.</span><span class="sxs-lookup"><span data-stu-id="7f1de-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1de-142">-ResourceGroupName</span></span>
<span data-ttu-id="7f1de-143">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7f1de-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f1de-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7f1de-144">-Tag</span></span>
<span data-ttu-id="7f1de-145">Hash-kod som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7f1de-145">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1de-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f1de-146">-Confirm</span></span>
<span data-ttu-id="7f1de-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f1de-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f1de-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1de-148">-WhatIf</span></span>
<span data-ttu-id="7f1de-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f1de-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f1de-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f1de-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f1de-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1de-151">CommonParameters</span></span>
<span data-ttu-id="7f1de-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1de-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1de-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f1de-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1de-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f1de-154">INPUTS</span></span>

### <span data-ttu-id="7f1de-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7f1de-155">System.String</span></span>

### <span data-ttu-id="7f1de-156">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7f1de-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f1de-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f1de-157">OUTPUTS</span></span>

### <span data-ttu-id="7f1de-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="7f1de-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="7f1de-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f1de-159">NOTES</span></span>

## <span data-ttu-id="7f1de-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f1de-160">RELATED LINKS</span></span>
