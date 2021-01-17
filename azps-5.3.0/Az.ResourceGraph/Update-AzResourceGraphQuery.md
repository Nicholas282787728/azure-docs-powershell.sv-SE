---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421003"
---
# <span data-ttu-id="0643d-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="0643d-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="0643d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0643d-102">SYNOPSIS</span></span>
<span data-ttu-id="0643d-103">Uppdaterar en kurva som redan har lagts till.</span><span class="sxs-lookup"><span data-stu-id="0643d-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="0643d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0643d-104">SYNTAX</span></span>

### <span data-ttu-id="0643d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0643d-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0643d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0643d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0643d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0643d-107">DESCRIPTION</span></span>
<span data-ttu-id="0643d-108">Uppdaterar en kurva som redan har lagts till.</span><span class="sxs-lookup"><span data-stu-id="0643d-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="0643d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0643d-109">EXAMPLES</span></span>

### <span data-ttu-id="0643d-110">Exempel 1: uppdatera parameter frågan och taggen med namn</span><span class="sxs-lookup"><span data-stu-id="0643d-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="0643d-111">Det här kommandot uppdaterar parameter frågan och taggen efter namn.</span><span class="sxs-lookup"><span data-stu-id="0643d-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="0643d-112">Exempel 2: uppdatera parameter filen efter objekt</span><span class="sxs-lookup"><span data-stu-id="0643d-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="0643d-113">Det här kommandot uppdaterar parameter frågan och flaggan efter objekt.</span><span class="sxs-lookup"><span data-stu-id="0643d-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="0643d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0643d-114">PARAMETERS</span></span>

### <span data-ttu-id="0643d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0643d-115">-DefaultProfile</span></span>
<span data-ttu-id="0643d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0643d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0643d-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0643d-117">-Description</span></span>
<span data-ttu-id="0643d-118">En beskrivning av en diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="0643d-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="0643d-119">-Fil</span><span class="sxs-lookup"><span data-stu-id="0643d-119">-File</span></span>
<span data-ttu-id="0643d-120">Innehållet i filen skickas till Frågeparametern.</span><span class="sxs-lookup"><span data-stu-id="0643d-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="0643d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0643d-121">-InputObject</span></span>
<span data-ttu-id="0643d-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0643d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0643d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0643d-123">-Name</span></span>
<span data-ttu-id="0643d-124">Namnet på grafen med diagrammet.</span><span class="sxs-lookup"><span data-stu-id="0643d-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0643d-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="0643d-125">-Query</span></span>
<span data-ttu-id="0643d-126">Keyword-fråga som ska vara graf.</span><span class="sxs-lookup"><span data-stu-id="0643d-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="0643d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0643d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0643d-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0643d-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0643d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0643d-129">-SubscriptionId</span></span>
<span data-ttu-id="0643d-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0643d-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0643d-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0643d-131">-Tag</span></span>
<span data-ttu-id="0643d-132">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="0643d-132">Resource tags</span></span>

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

### <span data-ttu-id="0643d-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0643d-133">-Confirm</span></span>
<span data-ttu-id="0643d-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0643d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0643d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0643d-135">-WhatIf</span></span>
<span data-ttu-id="0643d-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0643d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0643d-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0643d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0643d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0643d-138">CommonParameters</span></span>
<span data-ttu-id="0643d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0643d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0643d-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0643d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0643d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0643d-141">INPUTS</span></span>

### <span data-ttu-id="0643d-142">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="0643d-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="0643d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0643d-143">OUTPUTS</span></span>

### <span data-ttu-id="0643d-144">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="0643d-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="0643d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0643d-145">NOTES</span></span>

<span data-ttu-id="0643d-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0643d-146">ALIASES</span></span>

<span data-ttu-id="0643d-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0643d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0643d-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0643d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0643d-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0643d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0643d-150">INPUTOBJECT <IResourceGraphIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0643d-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0643d-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0643d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0643d-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0643d-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0643d-153">`[ResourceName <String>]`: Namnet på grafen med diagrammet.</span><span class="sxs-lookup"><span data-stu-id="0643d-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="0643d-154">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0643d-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="0643d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0643d-155">RELATED LINKS</span></span>

