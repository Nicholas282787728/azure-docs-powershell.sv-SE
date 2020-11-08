---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093092"
---
# <span data-ttu-id="c6ecc-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="c6ecc-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="c6ecc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ecc-103">Tar bort den angivna tilläggs avbildningen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="c6ecc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6ecc-104">SYNTAX</span></span>

### <span data-ttu-id="c6ecc-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="c6ecc-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6ecc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6ecc-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6ecc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6ecc-107">DESCRIPTION</span></span>
<span data-ttu-id="c6ecc-108">Tar bort den angivna tilläggs avbildningen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="c6ecc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6ecc-109">EXAMPLES</span></span>

### <span data-ttu-id="c6ecc-110">Exempel 1: ta bort ett VM-tillägg som finns</span><span class="sxs-lookup"><span data-stu-id="c6ecc-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="c6ecc-111">Ett lyckat samtal för att ta bort en Beräknad kvot returnerar inte något resultat</span><span class="sxs-lookup"><span data-stu-id="c6ecc-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="c6ecc-112">Exempel 2: ta bort ett VM-tillägg som inte finns</span><span class="sxs-lookup"><span data-stu-id="c6ecc-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="c6ecc-113">Ett lyckat samtal för att ta bort en plattforms bild som inte existerar returnerar inte något resultat</span><span class="sxs-lookup"><span data-stu-id="c6ecc-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="c6ecc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="c6ecc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ecc-115">-DefaultProfile</span></span>
<span data-ttu-id="c6ecc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ecc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6ecc-117">-InputObject</span></span>
<span data-ttu-id="c6ecc-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="c6ecc-119">-Location</span></span>
<span data-ttu-id="c6ecc-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-120">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6ecc-121">-PassThru</span></span>
<span data-ttu-id="c6ecc-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="c6ecc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c6ecc-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c6ecc-123">-Publisher</span></span>
<span data-ttu-id="c6ecc-124">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6ecc-125">-SubscriptionId</span></span>
<span data-ttu-id="c6ecc-126">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6ecc-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c6ecc-128">-Type</span></span>
<span data-ttu-id="c6ecc-129">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-130">-Version</span><span class="sxs-lookup"><span data-stu-id="c6ecc-130">-Version</span></span>
<span data-ttu-id="c6ecc-131">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c6ecc-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6ecc-132">-Confirm</span></span>
<span data-ttu-id="c6ecc-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ecc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ecc-134">-WhatIf</span></span>
<span data-ttu-id="c6ecc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ecc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ecc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ecc-137">CommonParameters</span></span>
<span data-ttu-id="c6ecc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ecc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6ecc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ecc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6ecc-140">INPUTS</span></span>

### <span data-ttu-id="c6ecc-141">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c6ecc-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c6ecc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6ecc-142">OUTPUTS</span></span>

### <span data-ttu-id="c6ecc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6ecc-143">System.Boolean</span></span>



## <span data-ttu-id="c6ecc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6ecc-144">NOTES</span></span>

<span data-ttu-id="c6ecc-145">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6ecc-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c6ecc-147">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c6ecc-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6ecc-148">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c6ecc-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c6ecc-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6ecc-150">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c6ecc-151">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c6ecc-152">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c6ecc-153">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c6ecc-154">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c6ecc-155">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c6ecc-156">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c6ecc-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c6ecc-158">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c6ecc-159">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c6ecc-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6ecc-160">RELATED LINKS</span></span>

