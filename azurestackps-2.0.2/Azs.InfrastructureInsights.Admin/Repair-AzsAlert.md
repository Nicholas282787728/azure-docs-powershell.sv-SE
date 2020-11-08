---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100086"
---
# <span data-ttu-id="c4ac8-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c4ac8-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="c4ac8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ac8-103">Reparerar en avisering.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-103">Repairs an alert.</span></span>

## <span data-ttu-id="c4ac8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4ac8-104">SYNTAX</span></span>

### <span data-ttu-id="c4ac8-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="c4ac8-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4ac8-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ac8-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4ac8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4ac8-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ac8-108">Reparerar en avisering.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-108">Repairs an alert.</span></span>

## <span data-ttu-id="c4ac8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4ac8-109">EXAMPLES</span></span>

### <span data-ttu-id="c4ac8-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="c4ac8-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="c4ac8-111">Reparerar en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="c4ac8-112">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="c4ac8-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="c4ac8-113">Reparerar en avisering genom rörledningar.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="c4ac8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4ac8-114">PARAMETERS</span></span>

### <span data-ttu-id="c4ac8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4ac8-115">-AsJob</span></span>
<span data-ttu-id="c4ac8-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c4ac8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c4ac8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ac8-117">-DefaultProfile</span></span>
<span data-ttu-id="c4ac8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ac8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4ac8-119">-InputObject</span></span>
<span data-ttu-id="c4ac8-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c4ac8-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4ac8-121">-Location</span></span>
<span data-ttu-id="c4ac8-122">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="c4ac8-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4ac8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4ac8-123">-Name</span></span>
<span data-ttu-id="c4ac8-124">Namn på aviseringen.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4ac8-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c4ac8-125">-NoWait</span></span>
<span data-ttu-id="c4ac8-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c4ac8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4ac8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ac8-127">-PassThru</span></span>
<span data-ttu-id="c4ac8-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="c4ac8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4ac8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ac8-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4ac8-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4ac8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4ac8-131">-SubscriptionId</span></span>
<span data-ttu-id="c4ac8-132">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4ac8-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4ac8-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4ac8-134">-Confirm</span></span>
<span data-ttu-id="c4ac8-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ac8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ac8-136">-WhatIf</span></span>
<span data-ttu-id="c4ac8-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ac8-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ac8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ac8-139">CommonParameters</span></span>
<span data-ttu-id="c4ac8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ac8-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4ac8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ac8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4ac8-142">INPUTS</span></span>

### <span data-ttu-id="c4ac8-143">Microsoft. Azure. PowerShell. cmdletar. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ac8-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="c4ac8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4ac8-144">OUTPUTS</span></span>

### <span data-ttu-id="c4ac8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4ac8-145">System.Boolean</span></span>



## <span data-ttu-id="c4ac8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4ac8-146">NOTES</span></span>

<span data-ttu-id="c4ac8-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4ac8-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c4ac8-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c4ac8-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4ac8-150">`[AlertName <String>]`: Aviseringens namn.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="c4ac8-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c4ac8-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4ac8-152">`[Location <String>]`: Regionens namn</span><span class="sxs-lookup"><span data-stu-id="c4ac8-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="c4ac8-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c4ac8-154">`[ResourceRegistrationId <String>]`: Registrerings-ID för resurs.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="c4ac8-155">`[ServiceHealth <String>]`: Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="c4ac8-156">`[ServiceRegistrationId <String>]`: ID för tjänste registrering.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="c4ac8-157">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4ac8-158">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c4ac8-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4ac8-159">RELATED LINKS</span></span>

