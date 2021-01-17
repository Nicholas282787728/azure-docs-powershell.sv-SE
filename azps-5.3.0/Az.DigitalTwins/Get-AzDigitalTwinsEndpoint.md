---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420419"
---
# <span data-ttu-id="439b4-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="439b4-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="439b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="439b4-102">SYNOPSIS</span></span>
<span data-ttu-id="439b4-103">Få DigitalTwinsInstances slut punkt.</span><span class="sxs-lookup"><span data-stu-id="439b4-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="439b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="439b4-104">SYNTAX</span></span>

### <span data-ttu-id="439b4-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="439b4-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="439b4-106">Lära</span><span class="sxs-lookup"><span data-stu-id="439b4-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="439b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="439b4-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="439b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="439b4-108">DESCRIPTION</span></span>
<span data-ttu-id="439b4-109">Få DigitalTwinsInstances slut punkt.</span><span class="sxs-lookup"><span data-stu-id="439b4-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="439b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="439b4-110">EXAMPLES</span></span>

### <span data-ttu-id="439b4-111">Exempel 1: list AzDigitalTwinsEndpoint i ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="439b4-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="439b4-112">Lista alla AzDigitalTwinsEndpoints med ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439b4-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="439b4-113">Exempel 2: get AzDigitalTwinsEndpoint by EndpointName</span><span class="sxs-lookup"><span data-stu-id="439b4-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="439b4-114">Få AzDigitalTwinsEndpoint via EndpointName i ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="439b4-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="439b4-115">Exempel 3: get AzDigitalTwinsEndpoint by ' AzDigitalTwinsEndpoint '-objekt</span><span class="sxs-lookup"><span data-stu-id="439b4-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="439b4-116">Hämta AzDigitalTwinsEndpoint via ' AzDigitalTwinsEndpoint '-objekt</span><span class="sxs-lookup"><span data-stu-id="439b4-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="439b4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="439b4-117">PARAMETERS</span></span>

### <span data-ttu-id="439b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439b4-118">-DefaultProfile</span></span>
<span data-ttu-id="439b4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="439b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439b4-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="439b4-120">-EndpointName</span></span>
<span data-ttu-id="439b4-121">Namn på slut punkts resurs.</span><span class="sxs-lookup"><span data-stu-id="439b4-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="439b4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="439b4-122">-InputObject</span></span>
<span data-ttu-id="439b4-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="439b4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="439b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="439b4-125">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="439b4-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="439b4-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="439b4-126">-ResourceName</span></span>
<span data-ttu-id="439b4-127">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="439b4-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="439b4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="439b4-128">-SubscriptionId</span></span>
<span data-ttu-id="439b4-129">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="439b4-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="439b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439b4-130">CommonParameters</span></span>
<span data-ttu-id="439b4-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439b4-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="439b4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439b4-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="439b4-133">INPUTS</span></span>

### <span data-ttu-id="439b4-134">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="439b4-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="439b4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="439b4-135">OUTPUTS</span></span>

### <span data-ttu-id="439b4-136">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="439b4-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="439b4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="439b4-137">NOTES</span></span>

<span data-ttu-id="439b4-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="439b4-138">ALIASES</span></span>

<span data-ttu-id="439b4-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="439b4-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="439b4-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="439b4-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="439b4-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="439b4-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="439b4-142">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="439b4-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="439b4-143">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="439b4-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="439b4-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="439b4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="439b4-145">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="439b4-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="439b4-146">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="439b4-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="439b4-147">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="439b4-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="439b4-148">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="439b4-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="439b4-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="439b4-149">RELATED LINKS</span></span>

