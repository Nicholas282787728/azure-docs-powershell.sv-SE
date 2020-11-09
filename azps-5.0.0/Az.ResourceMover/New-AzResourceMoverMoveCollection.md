---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324318"
---
# <span data-ttu-id="147aa-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="147aa-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="147aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="147aa-102">SYNOPSIS</span></span>
<span data-ttu-id="147aa-103">Skapar eller uppdaterar en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="147aa-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="147aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="147aa-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="147aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="147aa-105">DESCRIPTION</span></span>
<span data-ttu-id="147aa-106">Skapar eller uppdaterar en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="147aa-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="147aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="147aa-107">EXAMPLES</span></span>

### <span data-ttu-id="147aa-108">Exempel 1: skapa en ny flytt samling.</span><span class="sxs-lookup"><span data-stu-id="147aa-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="147aa-109">Skapa en ny drag samling i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="147aa-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="147aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="147aa-110">PARAMETERS</span></span>

### <span data-ttu-id="147aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147aa-111">-DefaultProfile</span></span>
<span data-ttu-id="147aa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="147aa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="147aa-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="147aa-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="147aa-114">Hämtar eller anger huvud-ID.</span><span class="sxs-lookup"><span data-stu-id="147aa-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="147aa-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="147aa-115">-IdentityTenantId</span></span>
<span data-ttu-id="147aa-116">Hämtar eller anger klient-ID.</span><span class="sxs-lookup"><span data-stu-id="147aa-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="147aa-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="147aa-117">-IdentityType</span></span>
<span data-ttu-id="147aa-118">Den typ av identitet som används för regionens flytt tjänst.</span><span class="sxs-lookup"><span data-stu-id="147aa-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147aa-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="147aa-119">-Location</span></span>
<span data-ttu-id="147aa-120">Geo-platsen där resursen bor.</span><span class="sxs-lookup"><span data-stu-id="147aa-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="147aa-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="147aa-121">-Name</span></span>
<span data-ttu-id="147aa-122">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="147aa-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="147aa-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="147aa-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="147aa-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="147aa-125">-SourceRegion</span></span>
<span data-ttu-id="147aa-126">Hämtar eller anger käll området.</span><span class="sxs-lookup"><span data-stu-id="147aa-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="147aa-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="147aa-127">-SubscriptionId</span></span>
<span data-ttu-id="147aa-128">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="147aa-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="147aa-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="147aa-129">-Tag</span></span>
<span data-ttu-id="147aa-130">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="147aa-130">Resource tags.</span></span>

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

### <span data-ttu-id="147aa-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="147aa-131">-TargetRegion</span></span>
<span data-ttu-id="147aa-132">Hämtar eller anger mål området.</span><span class="sxs-lookup"><span data-stu-id="147aa-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="147aa-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="147aa-133">-Confirm</span></span>
<span data-ttu-id="147aa-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="147aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="147aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147aa-135">-WhatIf</span></span>
<span data-ttu-id="147aa-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="147aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147aa-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="147aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="147aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147aa-138">CommonParameters</span></span>
<span data-ttu-id="147aa-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147aa-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="147aa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147aa-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="147aa-141">INPUTS</span></span>

## <span data-ttu-id="147aa-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="147aa-142">OUTPUTS</span></span>

### <span data-ttu-id="147aa-143">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="147aa-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="147aa-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="147aa-144">NOTES</span></span>

<span data-ttu-id="147aa-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="147aa-145">ALIASES</span></span>

## <span data-ttu-id="147aa-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="147aa-146">RELATED LINKS</span></span>

