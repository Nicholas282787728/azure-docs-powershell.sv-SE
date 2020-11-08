---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099957"
---
# <span data-ttu-id="2c256-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2c256-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="2c256-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c256-102">SYNOPSIS</span></span>
<span data-ttu-id="2c256-103">Ta bort en plattforms bild</span><span class="sxs-lookup"><span data-stu-id="2c256-103">Delete a platform image</span></span>

## <span data-ttu-id="2c256-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c256-104">SYNTAX</span></span>

### <span data-ttu-id="2c256-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="2c256-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2c256-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c256-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c256-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c256-107">DESCRIPTION</span></span>
<span data-ttu-id="2c256-108">Ta bort en plattforms bild</span><span class="sxs-lookup"><span data-stu-id="2c256-108">Delete a platform image</span></span>

## <span data-ttu-id="2c256-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c256-109">EXAMPLES</span></span>

### <span data-ttu-id="2c256-110">Exempel 1: ta bort en plattforms bild</span><span class="sxs-lookup"><span data-stu-id="2c256-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="2c256-111">Ett lyckat samtal för att ta bort en plattforms bild returnerar inte något resultat</span><span class="sxs-lookup"><span data-stu-id="2c256-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="2c256-112">Exempel 2: ta bort en plattforms bild som inte finns</span><span class="sxs-lookup"><span data-stu-id="2c256-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="2c256-113">Ett lyckat samtal för att ta bort en plattforms bild som inte existerar returnerar inte något resultat</span><span class="sxs-lookup"><span data-stu-id="2c256-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="2c256-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c256-114">PARAMETERS</span></span>

### <span data-ttu-id="2c256-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c256-115">-DefaultProfile</span></span>
<span data-ttu-id="2c256-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c256-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c256-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c256-117">-InputObject</span></span>
<span data-ttu-id="2c256-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2c256-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2c256-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="2c256-119">-Location</span></span>
<span data-ttu-id="2c256-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="2c256-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2c256-121">-Ge</span><span class="sxs-lookup"><span data-stu-id="2c256-121">-Offer</span></span>
<span data-ttu-id="2c256-122">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="2c256-122">Name of the offer.</span></span>

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

### <span data-ttu-id="2c256-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c256-123">-PassThru</span></span>
<span data-ttu-id="2c256-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="2c256-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2c256-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2c256-125">-Publisher</span></span>
<span data-ttu-id="2c256-126">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="2c256-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="2c256-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="2c256-127">-Sku</span></span>
<span data-ttu-id="2c256-128">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="2c256-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="2c256-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c256-129">-SubscriptionId</span></span>
<span data-ttu-id="2c256-130">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c256-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c256-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2c256-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2c256-132">-Version</span><span class="sxs-lookup"><span data-stu-id="2c256-132">-Version</span></span>
<span data-ttu-id="2c256-133">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="2c256-133">The version of the resource.</span></span>

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

### <span data-ttu-id="2c256-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c256-134">-Confirm</span></span>
<span data-ttu-id="2c256-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c256-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c256-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c256-136">-WhatIf</span></span>
<span data-ttu-id="2c256-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c256-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c256-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c256-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c256-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c256-139">CommonParameters</span></span>
<span data-ttu-id="2c256-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c256-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c256-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c256-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c256-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c256-142">INPUTS</span></span>

### <span data-ttu-id="2c256-143">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2c256-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="2c256-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c256-144">OUTPUTS</span></span>

### <span data-ttu-id="2c256-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c256-145">System.Boolean</span></span>



## <span data-ttu-id="2c256-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c256-146">NOTES</span></span>

<span data-ttu-id="2c256-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2c256-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c256-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c256-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2c256-149">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="2c256-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c256-150">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="2c256-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="2c256-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="2c256-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c256-152">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="2c256-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2c256-153">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="2c256-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="2c256-154">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="2c256-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="2c256-155">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="2c256-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="2c256-156">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="2c256-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2c256-157">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="2c256-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="2c256-158">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c256-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2c256-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2c256-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2c256-160">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="2c256-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="2c256-161">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="2c256-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="2c256-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c256-162">RELATED LINKS</span></span>
