---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099972"
---
# <span data-ttu-id="38b4f-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="38b4f-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="38b4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="38b4f-103">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="38b4f-103">Get an update location based on name.</span></span>

## <span data-ttu-id="38b4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38b4f-104">SYNTAX</span></span>

### <span data-ttu-id="38b4f-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="38b4f-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38b4f-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38b4f-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38b4f-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="38b4f-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="38b4f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38b4f-108">DESCRIPTION</span></span>
<span data-ttu-id="38b4f-109">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="38b4f-109">Get an update location based on name.</span></span>

## <span data-ttu-id="38b4f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38b4f-110">EXAMPLES</span></span>

### <span data-ttu-id="38b4f-111">Exempel 1: Hämta alla uppdateringar</span><span class="sxs-lookup"><span data-stu-id="38b4f-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="38b4f-112">Utan parametrar kommer detta cmdleten att hämta alla uppdaterings platser</span><span class="sxs-lookup"><span data-stu-id="38b4f-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="38b4f-113">Exempel 2: Hämta alla uppdateringar med namn</span><span class="sxs-lookup"><span data-stu-id="38b4f-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="38b4f-114">Hämtar alla uppdaterings platser som matchar angiven namn parameter</span><span class="sxs-lookup"><span data-stu-id="38b4f-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="38b4f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38b4f-115">PARAMETERS</span></span>

### <span data-ttu-id="38b4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b4f-116">-DefaultProfile</span></span>
<span data-ttu-id="38b4f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38b4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b4f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b4f-118">-InputObject</span></span>
<span data-ttu-id="38b4f-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="38b4f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38b4f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="38b4f-120">-Name</span></span>
<span data-ttu-id="38b4f-121">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="38b4f-121">The name of the update location.</span></span>

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

### <span data-ttu-id="38b4f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b4f-122">-ResourceGroupName</span></span>
<span data-ttu-id="38b4f-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="38b4f-123">Resource group name.</span></span>

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

### <span data-ttu-id="38b4f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38b4f-124">-SubscriptionId</span></span>
<span data-ttu-id="38b4f-125">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="38b4f-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="38b4f-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="38b4f-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="38b4f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b4f-127">CommonParameters</span></span>
<span data-ttu-id="38b4f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b4f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b4f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38b4f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b4f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38b4f-130">INPUTS</span></span>

### <span data-ttu-id="38b4f-131">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="38b4f-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="38b4f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38b4f-132">OUTPUTS</span></span>

### <span data-ttu-id="38b4f-133">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="38b4f-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="38b4f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38b4f-134">NOTES</span></span>

<span data-ttu-id="38b4f-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="38b4f-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38b4f-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38b4f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="38b4f-137">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="38b4f-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38b4f-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="38b4f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38b4f-139">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="38b4f-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="38b4f-140">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="38b4f-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="38b4f-141">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="38b4f-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="38b4f-142">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="38b4f-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="38b4f-143">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="38b4f-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="38b4f-144">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="38b4f-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="38b4f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38b4f-145">RELATED LINKS</span></span>

