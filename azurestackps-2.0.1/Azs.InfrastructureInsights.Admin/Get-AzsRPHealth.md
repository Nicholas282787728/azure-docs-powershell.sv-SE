---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093020"
---
# <span data-ttu-id="f9473-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="f9473-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="f9473-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9473-102">SYNOPSIS</span></span>
<span data-ttu-id="f9473-103">Returnerar den begärda tjänstens hälso objekt.</span><span class="sxs-lookup"><span data-stu-id="f9473-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="f9473-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9473-104">SYNTAX</span></span>

### <span data-ttu-id="f9473-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f9473-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9473-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f9473-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9473-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f9473-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9473-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9473-108">DESCRIPTION</span></span>
<span data-ttu-id="f9473-109">Returnerar den begärda tjänstens hälso objekt.</span><span class="sxs-lookup"><span data-stu-id="f9473-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="f9473-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9473-110">EXAMPLES</span></span>

### <span data-ttu-id="f9473-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="f9473-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="f9473-112">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="f9473-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="f9473-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="f9473-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="f9473-114">Returnerar tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="f9473-114">Returns a service's health.</span></span>

## <span data-ttu-id="f9473-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9473-115">PARAMETERS</span></span>

### <span data-ttu-id="f9473-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9473-116">-DefaultProfile</span></span>
<span data-ttu-id="f9473-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9473-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9473-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="f9473-118">-Filter</span></span>
<span data-ttu-id="f9473-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="f9473-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="f9473-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9473-120">-InputObject</span></span>
<span data-ttu-id="f9473-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f9473-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9473-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9473-122">-Location</span></span>
<span data-ttu-id="f9473-123">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="f9473-123">Name of the region</span></span>

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

### <span data-ttu-id="f9473-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9473-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9473-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9473-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9473-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="f9473-126">-ServiceHealth</span></span>
<span data-ttu-id="f9473-127">Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="f9473-127">Service Health name.</span></span>

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

### <span data-ttu-id="f9473-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9473-128">-SubscriptionId</span></span>
<span data-ttu-id="f9473-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f9473-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9473-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f9473-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f9473-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9473-131">CommonParameters</span></span>
<span data-ttu-id="f9473-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9473-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9473-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9473-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9473-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9473-134">INPUTS</span></span>

### <span data-ttu-id="f9473-135">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f9473-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="f9473-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9473-136">OUTPUTS</span></span>

### <span data-ttu-id="f9473-137">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="f9473-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="f9473-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9473-138">NOTES</span></span>

<span data-ttu-id="f9473-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f9473-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9473-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9473-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f9473-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f9473-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9473-142">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="f9473-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="f9473-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f9473-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9473-144">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="f9473-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="f9473-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9473-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f9473-146">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="f9473-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="f9473-147">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="f9473-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="f9473-148">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="f9473-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="f9473-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f9473-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9473-150">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f9473-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f9473-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9473-151">RELATED LINKS</span></span>

