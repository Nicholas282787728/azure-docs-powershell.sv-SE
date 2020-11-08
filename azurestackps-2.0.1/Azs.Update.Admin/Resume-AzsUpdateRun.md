---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092975"
---
# <span data-ttu-id="92f01-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="92f01-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="92f01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92f01-102">SYNOPSIS</span></span>
<span data-ttu-id="92f01-103">Återuppta en misslyckad uppdatering.</span><span class="sxs-lookup"><span data-stu-id="92f01-103">Resume a failed update.</span></span>

## <span data-ttu-id="92f01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92f01-104">SYNTAX</span></span>

### <span data-ttu-id="92f01-105">Kör om (standard)</span><span class="sxs-lookup"><span data-stu-id="92f01-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92f01-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92f01-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92f01-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92f01-107">DESCRIPTION</span></span>
<span data-ttu-id="92f01-108">Återuppta en misslyckad uppdatering.</span><span class="sxs-lookup"><span data-stu-id="92f01-108">Resume a failed update.</span></span>

## <span data-ttu-id="92f01-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92f01-109">EXAMPLES</span></span>

### <span data-ttu-id="92f01-110">Exempel 1: Resume-AzsUpdateRun efter namn och UpdateName</span><span class="sxs-lookup"><span data-stu-id="92f01-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="92f01-111">Med cmdleten kan du köra en viss misslyckad uppdaterings körning igen.</span><span class="sxs-lookup"><span data-stu-id="92f01-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="92f01-112">Observera att uppdaterings versionen är strikt större än den aktuella versionen.</span><span class="sxs-lookup"><span data-stu-id="92f01-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="92f01-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92f01-113">PARAMETERS</span></span>

### <span data-ttu-id="92f01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f01-114">-DefaultProfile</span></span>
<span data-ttu-id="92f01-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92f01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f01-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f01-116">-InputObject</span></span>
<span data-ttu-id="92f01-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="92f01-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="92f01-118">-Location</span></span>
<span data-ttu-id="92f01-119">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="92f01-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="92f01-120">-Name</span></span>
<span data-ttu-id="92f01-121">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="92f01-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92f01-122">-PassThru</span></span>
<span data-ttu-id="92f01-123">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="92f01-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92f01-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f01-124">-ResourceGroupName</span></span>
<span data-ttu-id="92f01-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="92f01-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92f01-126">-SubscriptionId</span></span>
<span data-ttu-id="92f01-127">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="92f01-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92f01-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="92f01-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="92f01-129">-UpdateName</span></span>
<span data-ttu-id="92f01-130">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="92f01-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92f01-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92f01-131">-Confirm</span></span>
<span data-ttu-id="92f01-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92f01-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f01-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f01-133">-WhatIf</span></span>
<span data-ttu-id="92f01-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92f01-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92f01-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92f01-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f01-136">CommonParameters</span></span>
<span data-ttu-id="92f01-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f01-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f01-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f01-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92f01-139">INPUTS</span></span>

### <span data-ttu-id="92f01-140">Microsoft. Azure. PowerShell. cmdletar. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="92f01-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="92f01-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92f01-141">OUTPUTS</span></span>

### <span data-ttu-id="92f01-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92f01-142">System.Boolean</span></span>



## <span data-ttu-id="92f01-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92f01-143">NOTES</span></span>

<span data-ttu-id="92f01-144">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="92f01-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92f01-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92f01-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="92f01-146">INPUTOBJECT <IUpdateAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="92f01-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92f01-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="92f01-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92f01-148">`[ResourceGroupName <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="92f01-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="92f01-149">`[RunName <String>]`: Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="92f01-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="92f01-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="92f01-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="92f01-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="92f01-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="92f01-152">`[UpdateLocation <String>]`: Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="92f01-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="92f01-153">`[UpdateName <String>]`: Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="92f01-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="92f01-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92f01-154">RELATED LINKS</span></span>

