---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925389"
---
# <span data-ttu-id="e4c95-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="e4c95-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="e4c95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4c95-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c95-103">Returnerar den begärda hälso statusen för en region.</span><span class="sxs-lookup"><span data-stu-id="e4c95-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="e4c95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4c95-104">SYNTAX</span></span>

### <span data-ttu-id="e4c95-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="e4c95-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e4c95-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4c95-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4c95-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="e4c95-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e4c95-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4c95-108">DESCRIPTION</span></span>
<span data-ttu-id="e4c95-109">Returnerar den begärda hälso statusen för en region.</span><span class="sxs-lookup"><span data-stu-id="e4c95-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="e4c95-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4c95-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c95-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="e4c95-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="e4c95-112">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="e4c95-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="e4c95-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4c95-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c95-114">-DefaultProfile</span></span>
<span data-ttu-id="e4c95-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c95-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e4c95-116">-Filter</span></span>
<span data-ttu-id="e4c95-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="e4c95-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e4c95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c95-118">-InputObject</span></span>
<span data-ttu-id="e4c95-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e4c95-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4c95-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="e4c95-120">-Location</span></span>
<span data-ttu-id="e4c95-121">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="e4c95-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c95-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4c95-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e4c95-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4c95-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4c95-124">-SubscriptionId</span></span>
<span data-ttu-id="e4c95-125">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e4c95-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4c95-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e4c95-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4c95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c95-127">CommonParameters</span></span>
<span data-ttu-id="e4c95-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c95-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4c95-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c95-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4c95-130">INPUTS</span></span>

### <span data-ttu-id="e4c95-131">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e4c95-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="e4c95-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4c95-132">OUTPUTS</span></span>

### <span data-ttu-id="e4c95-133">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="e4c95-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="e4c95-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4c95-134">NOTES</span></span>

<span data-ttu-id="e4c95-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e4c95-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4c95-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4c95-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e4c95-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e4c95-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4c95-138">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="e4c95-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="e4c95-139">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e4c95-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4c95-140">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="e4c95-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="e4c95-141">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e4c95-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e4c95-142">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="e4c95-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="e4c95-143">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="e4c95-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="e4c95-144">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="e4c95-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="e4c95-145">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e4c95-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e4c95-146">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e4c95-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4c95-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4c95-147">RELATED LINKS</span></span>
