---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 1a5cfb9f9bc7edb436d37847fc117565c3b71221
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921936"
---
# <span data-ttu-id="954a7-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="954a7-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="954a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="954a7-102">SYNOPSIS</span></span>
<span data-ttu-id="954a7-103">Få en instans av Update-körningen med hjälp av ID.</span><span class="sxs-lookup"><span data-stu-id="954a7-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="954a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="954a7-104">SYNTAX</span></span>

### <span data-ttu-id="954a7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="954a7-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="954a7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="954a7-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="954a7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="954a7-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="954a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="954a7-108">DESCRIPTION</span></span>
<span data-ttu-id="954a7-109">Få en instans av Update-körningen med hjälp av ID.</span><span class="sxs-lookup"><span data-stu-id="954a7-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="954a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="954a7-110">EXAMPLES</span></span>

### <span data-ttu-id="954a7-111">Exempel 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="954a7-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="954a7-112">Om inget UpdateName-värde anges frågar Get-UpdateRun alltid efter indata.</span><span class="sxs-lookup"><span data-stu-id="954a7-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="954a7-113">När det är angivet kommer det att ta med alla instanser av UpdateRun som misslyckats eller lyckats</span><span class="sxs-lookup"><span data-stu-id="954a7-113">Once provided, it will output all instances of UpdateRun that were Failed or Successfull</span></span>

### <span data-ttu-id="954a7-114">Exempel 2: Get-AzsUpdateRun genom UpdateName</span><span class="sxs-lookup"><span data-stu-id="954a7-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="954a7-115">Hämtar alla UpdateRuns som är kopplade till en viss uppdatering</span><span class="sxs-lookup"><span data-stu-id="954a7-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="954a7-116">Exempel 2: Get-AzsUpdateRun efter namn</span><span class="sxs-lookup"><span data-stu-id="954a7-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="954a7-117">Hämtar alla UpdateRuns som är kopplade till en viss uppdatering och ett visst namn</span><span class="sxs-lookup"><span data-stu-id="954a7-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="954a7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="954a7-118">PARAMETERS</span></span>

### <span data-ttu-id="954a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954a7-119">-DefaultProfile</span></span>
<span data-ttu-id="954a7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="954a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="954a7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="954a7-121">-InputObject</span></span>
<span data-ttu-id="954a7-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="954a7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="954a7-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="954a7-123">-Location</span></span>
<span data-ttu-id="954a7-124">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="954a7-124">The name of the update location.</span></span>

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

### <span data-ttu-id="954a7-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="954a7-125">-Name</span></span>
<span data-ttu-id="954a7-126">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="954a7-126">Update run identifier.</span></span>

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

### <span data-ttu-id="954a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="954a7-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="954a7-128">Resource group name.</span></span>

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

### <span data-ttu-id="954a7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="954a7-129">-SubscriptionId</span></span>
<span data-ttu-id="954a7-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="954a7-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="954a7-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="954a7-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="954a7-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="954a7-132">-UpdateName</span></span>
<span data-ttu-id="954a7-133">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="954a7-133">Name of the update.</span></span>

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

### <span data-ttu-id="954a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954a7-134">CommonParameters</span></span>
<span data-ttu-id="954a7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954a7-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="954a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954a7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="954a7-137">INPUTS</span></span>

### <span data-ttu-id="954a7-138">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="954a7-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="954a7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="954a7-139">OUTPUTS</span></span>

### <span data-ttu-id="954a7-140">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="954a7-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="954a7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="954a7-141">NOTES</span></span>

<span data-ttu-id="954a7-142">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="954a7-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="954a7-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="954a7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="954a7-144">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="954a7-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="954a7-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="954a7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="954a7-146">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="954a7-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="954a7-147">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="954a7-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="954a7-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="954a7-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="954a7-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="954a7-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="954a7-150">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="954a7-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="954a7-151">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="954a7-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="954a7-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="954a7-152">RELATED LINKS</span></span>
