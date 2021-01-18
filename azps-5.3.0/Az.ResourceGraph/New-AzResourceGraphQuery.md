---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522308"
---
# <span data-ttu-id="2ecfc-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="2ecfc-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="2ecfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ecfc-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecfc-103">Skapa en ny diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-103">Create a new graph query.</span></span>

## <span data-ttu-id="2ecfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ecfc-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ecfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ecfc-105">DESCRIPTION</span></span>
<span data-ttu-id="2ecfc-106">Skapa en ny diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-106">Create a new graph query.</span></span>

## <span data-ttu-id="2ecfc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ecfc-107">EXAMPLES</span></span>

### <span data-ttu-id="2ecfc-108">Exempel 1: skapa en resurs diagram fråga via Frågeparametern</span><span class="sxs-lookup"><span data-stu-id="2ecfc-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="2ecfc-109">Det här kommandot skapar en resurs diagram fråga via Frågeparametern.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="2ecfc-110">Exempel 2: skapa en resurs diagram fråga via parametern File</span><span class="sxs-lookup"><span data-stu-id="2ecfc-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="2ecfc-111">Det här kommandot skapar en resurs diagram fråga via parametern File.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="2ecfc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ecfc-112">PARAMETERS</span></span>

### <span data-ttu-id="2ecfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecfc-113">-DefaultProfile</span></span>
<span data-ttu-id="2ecfc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2ecfc-115">-Description</span></span>
<span data-ttu-id="2ecfc-116">En beskrivning av en diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-116">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-117">-Fil</span><span class="sxs-lookup"><span data-stu-id="2ecfc-117">-File</span></span>
<span data-ttu-id="2ecfc-118">Innehållet i filen skickas till Frågeparametern.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-118">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="2ecfc-119">-Location</span></span>
<span data-ttu-id="2ecfc-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="2ecfc-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ecfc-121">-Name</span></span>
<span data-ttu-id="2ecfc-122">Namnet på grafen med diagrammet.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-122">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-123">-Fråga</span><span class="sxs-lookup"><span data-stu-id="2ecfc-123">-Query</span></span>
<span data-ttu-id="2ecfc-124">Keyword-fråga som ska vara graf.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-124">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ecfc-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ecfc-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ecfc-127">-SubscriptionId</span></span>
<span data-ttu-id="2ecfc-128">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2ecfc-129">-Tag</span></span>
<span data-ttu-id="2ecfc-130">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="2ecfc-130">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecfc-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ecfc-131">-Confirm</span></span>
<span data-ttu-id="2ecfc-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ecfc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ecfc-133">-WhatIf</span></span>
<span data-ttu-id="2ecfc-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ecfc-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ecfc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecfc-136">CommonParameters</span></span>
<span data-ttu-id="2ecfc-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecfc-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ecfc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecfc-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ecfc-139">INPUTS</span></span>

### <span data-ttu-id="2ecfc-140">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="2ecfc-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="2ecfc-141">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="2ecfc-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="2ecfc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ecfc-142">OUTPUTS</span></span>

### <span data-ttu-id="2ecfc-143">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="2ecfc-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="2ecfc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ecfc-144">NOTES</span></span>

<span data-ttu-id="2ecfc-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2ecfc-145">ALIASES</span></span>

## <span data-ttu-id="2ecfc-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ecfc-146">RELATED LINKS</span></span>

