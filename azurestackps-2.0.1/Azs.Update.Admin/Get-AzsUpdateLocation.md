---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092921"
---
# <span data-ttu-id="b0d44-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="b0d44-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="b0d44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0d44-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d44-103">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="b0d44-103">Get an update location based on name.</span></span>

## <span data-ttu-id="b0d44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0d44-104">SYNTAX</span></span>

### <span data-ttu-id="b0d44-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="b0d44-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0d44-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0d44-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0d44-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="b0d44-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0d44-108">DESCRIPTION</span></span>
<span data-ttu-id="b0d44-109">Skaffa en uppdaterings plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="b0d44-109">Get an update location based on name.</span></span>

## <span data-ttu-id="b0d44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0d44-110">EXAMPLES</span></span>

### <span data-ttu-id="b0d44-111">Exempel 1: Hämta alla uppdateringar</span><span class="sxs-lookup"><span data-stu-id="b0d44-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="b0d44-112">Utan parametrar kommer detta cmdleten att hämta alla uppdaterings platser</span><span class="sxs-lookup"><span data-stu-id="b0d44-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="b0d44-113">Exempel 2: Hämta alla uppdateringar med namn</span><span class="sxs-lookup"><span data-stu-id="b0d44-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="b0d44-114">Hämtar alla uppdaterings platser som matchar angiven namn parameter</span><span class="sxs-lookup"><span data-stu-id="b0d44-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="b0d44-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0d44-115">PARAMETERS</span></span>

### <span data-ttu-id="b0d44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d44-116">-DefaultProfile</span></span>
<span data-ttu-id="b0d44-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0d44-118">-InputObject</span></span>
<span data-ttu-id="b0d44-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b0d44-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b0d44-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0d44-120">-Name</span></span>
<span data-ttu-id="b0d44-121">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="b0d44-121">The name of the update location.</span></span>

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

### <span data-ttu-id="b0d44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d44-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0d44-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b0d44-123">Resource group name.</span></span>

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

### <span data-ttu-id="b0d44-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0d44-124">-SubscriptionId</span></span>
<span data-ttu-id="b0d44-125">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b0d44-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0d44-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b0d44-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b0d44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d44-127">CommonParameters</span></span>
<span data-ttu-id="b0d44-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d44-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d44-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d44-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0d44-130">INPUTS</span></span>

### <span data-ttu-id="b0d44-131">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b0d44-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="b0d44-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0d44-132">OUTPUTS</span></span>

### <span data-ttu-id="b0d44-133">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="b0d44-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="b0d44-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0d44-134">NOTES</span></span>

<span data-ttu-id="b0d44-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b0d44-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0d44-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0d44-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b0d44-137">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b0d44-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0d44-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b0d44-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0d44-139">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b0d44-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="b0d44-140">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="b0d44-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="b0d44-141">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b0d44-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="b0d44-142">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b0d44-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0d44-143">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="b0d44-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="b0d44-144">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="b0d44-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="b0d44-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0d44-145">RELATED LINKS</span></span>
