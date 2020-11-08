---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092916"
---
# <span data-ttu-id="db925-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="db925-101">New-AzsPlan</span></span>

## <span data-ttu-id="db925-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db925-102">SYNOPSIS</span></span>
<span data-ttu-id="db925-103">Skapa eller uppdatera abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-103">Create or update the plan.</span></span>

## <span data-ttu-id="db925-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db925-104">SYNTAX</span></span>

### <span data-ttu-id="db925-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="db925-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db925-106">Göra</span><span class="sxs-lookup"><span data-stu-id="db925-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db925-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db925-107">DESCRIPTION</span></span>
<span data-ttu-id="db925-108">Skapa eller uppdatera abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-108">Create or update the plan.</span></span>

## <span data-ttu-id="db925-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db925-109">EXAMPLES</span></span>

### <span data-ttu-id="db925-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db925-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="db925-111">Skapar en ny plan</span><span class="sxs-lookup"><span data-stu-id="db925-111">Creates a new plan</span></span>

## <span data-ttu-id="db925-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db925-112">PARAMETERS</span></span>

### <span data-ttu-id="db925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db925-113">-DefaultProfile</span></span>
<span data-ttu-id="db925-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db925-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db925-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="db925-115">-Description</span></span>
<span data-ttu-id="db925-116">Beskrivning av planen.</span><span class="sxs-lookup"><span data-stu-id="db925-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db925-117">-DisplayName</span></span>
<span data-ttu-id="db925-118">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="db925-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="db925-119">-ExternalReferenceId</span></span>
<span data-ttu-id="db925-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="db925-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="db925-121">-Location</span></span>
<span data-ttu-id="db925-122">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="db925-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="db925-123">-Name</span></span>
<span data-ttu-id="db925-124">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-124">Name of the plan.</span></span>

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

### <span data-ttu-id="db925-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="db925-125">-PlanDefinition</span></span>
<span data-ttu-id="db925-126">En plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="db925-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="db925-127">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="db925-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="db925-128">För att konstruera kan du läsa avsnittet anteckningar för PLANDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="db925-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="db925-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="db925-129">-PropertiesName</span></span>
<span data-ttu-id="db925-130">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="db925-131">-QuotaIds</span></span>
<span data-ttu-id="db925-132">Kvot-ID: n under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db925-133">-ResourceGroupName</span></span>
<span data-ttu-id="db925-134">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="db925-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="db925-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="db925-135">-SkuIds</span></span>
<span data-ttu-id="db925-136">SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="db925-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="db925-137">-SubscriptionCount</span></span>
<span data-ttu-id="db925-138">Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="db925-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db925-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db925-139">-SubscriptionId</span></span>
<span data-ttu-id="db925-140">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="db925-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db925-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db925-141">-Confirm</span></span>
<span data-ttu-id="db925-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db925-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db925-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db925-143">-WhatIf</span></span>
<span data-ttu-id="db925-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db925-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db925-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db925-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db925-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db925-146">CommonParameters</span></span>
<span data-ttu-id="db925-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db925-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db925-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db925-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db925-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db925-149">INPUTS</span></span>

### <span data-ttu-id="db925-150">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="db925-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="db925-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db925-151">OUTPUTS</span></span>

### <span data-ttu-id="db925-152">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="db925-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="db925-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="db925-153">ALIASES</span></span>

## <span data-ttu-id="db925-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db925-154">NOTES</span></span>

<span data-ttu-id="db925-155">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="db925-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db925-156">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db925-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="db925-157">PLANDEFINITION <IPlan> : en plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="db925-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="db925-158">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="db925-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="db925-159">`[Location <String>]`: Resursens plats</span><span class="sxs-lookup"><span data-stu-id="db925-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="db925-160">`[Description <String>]`: Beskrivning av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="db925-161">`[DisplayName <String>]`: Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="db925-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="db925-162">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="db925-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="db925-163">`[PropertiesName <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="db925-164">`[QuotaIds <String[]>]`: Kvot-ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db925-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="db925-165">`[SkuIds <String[]>]`: SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="db925-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="db925-166">`[SubscriptionCount <Int32?>]`: Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="db925-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="db925-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db925-167">RELATED LINKS</span></span>

