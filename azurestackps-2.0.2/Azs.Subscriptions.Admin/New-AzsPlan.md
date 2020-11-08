---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100314"
---
# <span data-ttu-id="6d815-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="6d815-101">New-AzsPlan</span></span>

## <span data-ttu-id="6d815-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d815-102">SYNOPSIS</span></span>
<span data-ttu-id="6d815-103">Skapa eller uppdatera abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-103">Create or update the plan.</span></span>

## <span data-ttu-id="6d815-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d815-104">SYNTAX</span></span>

### <span data-ttu-id="6d815-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6d815-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d815-106">Göra</span><span class="sxs-lookup"><span data-stu-id="6d815-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d815-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d815-107">DESCRIPTION</span></span>
<span data-ttu-id="6d815-108">Skapa eller uppdatera abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-108">Create or update the plan.</span></span>

## <span data-ttu-id="6d815-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d815-109">EXAMPLES</span></span>

### <span data-ttu-id="6d815-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d815-110">Example 1</span></span>
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

<span data-ttu-id="6d815-111">Skapar en ny plan</span><span class="sxs-lookup"><span data-stu-id="6d815-111">Creates a new plan</span></span>

## <span data-ttu-id="6d815-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d815-112">PARAMETERS</span></span>

### <span data-ttu-id="6d815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d815-113">-DefaultProfile</span></span>
<span data-ttu-id="6d815-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d815-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d815-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6d815-115">-Description</span></span>
<span data-ttu-id="6d815-116">Beskrivning av planen.</span><span class="sxs-lookup"><span data-stu-id="6d815-116">Description of the plan.</span></span>

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

### <span data-ttu-id="6d815-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d815-117">-DisplayName</span></span>
<span data-ttu-id="6d815-118">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="6d815-118">Display name.</span></span>

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

### <span data-ttu-id="6d815-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="6d815-119">-ExternalReferenceId</span></span>
<span data-ttu-id="6d815-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="6d815-120">External reference identifier.</span></span>

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

### <span data-ttu-id="6d815-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6d815-121">-Location</span></span>
<span data-ttu-id="6d815-122">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="6d815-122">Location of the resource</span></span>

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

### <span data-ttu-id="6d815-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d815-123">-Name</span></span>
<span data-ttu-id="6d815-124">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-124">Name of the plan.</span></span>

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

### <span data-ttu-id="6d815-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="6d815-125">-PlanDefinition</span></span>
<span data-ttu-id="6d815-126">En plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="6d815-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="6d815-127">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="6d815-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="6d815-128">För att konstruera kan du läsa avsnittet anteckningar för PLANDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6d815-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d815-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="6d815-129">-PropertiesName</span></span>
<span data-ttu-id="6d815-130">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-130">Name of the plan.</span></span>

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

### <span data-ttu-id="6d815-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="6d815-131">-QuotaIds</span></span>
<span data-ttu-id="6d815-132">Kvot-ID: n under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-132">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="6d815-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d815-133">-ResourceGroupName</span></span>
<span data-ttu-id="6d815-134">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="6d815-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6d815-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="6d815-135">-SkuIds</span></span>
<span data-ttu-id="6d815-136">SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="6d815-136">SKU identifiers.</span></span>

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

### <span data-ttu-id="6d815-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="6d815-137">-SubscriptionCount</span></span>
<span data-ttu-id="6d815-138">Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="6d815-138">Subscription count.</span></span>

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

### <span data-ttu-id="6d815-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d815-139">-SubscriptionId</span></span>
<span data-ttu-id="6d815-140">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6d815-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d815-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d815-141">-Confirm</span></span>
<span data-ttu-id="6d815-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d815-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d815-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d815-143">-WhatIf</span></span>
<span data-ttu-id="6d815-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d815-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d815-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d815-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d815-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d815-146">CommonParameters</span></span>
<span data-ttu-id="6d815-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d815-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d815-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d815-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d815-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d815-149">INPUTS</span></span>

### <span data-ttu-id="6d815-150">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="6d815-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="6d815-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d815-151">OUTPUTS</span></span>

### <span data-ttu-id="6d815-152">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="6d815-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="6d815-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d815-153">ALIASES</span></span>

## <span data-ttu-id="6d815-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d815-154">NOTES</span></span>

<span data-ttu-id="6d815-155">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6d815-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d815-156">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d815-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6d815-157">PLANDEFINITION <IPlan> : en plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="6d815-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="6d815-158">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="6d815-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="6d815-159">`[Location <String>]`: Resursens plats</span><span class="sxs-lookup"><span data-stu-id="6d815-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="6d815-160">`[Description <String>]`: Beskrivning av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="6d815-161">`[DisplayName <String>]`: Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="6d815-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="6d815-162">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="6d815-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="6d815-163">`[PropertiesName <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="6d815-164">`[QuotaIds <String[]>]`: Kvot-ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d815-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="6d815-165">`[SkuIds <String[]>]`: SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="6d815-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="6d815-166">`[SubscriptionCount <Int32?>]`: Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="6d815-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="6d815-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d815-167">RELATED LINKS</span></span>

