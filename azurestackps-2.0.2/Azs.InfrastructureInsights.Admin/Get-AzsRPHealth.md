---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100057"
---
# <span data-ttu-id="720d1-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="720d1-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="720d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="720d1-102">SYNOPSIS</span></span>
<span data-ttu-id="720d1-103">Returnerar den begärda tjänstens hälso objekt.</span><span class="sxs-lookup"><span data-stu-id="720d1-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="720d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="720d1-104">SYNTAX</span></span>

### <span data-ttu-id="720d1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="720d1-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="720d1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="720d1-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="720d1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="720d1-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="720d1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="720d1-108">DESCRIPTION</span></span>
<span data-ttu-id="720d1-109">Returnerar den begärda tjänstens hälso objekt.</span><span class="sxs-lookup"><span data-stu-id="720d1-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="720d1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="720d1-110">EXAMPLES</span></span>

### <span data-ttu-id="720d1-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="720d1-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="720d1-112">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="720d1-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="720d1-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="720d1-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="720d1-114">Returnerar tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="720d1-114">Returns a service's health.</span></span>

## <span data-ttu-id="720d1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="720d1-115">PARAMETERS</span></span>

### <span data-ttu-id="720d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720d1-116">-DefaultProfile</span></span>
<span data-ttu-id="720d1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="720d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="720d1-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="720d1-118">-Filter</span></span>
<span data-ttu-id="720d1-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="720d1-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="720d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="720d1-120">-InputObject</span></span>
<span data-ttu-id="720d1-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="720d1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="720d1-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="720d1-122">-Location</span></span>
<span data-ttu-id="720d1-123">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="720d1-123">Name of the region</span></span>

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

### <span data-ttu-id="720d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="720d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="720d1-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="720d1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="720d1-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="720d1-126">-ServiceHealth</span></span>
<span data-ttu-id="720d1-127">Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="720d1-127">Service Health name.</span></span>

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

### <span data-ttu-id="720d1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="720d1-128">-SubscriptionId</span></span>
<span data-ttu-id="720d1-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="720d1-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="720d1-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="720d1-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="720d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720d1-131">CommonParameters</span></span>
<span data-ttu-id="720d1-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720d1-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="720d1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720d1-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="720d1-134">INPUTS</span></span>

### <span data-ttu-id="720d1-135">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="720d1-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="720d1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="720d1-136">OUTPUTS</span></span>

### <span data-ttu-id="720d1-137">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="720d1-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="720d1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="720d1-138">NOTES</span></span>

<span data-ttu-id="720d1-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="720d1-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="720d1-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="720d1-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="720d1-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="720d1-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="720d1-142">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="720d1-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="720d1-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="720d1-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="720d1-144">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="720d1-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="720d1-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="720d1-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="720d1-146">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="720d1-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="720d1-147">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="720d1-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="720d1-148">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="720d1-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="720d1-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="720d1-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="720d1-150">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="720d1-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="720d1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="720d1-151">RELATED LINKS</span></span>

