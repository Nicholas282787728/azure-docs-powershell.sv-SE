---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319495"
---
# <span data-ttu-id="4b0cf-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4b0cf-101">New-AzImportExport</span></span>

## <span data-ttu-id="4b0cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0cf-103">Skapar ett nytt jobb eller uppdaterar ett befintligt jobb i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4b0cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b0cf-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4b0cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="4b0cf-106">Skapar ett nytt jobb eller uppdaterar ett befintligt jobb i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4b0cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b0cf-107">EXAMPLES</span></span>

### <span data-ttu-id="4b0cf-108">Exempel 1: skapa ett nytt ImportExport-jobb</span><span class="sxs-lookup"><span data-stu-id="4b0cf-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="4b0cf-109">Dessa cmdletar skapar ett nytt ImportExport-jobb.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="4b0cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b0cf-110">PARAMETERS</span></span>

### <span data-ttu-id="4b0cf-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4b0cf-111">-AcceptLanguage</span></span>
<span data-ttu-id="4b0cf-112">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4b0cf-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="4b0cf-113">-BackupDriveManifest</span></span>
<span data-ttu-id="4b0cf-114">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-114">Default value is false.</span></span>
<span data-ttu-id="4b0cf-115">Anger om manifest filerna på enheterna ska kopieras för att blockera blob.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="4b0cf-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="4b0cf-116">-BlobListBlobPath</span></span>
<span data-ttu-id="4b0cf-117">En samling med BLOB-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="4b0cf-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="4b0cf-119">En uppsättning BLOB-adressprefix.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="4b0cf-120">-CancelRequested</span></span>
<span data-ttu-id="4b0cf-121">Anger om en begäran har skickats för att avbryta jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="4b0cf-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="4b0cf-122">-ClientTenantId</span></span>
<span data-ttu-id="4b0cf-123">Klient organisationens ID för klienten som gör begäran.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="4b0cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0cf-124">-DefaultProfile</span></span>
<span data-ttu-id="4b0cf-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b0cf-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="4b0cf-127">Namnet på den operatör som används för att leverera import-eller export enheterna.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="4b0cf-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4b0cf-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="4b0cf-129">Antalet enheter som ingår i paketet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="4b0cf-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4b0cf-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="4b0cf-131">Det datum då paketet levereras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="4b0cf-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4b0cf-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="4b0cf-133">Paketets spårnings nummer.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="4b0cf-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="4b0cf-134">-DiagnosticsPath</span></span>
<span data-ttu-id="4b0cf-135">Den virtuella BLOB-katalogen där kopierings loggar och säkerhets kopior av enhets MANIFEST filer (om de är aktiverade) lagras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="4b0cf-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="4b0cf-136">-DriveList</span></span>
<span data-ttu-id="4b0cf-137">Lista över upp till tio enheter som utgör jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="4b0cf-138">Enhets listan är ett obligatoriskt element för ett import jobb. den är inte angiven för export jobb.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="4b0cf-139">För att konstruera kan du läsa avsnittet anteckningar för DRIVELIST-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b0cf-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="4b0cf-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="4b0cf-141">Den relativa URI: n till den Block-Blob som innehåller listan över BLOB-sökvägar eller BLOB-sökprefix enligt definitionen ovan, med början med behållar namnet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="4b0cf-142">Om blobben finns i rot behållaren måste URI: n börja med $root.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="4b0cf-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="4b0cf-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="4b0cf-144">En BLOB-sökväg som pekar på en Block-Blob som innehåller en lista över BLOB-namn som inte har exporter ATS på grund av otillräckligt disk utrymme.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="4b0cf-145">Om alla blobbar har exporter ATS är det här elementet inte inkluderat i svaret.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="4b0cf-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="4b0cf-146">-JobType</span></span>
<span data-ttu-id="4b0cf-147">Typ av jobb</span><span class="sxs-lookup"><span data-stu-id="4b0cf-147">The type of job</span></span>

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

### <span data-ttu-id="4b0cf-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="4b0cf-148">-Location</span></span>
<span data-ttu-id="4b0cf-149">Anger den Azure-plats som stöds där jobbet ska skapas</span><span class="sxs-lookup"><span data-stu-id="4b0cf-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="4b0cf-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4b0cf-150">-LogLevel</span></span>
<span data-ttu-id="4b0cf-151">Standardvärdet är fel.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-151">Default value is Error.</span></span>
<span data-ttu-id="4b0cf-152">Anger om fel loggning eller utförlig loggning ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="4b0cf-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b0cf-153">-Name</span></span>
<span data-ttu-id="4b0cf-154">Namnet på import-och export jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-155">-Procent färdigt</span><span class="sxs-lookup"><span data-stu-id="4b0cf-155">-PercentComplete</span></span>
<span data-ttu-id="4b0cf-156">Total procent färdigt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="4b0cf-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="4b0cf-157">-ProvisioningState</span></span>
<span data-ttu-id="4b0cf-158">Anger jobbets etablerings status.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="4b0cf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-159">-ResourceGroupName</span></span>
<span data-ttu-id="4b0cf-160">Resurs gruppens namn identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="4b0cf-161">-ReturnAddressCity</span></span>
<span data-ttu-id="4b0cf-162">Orts namn som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4b0cf-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="4b0cf-164">Det land eller den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="4b0cf-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="4b0cf-166">E-postadress för mottagaren av de enheter som returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4b0cf-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="4b0cf-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="4b0cf-168">Telefonnummer till mottagaren av de enheter som returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4b0cf-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="4b0cf-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="4b0cf-170">Post numret som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="4b0cf-172">Namnet på mottagaren som kommer att få hård diskarna när de returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="4b0cf-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4b0cf-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="4b0cf-174">Den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4b0cf-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="4b0cf-176">Den första raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4b0cf-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="4b0cf-178">Den andra raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="4b0cf-180">Namnet på den operatör som används för att leverera import-eller export enheterna.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="4b0cf-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4b0cf-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="4b0cf-182">Antalet enheter som ingår i paketet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="4b0cf-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4b0cf-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="4b0cf-184">Det datum då paketet levereras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="4b0cf-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4b0cf-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="4b0cf-186">Paketets spårnings nummer.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="4b0cf-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="4b0cf-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="4b0cf-188">Kundens konto nummer med operatören.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="4b0cf-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="4b0cf-190">Operatörens namn.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-190">The carrier's name.</span></span>

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

### <span data-ttu-id="4b0cf-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="4b0cf-191">-ShippingInformationCity</span></span>
<span data-ttu-id="4b0cf-192">Orts namn som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4b0cf-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="4b0cf-194">Det land eller den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="4b0cf-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="4b0cf-196">Telefonnummer till mottagaren av de enheter som returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4b0cf-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="4b0cf-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="4b0cf-198">Post numret som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="4b0cf-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="4b0cf-200">Namnet på mottagaren som kommer att få hård diskarna när de returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="4b0cf-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4b0cf-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="4b0cf-202">Den region som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4b0cf-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="4b0cf-204">Den första raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4b0cf-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="4b0cf-206">Den andra raden i gatuadressen som ska användas när enheterna returneras.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4b0cf-207">-State</span><span class="sxs-lookup"><span data-stu-id="4b0cf-207">-State</span></span>
<span data-ttu-id="4b0cf-208">Aktuellt tillstånd för jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-208">Current state of the job.</span></span>

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

### <span data-ttu-id="4b0cf-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b0cf-209">-StorageAccountId</span></span>
<span data-ttu-id="4b0cf-210">Resurs-ID för det lagrings konto som data ska importeras till eller exporteras från.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="4b0cf-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b0cf-211">-SubscriptionId</span></span>
<span data-ttu-id="4b0cf-212">Abonnemangs-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-213">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4b0cf-213">-Tag</span></span>
<span data-ttu-id="4b0cf-214">Anger de taggar som ska kopplas till jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0cf-215">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b0cf-215">-Confirm</span></span>
<span data-ttu-id="4b0cf-216">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b0cf-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0cf-217">-WhatIf</span></span>
<span data-ttu-id="4b0cf-218">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b0cf-219">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b0cf-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0cf-220">CommonParameters</span></span>
<span data-ttu-id="4b0cf-221">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0cf-222">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b0cf-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0cf-223">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b0cf-223">INPUTS</span></span>

## <span data-ttu-id="4b0cf-224">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b0cf-224">OUTPUTS</span></span>

### <span data-ttu-id="4b0cf-225">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="4b0cf-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="4b0cf-226">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b0cf-226">NOTES</span></span>

<span data-ttu-id="4b0cf-227">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4b0cf-227">ALIASES</span></span>

<span data-ttu-id="4b0cf-228">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4b0cf-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b0cf-229">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b0cf-230">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b0cf-231">DRIVELIST <IDriveStatus [] >: lista med upp till tio enheter som utgör jobbet.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="4b0cf-232">Enhets listan är ett obligatoriskt element för ett import jobb. den är inte angiven för export jobb.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="4b0cf-233">`[BitLockerKey <String>]`: Den BitLocker-nyckel som används för att kryptera enheten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="4b0cf-234">`[BytesSucceeded <Int64?>]`: Byte har överförts för enheten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="4b0cf-235">`[CopyStatus <String>]`: Detaljerad status om data överförings processen.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="4b0cf-236">Det här fältet returneras inte i svaret förrän enheten är i överförings läget.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="4b0cf-237">`[DriveHeaderHash <String>]`: Värdet på enhetens huvud.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="4b0cf-238">`[DriveId <String>]`: Enhetens maskin varu serie nummer utan blank steg.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="4b0cf-239">`[ErrorLogUri <String>]`: En URI som pekar på blobben som innehåller fel loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="4b0cf-240">`[ManifestFile <String>]`: Den relativa sökvägen för manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="4b0cf-241">`[ManifestHash <String>]`: Den Base16iska MD5-hashen för manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="4b0cf-242">`[ManifestUri <String>]`: En URI som pekar på blobben som innehåller enhetens manifest fil.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="4b0cf-243">`[PercentComplete <Int32?>]`: Procent färdigt för enheten.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="4b0cf-244">`[State <DriveState?>]`: Enhetens aktuella status.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="4b0cf-245">`[VerboseLogUri <String>]`: En URI som pekar på blobben som innehåller utförlig loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="4b0cf-246">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b0cf-246">RELATED LINKS</span></span>
