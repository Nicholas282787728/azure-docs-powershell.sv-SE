---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259163"
---
# <span data-ttu-id="8ea9e-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="8ea9e-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="8ea9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea9e-103">Skapar eller uppdaterar en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="8ea9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ea9e-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ea9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ea9e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ea9e-106">Skapar eller uppdaterar en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="8ea9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ea9e-107">EXAMPLES</span></span>

### <span data-ttu-id="8ea9e-108">Exempel 1: skapa en ny flytt samling.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="8ea9e-109">Skapa en ny drag samling i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="8ea9e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ea9e-110">PARAMETERS</span></span>

### <span data-ttu-id="8ea9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea9e-111">-DefaultProfile</span></span>
<span data-ttu-id="8ea9e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea9e-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="8ea9e-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="8ea9e-114">Hämtar eller anger huvud-ID.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="8ea9e-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="8ea9e-115">-IdentityTenantId</span></span>
<span data-ttu-id="8ea9e-116">Hämtar eller anger klient-ID.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="8ea9e-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8ea9e-117">-IdentityType</span></span>
<span data-ttu-id="8ea9e-118">Den typ av identitet som används för regionens flytt tjänst.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="8ea9e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8ea9e-119">-Location</span></span>
<span data-ttu-id="8ea9e-120">Geo-platsen där resursen bor.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="8ea9e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ea9e-121">-Name</span></span>
<span data-ttu-id="8ea9e-122">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8ea9e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea9e-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ea9e-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8ea9e-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="8ea9e-125">-SourceRegion</span></span>
<span data-ttu-id="8ea9e-126">Hämtar eller anger käll området.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="8ea9e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ea9e-127">-SubscriptionId</span></span>
<span data-ttu-id="8ea9e-128">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="8ea9e-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8ea9e-129">-Tag</span></span>
<span data-ttu-id="8ea9e-130">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-130">Resource tags.</span></span>

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

### <span data-ttu-id="8ea9e-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="8ea9e-131">-TargetRegion</span></span>
<span data-ttu-id="8ea9e-132">Hämtar eller anger mål området.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="8ea9e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ea9e-133">-Confirm</span></span>
<span data-ttu-id="8ea9e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ea9e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea9e-135">-WhatIf</span></span>
<span data-ttu-id="8ea9e-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ea9e-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ea9e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea9e-138">CommonParameters</span></span>
<span data-ttu-id="8ea9e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea9e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea9e-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ea9e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea9e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ea9e-141">INPUTS</span></span>

## <span data-ttu-id="8ea9e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ea9e-142">OUTPUTS</span></span>

### <span data-ttu-id="8ea9e-143">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="8ea9e-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="8ea9e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ea9e-144">NOTES</span></span>

<span data-ttu-id="8ea9e-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8ea9e-145">ALIASES</span></span>

## <span data-ttu-id="8ea9e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ea9e-146">RELATED LINKS</span></span>

