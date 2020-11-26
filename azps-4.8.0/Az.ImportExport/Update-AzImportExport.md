---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259939"
---
# <span data-ttu-id="cd65e-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="cd65e-101">Update-AzImportExport</span></span>

## <span data-ttu-id="cd65e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd65e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd65e-103">Uppdaterar specifika egenskaper för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="cd65e-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="cd65e-104">Du kan ringa den här åtgärden för att meddela import-och export tjänsten att hård diskarna som innehåller import-eller export jobbet har levererats till Microsoft Data Center.</span><span class="sxs-lookup"><span data-stu-id="cd65e-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="cd65e-105">Den kan också användas för att avbryta ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="cd65e-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="cd65e-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd65e-106">SYNTAX</span></span>

### <span data-ttu-id="cd65e-107">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="cd65e-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd65e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd65e-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd65e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd65e-109">DESCRIPTION</span></span>
<span data-ttu-id="cd65e-110">Uppdaterar specifika egenskaper för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="cd65e-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="cd65e-111">Du kan ringa den här åtgärden för att meddela import-och export tjänsten att hård diskarna som innehåller import-eller export jobbet har levererats till Microsoft Data Center.</span><span class="sxs-lookup"><span data-stu-id="cd65e-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="cd65e-112">Den kan också användas för att avbryta ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="cd65e-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="cd65e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd65e-113">EXAMPLES</span></span>

### <span data-ttu-id="cd65e-114">Exempel 1: uppdatera ImportExport-jobbet efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="cd65e-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="cd65e-115">Denna cmdlet uppdaterar ImportExport-jobbet efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="cd65e-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="cd65e-116">Exempel 2: uppdatera ImportExport-jobbet efter identitet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="cd65e-117">Denna cmdlet uppdaterar ImportExport-jobbet efter identitet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="cd65e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd65e-118">PARAMETERS</span></span>

### <span data-ttu-id="cd65e-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cd65e-119">-AcceptLanguage</span></span>
<span data-ttu-id="cd65e-120">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="cd65e-120">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="cd65e-121">-BackupDriveManifest</span></span>
<span data-ttu-id="cd65e-122">Anger om manifest filerna på enheterna ska kopieras för att blockera blob.</span><span class="sxs-lookup"><span data-stu-id="cd65e-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="cd65e-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="cd65e-123">-CancelRequested</span></span>
<span data-ttu-id="cd65e-124">Om det anges måste värdet vara sant.</span><span class="sxs-lookup"><span data-stu-id="cd65e-124">If specified, the value must be true.</span></span>
<span data-ttu-id="cd65e-125">Tjänsten försöker avbryta jobbet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="cd65e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd65e-126">-DefaultProfile</span></span>
<span data-ttu-id="cd65e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd65e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd65e-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="cd65e-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="cd65e-129">Namnet på den operatör som används för att leverera import-eller export enheterna.</span><span class="sxs-lookup"><span data-stu-id="cd65e-129">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="cd65e-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="cd65e-131">Antalet enheter som ingår i paketet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-131">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="cd65e-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="cd65e-133">Det datum då paketet levereras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-133">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="cd65e-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="cd65e-135">Paketets spårnings nummer.</span><span class="sxs-lookup"><span data-stu-id="cd65e-135">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="cd65e-136">-DriveList</span></span>
<span data-ttu-id="cd65e-137">Lista över enheter som utgör jobbet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="cd65e-138">För att konstruera kan du läsa avsnittet anteckningar för DRIVELIST-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cd65e-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd65e-139">-InputObject</span></span>
<span data-ttu-id="cd65e-140">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cd65e-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="cd65e-141">-LogLevel</span></span>
<span data-ttu-id="cd65e-142">Anger om fel loggning eller utförlig loggning är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="cd65e-142">Indicates whether error logging or verbose logging is enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd65e-143">-Name</span></span>
<span data-ttu-id="cd65e-144">Namnet på import-och export jobbet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd65e-145">-ResourceGroupName</span></span>
<span data-ttu-id="cd65e-146">Resurs gruppens namn identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cd65e-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="cd65e-147">-ReturnAddressCity</span></span>
<span data-ttu-id="cd65e-148">Orts namn som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-148">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="cd65e-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="cd65e-150">Det land eller den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-150">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="cd65e-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="cd65e-152">E-postadress för mottagaren av de enheter som returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-152">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="cd65e-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="cd65e-154">Telefonnummer till mottagaren av de enheter som returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-154">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="cd65e-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="cd65e-156">Post numret som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-156">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="cd65e-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="cd65e-158">Namnet på mottagaren som kommer att få hård diskarna när de returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="cd65e-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="cd65e-160">Den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-160">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="cd65e-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="cd65e-162">Den första raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-162">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="cd65e-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="cd65e-164">Den andra raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="cd65e-164">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="cd65e-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="cd65e-166">Kundens konto nummer med operatören.</span><span class="sxs-lookup"><span data-stu-id="cd65e-166">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="cd65e-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="cd65e-168">Operatörens namn.</span><span class="sxs-lookup"><span data-stu-id="cd65e-168">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-169">-State</span><span class="sxs-lookup"><span data-stu-id="cd65e-169">-State</span></span>
<span data-ttu-id="cd65e-170">Om det här alternativet anges måste värdet levereras, vilket anger import-och export tjänsten som paketet för jobbet har levererats.</span><span class="sxs-lookup"><span data-stu-id="cd65e-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="cd65e-171">Egenskaperna ReturnAddress och DeliveryPackage måste ha angetts antingen i denna begäran eller i en tidigare begäran, annars Miss lyckas begäran.</span><span class="sxs-lookup"><span data-stu-id="cd65e-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd65e-172">-SubscriptionId</span></span>
<span data-ttu-id="cd65e-173">Abonnemangs-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="cd65e-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-174">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cd65e-174">-Tag</span></span>
<span data-ttu-id="cd65e-175">Anger de taggar som ska kopplas till jobbet</span><span class="sxs-lookup"><span data-stu-id="cd65e-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd65e-176">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd65e-176">-Confirm</span></span>
<span data-ttu-id="cd65e-177">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd65e-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd65e-178">-WhatIf</span></span>
<span data-ttu-id="cd65e-179">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd65e-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd65e-180">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd65e-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd65e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd65e-181">CommonParameters</span></span>
<span data-ttu-id="cd65e-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd65e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd65e-183">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd65e-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd65e-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd65e-184">INPUTS</span></span>

### <span data-ttu-id="cd65e-185">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="cd65e-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="cd65e-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd65e-186">OUTPUTS</span></span>

### <span data-ttu-id="cd65e-187">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="cd65e-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="cd65e-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd65e-188">NOTES</span></span>

<span data-ttu-id="cd65e-189">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd65e-189">ALIASES</span></span>

<span data-ttu-id="cd65e-190">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cd65e-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd65e-191">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cd65e-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd65e-192">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd65e-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd65e-193">DRIVELIST <IDriveStatus [] >: lista med enheter som utgör jobbet.</span><span class="sxs-lookup"><span data-stu-id="cd65e-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="cd65e-194">`[BitLockerKey <String>]`: Den BitLocker-nyckel som används för att kryptera enheten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="cd65e-195">`[BytesSucceeded <Int64?>]`: Byte har överförts för enheten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="cd65e-196">`[CopyStatus <String>]`: Detaljerad status om data överförings processen.</span><span class="sxs-lookup"><span data-stu-id="cd65e-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="cd65e-197">Det här fältet returneras inte i svaret förrän enheten är i överförings läget.</span><span class="sxs-lookup"><span data-stu-id="cd65e-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="cd65e-198">`[DriveHeaderHash <String>]`: Värdet på enhetens huvud.</span><span class="sxs-lookup"><span data-stu-id="cd65e-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="cd65e-199">`[DriveId <String>]`: Enhetens maskin varu serie nummer utan blank steg.</span><span class="sxs-lookup"><span data-stu-id="cd65e-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="cd65e-200">`[ErrorLogUri <String>]`: En URI som pekar på blobben som innehåller fel loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cd65e-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="cd65e-201">`[ManifestFile <String>]`: Den relativa sökvägen för manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="cd65e-202">`[ManifestHash <String>]`: Den Base16iska MD5-hashen för manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="cd65e-203">`[ManifestUri <String>]`: En URI som pekar på blobben som innehåller enhetens manifest fil.</span><span class="sxs-lookup"><span data-stu-id="cd65e-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="cd65e-204">`[PercentComplete <Int32?>]`: Procent färdigt för enheten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="cd65e-205">`[State <DriveState?>]`: Enhetens aktuella status.</span><span class="sxs-lookup"><span data-stu-id="cd65e-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="cd65e-206">`[VerboseLogUri <String>]`: En URI som pekar på blobben som innehåller utförlig loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cd65e-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="cd65e-207">INPUTOBJECT <IImportExportIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="cd65e-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd65e-208">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cd65e-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd65e-209">`[JobName <String>]`: Import-och export jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="cd65e-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="cd65e-210">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="cd65e-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="cd65e-211">Till exempel West, USA eller västkusten.</span><span class="sxs-lookup"><span data-stu-id="cd65e-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="cd65e-212">`[ResourceGroupName <String>]`: Resurs grupp namnet identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cd65e-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="cd65e-213">`[SubscriptionId <String>]`: Prenumerations-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="cd65e-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="cd65e-214">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd65e-214">RELATED LINKS</span></span>
