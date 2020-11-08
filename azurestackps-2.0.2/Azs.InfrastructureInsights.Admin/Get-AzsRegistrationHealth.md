---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099936"
---
# <span data-ttu-id="9a30d-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="9a30d-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="9a30d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a30d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a30d-103">Returnerar den begärda hälso informationen om en resurs.</span><span class="sxs-lookup"><span data-stu-id="9a30d-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="9a30d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a30d-104">SYNTAX</span></span>

### <span data-ttu-id="9a30d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9a30d-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9a30d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9a30d-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9a30d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a30d-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9a30d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a30d-108">DESCRIPTION</span></span>
<span data-ttu-id="9a30d-109">Returnerar den begärda hälso informationen om en resurs.</span><span class="sxs-lookup"><span data-stu-id="9a30d-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="9a30d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a30d-110">EXAMPLES</span></span>

### <span data-ttu-id="9a30d-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="9a30d-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="9a30d-112">Returnerar en lista över statusen för varje resurs under en tjänst.</span><span class="sxs-lookup"><span data-stu-id="9a30d-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="9a30d-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="9a30d-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="9a30d-114">Returnerar hälso status under a för Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="9a30d-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="9a30d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a30d-115">PARAMETERS</span></span>

### <span data-ttu-id="9a30d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a30d-116">-DefaultProfile</span></span>
<span data-ttu-id="9a30d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a30d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a30d-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="9a30d-118">-Filter</span></span>
<span data-ttu-id="9a30d-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="9a30d-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="9a30d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a30d-120">-InputObject</span></span>
<span data-ttu-id="9a30d-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9a30d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9a30d-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="9a30d-122">-Location</span></span>
<span data-ttu-id="9a30d-123">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="9a30d-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9a30d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a30d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a30d-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9a30d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9a30d-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="9a30d-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="9a30d-127">Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="9a30d-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="9a30d-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="9a30d-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="9a30d-129">Registrerings-ID för tjänst.</span><span class="sxs-lookup"><span data-stu-id="9a30d-129">Service registration ID.</span></span>

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

### <span data-ttu-id="9a30d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a30d-130">-SubscriptionId</span></span>
<span data-ttu-id="9a30d-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9a30d-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a30d-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9a30d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9a30d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a30d-133">CommonParameters</span></span>
<span data-ttu-id="9a30d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a30d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a30d-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a30d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a30d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a30d-136">INPUTS</span></span>

### <span data-ttu-id="9a30d-137">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9a30d-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="9a30d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a30d-138">OUTPUTS</span></span>

### <span data-ttu-id="9a30d-139">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="9a30d-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="9a30d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a30d-140">NOTES</span></span>

<span data-ttu-id="9a30d-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9a30d-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a30d-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a30d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9a30d-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9a30d-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a30d-144">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="9a30d-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="9a30d-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9a30d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a30d-146">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="9a30d-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="9a30d-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9a30d-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9a30d-148">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="9a30d-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="9a30d-149">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="9a30d-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="9a30d-150">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="9a30d-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="9a30d-151">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9a30d-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9a30d-152">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9a30d-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9a30d-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a30d-153">RELATED LINKS</span></span>

