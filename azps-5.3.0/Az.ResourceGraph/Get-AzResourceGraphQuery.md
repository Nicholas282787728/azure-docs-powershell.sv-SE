---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523054"
---
# <span data-ttu-id="99841-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="99841-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="99841-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99841-102">SYNOPSIS</span></span>
<span data-ttu-id="99841-103">Få en enda kurva-fråga per resourceName.</span><span class="sxs-lookup"><span data-stu-id="99841-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="99841-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99841-104">SYNTAX</span></span>

### <span data-ttu-id="99841-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="99841-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="99841-106">Lära</span><span class="sxs-lookup"><span data-stu-id="99841-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99841-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99841-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="99841-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99841-108">DESCRIPTION</span></span>
<span data-ttu-id="99841-109">Få en enda kurva-fråga per resourceName.</span><span class="sxs-lookup"><span data-stu-id="99841-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="99841-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99841-110">EXAMPLES</span></span>

### <span data-ttu-id="99841-111">Exempel 1: Hämta alla resurs diagram frågor under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="99841-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="99841-112">Det här kommandot får alla resurs diagram frågor under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="99841-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="99841-113">Exempel 2: Hämta en resurs diagram fråga efter namn</span><span class="sxs-lookup"><span data-stu-id="99841-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="99841-114">Det här kommandot får en resurs diagram fråga efter namn.</span><span class="sxs-lookup"><span data-stu-id="99841-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="99841-115">Exempel 2: Hämta en resurs diagram fråga genom objecy</span><span class="sxs-lookup"><span data-stu-id="99841-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="99841-116">Det här kommandot får en resurs diagram fråga efter objekt.</span><span class="sxs-lookup"><span data-stu-id="99841-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="99841-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99841-117">PARAMETERS</span></span>

### <span data-ttu-id="99841-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99841-118">-DefaultProfile</span></span>
<span data-ttu-id="99841-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99841-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99841-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99841-120">-InputObject</span></span>
<span data-ttu-id="99841-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="99841-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99841-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="99841-122">-Name</span></span>
<span data-ttu-id="99841-123">Namnet på grafen med diagrammet.</span><span class="sxs-lookup"><span data-stu-id="99841-123">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99841-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99841-124">-ResourceGroupName</span></span>
<span data-ttu-id="99841-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="99841-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99841-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99841-126">-SubscriptionId</span></span>
<span data-ttu-id="99841-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="99841-127">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99841-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99841-128">CommonParameters</span></span>
<span data-ttu-id="99841-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99841-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99841-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99841-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99841-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99841-131">INPUTS</span></span>

### <span data-ttu-id="99841-132">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="99841-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="99841-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99841-133">OUTPUTS</span></span>

### <span data-ttu-id="99841-134">Microsoft. Azure. PowerShell. cmdletar. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="99841-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="99841-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99841-135">NOTES</span></span>

<span data-ttu-id="99841-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="99841-136">ALIASES</span></span>

<span data-ttu-id="99841-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="99841-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99841-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="99841-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99841-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99841-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99841-140">INPUTOBJECT <IResourceGraphIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="99841-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99841-141">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="99841-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99841-142">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="99841-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="99841-143">`[ResourceName <String>]`: Namnet på grafen med diagrammet.</span><span class="sxs-lookup"><span data-stu-id="99841-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="99841-144">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="99841-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="99841-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99841-145">RELATED LINKS</span></span>

