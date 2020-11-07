---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921935"
---
# <span data-ttu-id="5ce64-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="5ce64-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="5ce64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ce64-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce64-103">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="5ce64-103">Get an update location based on name.</span></span>

## <span data-ttu-id="5ce64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ce64-104">SYNTAX</span></span>

### <span data-ttu-id="5ce64-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="5ce64-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce64-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce64-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce64-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="5ce64-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce64-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ce64-108">DESCRIPTION</span></span>
<span data-ttu-id="5ce64-109">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="5ce64-109">Get an update location based on name.</span></span>

## <span data-ttu-id="5ce64-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ce64-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce64-111">Exempel 1: Hämta alla uppdateringar</span><span class="sxs-lookup"><span data-stu-id="5ce64-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="5ce64-112">Utan parametrar kommer detta cmdleten att hämta alla uppdaterings platser</span><span class="sxs-lookup"><span data-stu-id="5ce64-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="5ce64-113">Exempel 2: Hämta alla uppdateringar med namn</span><span class="sxs-lookup"><span data-stu-id="5ce64-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="5ce64-114">Hämtar alla uppdaterings platser som matchar angiven namn parameter</span><span class="sxs-lookup"><span data-stu-id="5ce64-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="5ce64-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ce64-115">PARAMETERS</span></span>

### <span data-ttu-id="5ce64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce64-116">-DefaultProfile</span></span>
<span data-ttu-id="5ce64-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce64-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce64-118">-InputObject</span></span>
<span data-ttu-id="5ce64-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5ce64-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5ce64-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ce64-120">-Name</span></span>
<span data-ttu-id="5ce64-121">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="5ce64-121">The name of the update location.</span></span>

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

### <span data-ttu-id="5ce64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce64-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ce64-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5ce64-123">Resource group name.</span></span>

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

### <span data-ttu-id="5ce64-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ce64-124">-SubscriptionId</span></span>
<span data-ttu-id="5ce64-125">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5ce64-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ce64-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5ce64-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ce64-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce64-127">CommonParameters</span></span>
<span data-ttu-id="5ce64-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce64-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce64-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce64-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce64-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ce64-130">INPUTS</span></span>

### <span data-ttu-id="5ce64-131">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce64-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="5ce64-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ce64-132">OUTPUTS</span></span>

### <span data-ttu-id="5ce64-133">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="5ce64-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="5ce64-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ce64-134">NOTES</span></span>

<span data-ttu-id="5ce64-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5ce64-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ce64-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ce64-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5ce64-137">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5ce64-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ce64-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5ce64-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ce64-139">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5ce64-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="5ce64-140">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="5ce64-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="5ce64-141">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5ce64-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="5ce64-142">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5ce64-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5ce64-143">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="5ce64-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="5ce64-144">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="5ce64-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="5ce64-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ce64-145">RELATED LINKS</span></span>

