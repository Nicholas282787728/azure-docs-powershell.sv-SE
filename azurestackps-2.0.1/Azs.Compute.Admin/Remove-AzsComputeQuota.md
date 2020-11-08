---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093094"
---
# <span data-ttu-id="60f79-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="60f79-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="60f79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60f79-102">SYNOPSIS</span></span>
<span data-ttu-id="60f79-103">Ta bort en befintlig Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="60f79-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="60f79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60f79-104">SYNTAX</span></span>

### <span data-ttu-id="60f79-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="60f79-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60f79-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60f79-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60f79-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60f79-107">DESCRIPTION</span></span>
<span data-ttu-id="60f79-108">Ta bort en befintlig Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="60f79-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="60f79-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60f79-109">EXAMPLES</span></span>

### <span data-ttu-id="60f79-110">Exempel 1: ta bort en beräknings kvot</span><span class="sxs-lookup"><span data-stu-id="60f79-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="60f79-111">Ett lyckat samtal för att ta bort en Beräknad kvot returnerar inte något resultat</span><span class="sxs-lookup"><span data-stu-id="60f79-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="60f79-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60f79-112">PARAMETERS</span></span>

### <span data-ttu-id="60f79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f79-113">-DefaultProfile</span></span>
<span data-ttu-id="60f79-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60f79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f79-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f79-115">-InputObject</span></span>
<span data-ttu-id="60f79-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="60f79-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60f79-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="60f79-117">-Location</span></span>
<span data-ttu-id="60f79-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="60f79-118">Location of the resource.</span></span>

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

### <span data-ttu-id="60f79-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="60f79-119">-Name</span></span>
<span data-ttu-id="60f79-120">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="60f79-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="60f79-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60f79-121">-PassThru</span></span>
<span data-ttu-id="60f79-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="60f79-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="60f79-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60f79-123">-SubscriptionId</span></span>
<span data-ttu-id="60f79-124">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="60f79-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60f79-125">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="60f79-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60f79-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60f79-126">-Confirm</span></span>
<span data-ttu-id="60f79-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60f79-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f79-128">-WhatIf</span></span>
<span data-ttu-id="60f79-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60f79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f79-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60f79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f79-131">CommonParameters</span></span>
<span data-ttu-id="60f79-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f79-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f79-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f79-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60f79-134">INPUTS</span></span>

### <span data-ttu-id="60f79-135">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="60f79-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="60f79-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60f79-136">OUTPUTS</span></span>

### <span data-ttu-id="60f79-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60f79-137">System.Boolean</span></span>



## <span data-ttu-id="60f79-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60f79-138">NOTES</span></span>

<span data-ttu-id="60f79-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="60f79-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60f79-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60f79-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="60f79-141">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="60f79-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60f79-142">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="60f79-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="60f79-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="60f79-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60f79-144">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="60f79-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="60f79-145">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="60f79-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="60f79-146">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="60f79-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="60f79-147">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="60f79-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="60f79-148">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="60f79-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="60f79-149">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="60f79-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="60f79-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="60f79-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="60f79-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="60f79-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="60f79-152">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="60f79-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="60f79-153">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="60f79-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="60f79-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60f79-154">RELATED LINKS</span></span>

