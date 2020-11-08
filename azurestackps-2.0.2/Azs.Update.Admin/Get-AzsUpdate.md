---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099839"
---
# <span data-ttu-id="1e6b5-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="1e6b5-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="1e6b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6b5-103">Skaffa en specifik uppdatering till en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="1e6b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e6b5-104">SYNTAX</span></span>

### <span data-ttu-id="1e6b5-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1e6b5-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e6b5-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1e6b5-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e6b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e6b5-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1e6b5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e6b5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e6b5-109">Skaffa en specifik uppdatering till en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="1e6b5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e6b5-110">EXAMPLES</span></span>

### <span data-ttu-id="1e6b5-111">Exempel 1: Hämta alla uppdateringar</span><span class="sxs-lookup"><span data-stu-id="1e6b5-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="1e6b5-112">Utan parametrar visar Get-AzsUpdate alla uppdateringar som Stamp kan upptäcka</span><span class="sxs-lookup"><span data-stu-id="1e6b5-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="1e6b5-113">Exempel 2: Hämta uppdatering efter namn</span><span class="sxs-lookup"><span data-stu-id="1e6b5-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="1e6b5-114">Hämtar alla uppdateringar som motsvarar det angivna namnet</span><span class="sxs-lookup"><span data-stu-id="1e6b5-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="1e6b5-115">Exempel 3: Hämta alla uppdateringar efter plats</span><span class="sxs-lookup"><span data-stu-id="1e6b5-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="1e6b5-116">Hämtar alla uppdateringar inom en angiven plats.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="1e6b5-117">För närvarande stöds endast en plats, så detta är det som bara Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="1e6b5-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="1e6b5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e6b5-118">PARAMETERS</span></span>

### <span data-ttu-id="1e6b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6b5-119">-DefaultProfile</span></span>
<span data-ttu-id="1e6b5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6b5-121">-InputObject</span></span>
<span data-ttu-id="1e6b5-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e6b5-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="1e6b5-123">-Location</span></span>
<span data-ttu-id="1e6b5-124">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-124">The name of the update location.</span></span>

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

### <span data-ttu-id="1e6b5-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e6b5-125">-Name</span></span>
<span data-ttu-id="1e6b5-126">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-126">Name of the update.</span></span>

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

### <span data-ttu-id="1e6b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e6b5-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-128">Resource group name.</span></span>

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

### <span data-ttu-id="1e6b5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e6b5-129">-SubscriptionId</span></span>
<span data-ttu-id="1e6b5-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e6b5-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1e6b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6b5-132">CommonParameters</span></span>
<span data-ttu-id="1e6b5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6b5-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e6b5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6b5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e6b5-135">INPUTS</span></span>

### <span data-ttu-id="1e6b5-136">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1e6b5-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="1e6b5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e6b5-137">OUTPUTS</span></span>

### <span data-ttu-id="1e6b5-138">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="1e6b5-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="1e6b5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e6b5-139">NOTES</span></span>

<span data-ttu-id="1e6b5-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e6b5-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1e6b5-142">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1e6b5-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e6b5-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1e6b5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e6b5-144">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="1e6b5-145">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="1e6b5-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="1e6b5-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1e6b5-148">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="1e6b5-149">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="1e6b5-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e6b5-150">RELATED LINKS</span></span>

