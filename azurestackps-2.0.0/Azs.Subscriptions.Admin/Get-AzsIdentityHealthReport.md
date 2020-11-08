---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092859"
---
# <span data-ttu-id="e335f-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="e335f-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="e335f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e335f-102">SYNOPSIS</span></span>
<span data-ttu-id="e335f-103">Kontrollerar identitets tillståndet</span><span class="sxs-lookup"><span data-stu-id="e335f-103">Checks the identity health</span></span>

## <span data-ttu-id="e335f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e335f-104">SYNTAX</span></span>

### <span data-ttu-id="e335f-105">Kontrol lera (standard)</span><span class="sxs-lookup"><span data-stu-id="e335f-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e335f-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e335f-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e335f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e335f-107">DESCRIPTION</span></span>
<span data-ttu-id="e335f-108">Kontrollerar identitets tillståndet</span><span class="sxs-lookup"><span data-stu-id="e335f-108">Checks the identity health</span></span>

## <span data-ttu-id="e335f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e335f-109">EXAMPLES</span></span>

### <span data-ttu-id="e335f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e335f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="e335f-111">Få statusen för identitets tillståndet.</span><span class="sxs-lookup"><span data-stu-id="e335f-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="e335f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e335f-112">PARAMETERS</span></span>

### <span data-ttu-id="e335f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e335f-113">-DefaultProfile</span></span>
<span data-ttu-id="e335f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e335f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e335f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e335f-115">-InputObject</span></span>
<span data-ttu-id="e335f-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e335f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e335f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e335f-117">-SubscriptionId</span></span>
<span data-ttu-id="e335f-118">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e335f-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e335f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e335f-119">-Confirm</span></span>
<span data-ttu-id="e335f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e335f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e335f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e335f-121">-WhatIf</span></span>
<span data-ttu-id="e335f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e335f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e335f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e335f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e335f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e335f-124">CommonParameters</span></span>
<span data-ttu-id="e335f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e335f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e335f-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e335f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e335f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e335f-127">INPUTS</span></span>

### <span data-ttu-id="e335f-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e335f-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e335f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e335f-129">OUTPUTS</span></span>

### <span data-ttu-id="e335f-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="e335f-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="e335f-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e335f-131">ALIASES</span></span>

## <span data-ttu-id="e335f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e335f-132">NOTES</span></span>

<span data-ttu-id="e335f-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e335f-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e335f-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e335f-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e335f-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e335f-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e335f-136">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="e335f-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e335f-137">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="e335f-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e335f-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e335f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e335f-139">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="e335f-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e335f-140">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="e335f-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e335f-141">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="e335f-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e335f-142">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="e335f-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e335f-143">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="e335f-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e335f-144">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e335f-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e335f-145">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e335f-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e335f-146">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="e335f-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e335f-147">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="e335f-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e335f-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e335f-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e335f-149">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e335f-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e335f-150">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="e335f-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e335f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e335f-151">RELATED LINKS</span></span>

