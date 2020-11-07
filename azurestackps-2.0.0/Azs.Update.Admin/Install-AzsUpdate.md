---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921937"
---
# <span data-ttu-id="230eb-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="230eb-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="230eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="230eb-102">SYNOPSIS</span></span>
<span data-ttu-id="230eb-103">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="230eb-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="230eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="230eb-104">SYNTAX</span></span>

### <span data-ttu-id="230eb-105">Tillämpa (standard)</span><span class="sxs-lookup"><span data-stu-id="230eb-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="230eb-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="230eb-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="230eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="230eb-107">DESCRIPTION</span></span>
<span data-ttu-id="230eb-108">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="230eb-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="230eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="230eb-109">EXAMPLES</span></span>

### <span data-ttu-id="230eb-110">Exempel 1: Install-AzsUpdate efter namn</span><span class="sxs-lookup"><span data-stu-id="230eb-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="230eb-111">Med cmdleten kan du installera specifika uppdateringar efter namn.</span><span class="sxs-lookup"><span data-stu-id="230eb-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="230eb-112">Observera att uppdaterings versionen är strikt större än den aktuella versionen.</span><span class="sxs-lookup"><span data-stu-id="230eb-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="230eb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="230eb-113">PARAMETERS</span></span>

### <span data-ttu-id="230eb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="230eb-114">-AsJob</span></span>
<span data-ttu-id="230eb-115">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="230eb-115">Run the command as a job</span></span>

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

### <span data-ttu-id="230eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230eb-116">-DefaultProfile</span></span>
<span data-ttu-id="230eb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="230eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="230eb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="230eb-118">-InputObject</span></span>
<span data-ttu-id="230eb-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="230eb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="230eb-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="230eb-120">-Location</span></span>
<span data-ttu-id="230eb-121">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="230eb-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="230eb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="230eb-122">-Name</span></span>
<span data-ttu-id="230eb-123">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="230eb-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="230eb-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="230eb-124">-NoWait</span></span>
<span data-ttu-id="230eb-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="230eb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="230eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="230eb-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="230eb-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="230eb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="230eb-128">-SubscriptionId</span></span>
<span data-ttu-id="230eb-129">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="230eb-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="230eb-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="230eb-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="230eb-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="230eb-131">-Confirm</span></span>
<span data-ttu-id="230eb-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="230eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="230eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="230eb-133">-WhatIf</span></span>
<span data-ttu-id="230eb-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="230eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="230eb-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="230eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="230eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230eb-136">CommonParameters</span></span>
<span data-ttu-id="230eb-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="230eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230eb-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="230eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230eb-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="230eb-139">INPUTS</span></span>

### <span data-ttu-id="230eb-140">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="230eb-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="230eb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="230eb-141">OUTPUTS</span></span>

### <span data-ttu-id="230eb-142">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="230eb-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="230eb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="230eb-143">NOTES</span></span>

<span data-ttu-id="230eb-144">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="230eb-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="230eb-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="230eb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="230eb-146">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="230eb-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="230eb-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="230eb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="230eb-148">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="230eb-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="230eb-149">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="230eb-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="230eb-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="230eb-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="230eb-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="230eb-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="230eb-152">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="230eb-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="230eb-153">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="230eb-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="230eb-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="230eb-154">RELATED LINKS</span></span>

