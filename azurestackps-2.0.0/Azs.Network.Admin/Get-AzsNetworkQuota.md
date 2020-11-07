---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923113"
---
# <span data-ttu-id="fe022-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="fe022-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="fe022-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe022-102">SYNOPSIS</span></span>
<span data-ttu-id="fe022-103">Skaffa en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="fe022-103">Get a quota by name.</span></span>

## <span data-ttu-id="fe022-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe022-104">SYNTAX</span></span>

### <span data-ttu-id="fe022-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="fe022-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fe022-106">Lära</span><span class="sxs-lookup"><span data-stu-id="fe022-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fe022-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fe022-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="fe022-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe022-108">DESCRIPTION</span></span>
<span data-ttu-id="fe022-109">Lista alla kvoter.</span><span class="sxs-lookup"><span data-stu-id="fe022-109">List all quotas.</span></span>
<span data-ttu-id="fe022-110">Begränsa listan genom att skicka ett namn eller ett filter.</span><span class="sxs-lookup"><span data-stu-id="fe022-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="fe022-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe022-111">EXAMPLES</span></span>

### <span data-ttu-id="fe022-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe022-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="fe022-113">Visar alla nätverks kvoter.</span><span class="sxs-lookup"><span data-stu-id="fe022-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="fe022-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe022-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="fe022-115">Hämtar den angivna nätverks kvoten.</span><span class="sxs-lookup"><span data-stu-id="fe022-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="fe022-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe022-116">PARAMETERS</span></span>

### <span data-ttu-id="fe022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe022-117">-DefaultProfile</span></span>
<span data-ttu-id="fe022-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe022-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe022-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="fe022-119">-Filter</span></span>
<span data-ttu-id="fe022-120">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="fe022-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="fe022-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe022-121">-InputObject</span></span>
<span data-ttu-id="fe022-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fe022-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fe022-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe022-123">-Location</span></span>
<span data-ttu-id="fe022-124">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="fe022-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe022-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe022-125">-Name</span></span>
<span data-ttu-id="fe022-126">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="fe022-126">Name of the resource.</span></span>

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

### <span data-ttu-id="fe022-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe022-127">-PassThru</span></span>
<span data-ttu-id="fe022-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="fe022-128">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe022-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe022-129">-SubscriptionId</span></span>
<span data-ttu-id="fe022-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fe022-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe022-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fe022-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fe022-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe022-132">CommonParameters</span></span>
<span data-ttu-id="fe022-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe022-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe022-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe022-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe022-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe022-135">INPUTS</span></span>

### <span data-ttu-id="fe022-136">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fe022-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="fe022-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe022-137">OUTPUTS</span></span>

### <span data-ttu-id="fe022-138">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="fe022-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="fe022-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe022-139">NOTES</span></span>

<span data-ttu-id="fe022-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="fe022-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe022-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe022-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fe022-142">INPUTOBJECT <INetworkAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="fe022-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fe022-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="fe022-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fe022-144">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="fe022-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fe022-145">`[ResourceName <String>]`: Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="fe022-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="fe022-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe022-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fe022-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fe022-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fe022-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe022-148">RELATED LINKS</span></span>

