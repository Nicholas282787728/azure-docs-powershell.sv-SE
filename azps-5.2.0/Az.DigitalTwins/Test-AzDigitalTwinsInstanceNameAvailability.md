---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402408"
---
# <span data-ttu-id="7b50a-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7b50a-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="7b50a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b50a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b50a-103">Kontrol lera om det finns ett DigitalTwinsInstance-namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="7b50a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b50a-104">SYNTAX</span></span>

### <span data-ttu-id="7b50a-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7b50a-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b50a-106">Igen</span><span class="sxs-lookup"><span data-stu-id="7b50a-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b50a-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b50a-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7b50a-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7b50a-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b50a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b50a-109">DESCRIPTION</span></span>
<span data-ttu-id="7b50a-110">Kontrol lera om det finns ett DigitalTwinsInstance-namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="7b50a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b50a-111">EXAMPLES</span></span>

### <span data-ttu-id="7b50a-112">Exempel 1: kontrol lera namnet efter plats och namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="7b50a-113">Kontrol lera tillgängligheten för namnet efter plats och namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="7b50a-114">Exempel 2: kontrol lera namnet med DigitalTwinsObject och CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="7b50a-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="7b50a-115">Hämta en DigitalTwinsInstance och skapa ett Requset-objekt för att testa tillgängligheten för namnet.</span><span class="sxs-lookup"><span data-stu-id="7b50a-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="7b50a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b50a-116">PARAMETERS</span></span>

### <span data-ttu-id="7b50a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b50a-117">-DefaultProfile</span></span>
<span data-ttu-id="7b50a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b50a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b50a-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="7b50a-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="7b50a-120">Resultatet som returneras från en begäran om namn tillgänglighet för databas kontroll.</span><span class="sxs-lookup"><span data-stu-id="7b50a-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="7b50a-121">För att konstruera kan du läsa avsnittet anteckningar för DIGITALTWINSINSTANCECHECKNAME-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7b50a-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b50a-122">-InputObject</span></span>
<span data-ttu-id="7b50a-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7b50a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="7b50a-124">-Location</span></span>
<span data-ttu-id="7b50a-125">Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7b50a-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b50a-126">-Name</span></span>
<span data-ttu-id="7b50a-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b50a-128">-SubscriptionId</span></span>
<span data-ttu-id="7b50a-129">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="7b50a-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b50a-130">-Confirm</span></span>
<span data-ttu-id="7b50a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b50a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b50a-132">-WhatIf</span></span>
<span data-ttu-id="7b50a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b50a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b50a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b50a-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b50a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b50a-135">CommonParameters</span></span>
<span data-ttu-id="7b50a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b50a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b50a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b50a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b50a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b50a-138">INPUTS</span></span>

### <span data-ttu-id="7b50a-139">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="7b50a-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="7b50a-140">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7b50a-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="7b50a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b50a-141">OUTPUTS</span></span>

### <span data-ttu-id="7b50a-142">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="7b50a-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="7b50a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b50a-143">NOTES</span></span>

<span data-ttu-id="7b50a-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7b50a-144">ALIASES</span></span>

<span data-ttu-id="7b50a-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7b50a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b50a-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7b50a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b50a-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b50a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b50a-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest> : resultatet returneras från en begäran om namn tillgänglighet för databasen.</span><span class="sxs-lookup"><span data-stu-id="7b50a-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="7b50a-149">`Name <String>`: Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="7b50a-150">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7b50a-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b50a-151">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="7b50a-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="7b50a-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7b50a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b50a-153">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7b50a-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7b50a-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7b50a-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7b50a-155">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7b50a-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7b50a-156">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="7b50a-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7b50a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b50a-157">RELATED LINKS</span></span>

