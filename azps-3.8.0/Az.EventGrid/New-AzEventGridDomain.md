---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926650"
---
# <span data-ttu-id="b293f-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b293f-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="b293f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b293f-102">SYNOPSIS</span></span>
<span data-ttu-id="b293f-103">Skapar en ny Azure Event-Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b293f-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="b293f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b293f-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b293f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b293f-105">DESCRIPTION</span></span>
<span data-ttu-id="b293f-106">Skapar en ny Azure Event-Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="b293f-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="b293f-107">När domänen har skapats kan ett program publicera händelser till Avsnittets slut punkt.</span><span class="sxs-lookup"><span data-stu-id="b293f-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="b293f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b293f-108">EXAMPLES</span></span>

### <span data-ttu-id="b293f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b293f-109">Example 1</span></span>

<span data-ttu-id="b293f-110">Skapar en \` domain1 för händelse rutnät \` på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b293f-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="b293f-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b293f-111">Example 2</span></span>

<span data-ttu-id="b293f-112">Skapar en \` domain1 för händelse rutnät \` på den geografiska plats \` westus2 \` i resurs grupps \` MyResourceGroupName \` med de angivna taggarna "avdelning" och "miljö".</span><span class="sxs-lookup"><span data-stu-id="b293f-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="b293f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b293f-113">PARAMETERS</span></span>

### <span data-ttu-id="b293f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b293f-114">-DefaultProfile</span></span>
<span data-ttu-id="b293f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b293f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b293f-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b293f-116">-Location</span></span>
<span data-ttu-id="b293f-117">Domänens plats.</span><span class="sxs-lookup"><span data-stu-id="b293f-117">The location of the domain.</span></span>

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

### <span data-ttu-id="b293f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b293f-118">-Name</span></span>
<span data-ttu-id="b293f-119">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="b293f-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b293f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b293f-120">-ResourceGroupName</span></span>
<span data-ttu-id="b293f-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b293f-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="b293f-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b293f-122">-Tag</span></span>
<span data-ttu-id="b293f-123">Hash-kod som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b293f-123">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="b293f-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b293f-124">-Confirm</span></span>
<span data-ttu-id="b293f-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b293f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b293f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b293f-126">-WhatIf</span></span>
<span data-ttu-id="b293f-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b293f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b293f-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b293f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b293f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b293f-129">CommonParameters</span></span>
<span data-ttu-id="b293f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b293f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b293f-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b293f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b293f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b293f-132">INPUTS</span></span>

### <span data-ttu-id="b293f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b293f-133">System.String</span></span>

### <span data-ttu-id="b293f-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b293f-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b293f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b293f-135">OUTPUTS</span></span>

### <span data-ttu-id="b293f-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="b293f-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="b293f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b293f-137">NOTES</span></span>

## <span data-ttu-id="b293f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b293f-138">RELATED LINKS</span></span>
