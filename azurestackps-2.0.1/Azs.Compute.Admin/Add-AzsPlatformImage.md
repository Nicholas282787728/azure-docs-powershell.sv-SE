---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093068"
---
# <span data-ttu-id="74583-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="74583-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="74583-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74583-102">SYNOPSIS</span></span>
<span data-ttu-id="74583-103">Skapar en ny plattforms bild med given utgivare, utbud, SKU: er och version.</span><span class="sxs-lookup"><span data-stu-id="74583-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="74583-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74583-104">SYNTAX</span></span>

### <span data-ttu-id="74583-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="74583-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74583-106">Göra</span><span class="sxs-lookup"><span data-stu-id="74583-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74583-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74583-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74583-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="74583-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74583-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74583-109">DESCRIPTION</span></span>
<span data-ttu-id="74583-110">Skapar en ny plattforms bild med given utgivare, utbud, SKU: er och version.</span><span class="sxs-lookup"><span data-stu-id="74583-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="74583-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74583-111">EXAMPLES</span></span>

### <span data-ttu-id="74583-112">Exempel 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="74583-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="74583-113">Lägga till en plattforms bild från Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="74583-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="74583-114">Använd en SasUri för att ange platsen för PlatformImage eller Använd en allmänt tillgänglig URL-adress.</span><span class="sxs-lookup"><span data-stu-id="74583-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="74583-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74583-115">PARAMETERS</span></span>

### <span data-ttu-id="74583-116">Undantag. meddelande</span><span class="sxs-lookup"><span data-stu-id="74583-116">Exception.Message</span></span>
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

### <span data-ttu-id="74583-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="74583-117">-BillingPartNumber</span></span>
<span data-ttu-id="74583-118">Artikel numret används för att debitera program varu kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="74583-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-119">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="74583-119">-DataDisks</span></span>
<span data-ttu-id="74583-120">Data diskar som används av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="74583-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="74583-121">För att konstruera kan du läsa avsnittet anteckningar för DATADISKS-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="74583-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74583-122">-DefaultProfile</span></span>
<span data-ttu-id="74583-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74583-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74583-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74583-124">-InputObject</span></span>
<span data-ttu-id="74583-125">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="74583-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="74583-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="74583-126">-Location</span></span>
<span data-ttu-id="74583-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="74583-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="74583-128">-NewImage</span></span>
<span data-ttu-id="74583-129">Parametrar som används för att skapa en ny plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="74583-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="74583-130">För att konstruera kan du läsa avsnittet anteckningar för NEWIMAGE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="74583-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="74583-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="74583-131">-NoWait</span></span>
<span data-ttu-id="74583-132">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="74583-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74583-133">-Ge</span><span class="sxs-lookup"><span data-stu-id="74583-133">-Offer</span></span>
<span data-ttu-id="74583-134">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="74583-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="74583-135">-OsType</span></span>
<span data-ttu-id="74583-136">Typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="74583-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="74583-137">-OsUri</span></span>
<span data-ttu-id="74583-138">Diskens plats.</span><span class="sxs-lookup"><span data-stu-id="74583-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="74583-139">-ProvisioningState</span></span>
<span data-ttu-id="74583-140">Konfigurations status för plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="74583-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="74583-141">-Publisher</span></span>
<span data-ttu-id="74583-142">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="74583-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="74583-143">-Sku</span></span>
<span data-ttu-id="74583-144">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="74583-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74583-145">-SubscriptionId</span></span>
<span data-ttu-id="74583-146">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="74583-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="74583-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="74583-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-148">-Version</span><span class="sxs-lookup"><span data-stu-id="74583-148">-Version</span></span>
<span data-ttu-id="74583-149">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="74583-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74583-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74583-150">-Confirm</span></span>
<span data-ttu-id="74583-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74583-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74583-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74583-152">-WhatIf</span></span>
<span data-ttu-id="74583-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74583-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74583-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74583-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="74583-155">Undantag. meddelande</span><span class="sxs-lookup"><span data-stu-id="74583-155">Exception.Message</span></span>

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

### <span data-ttu-id="74583-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74583-156">CommonParameters</span></span>
<span data-ttu-id="74583-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74583-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74583-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74583-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74583-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74583-159">INPUTS</span></span>

### <span data-ttu-id="74583-160">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="74583-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="74583-161">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="74583-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="74583-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74583-162">OUTPUTS</span></span>

### <span data-ttu-id="74583-163">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="74583-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="74583-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74583-164">NOTES</span></span>

<span data-ttu-id="74583-165">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="74583-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74583-166">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74583-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="74583-167">DATADISKS <IDataDisk [] >: data diskar som används av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="74583-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="74583-168">`[Lun <Int32?>]`: Logiskt enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="74583-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="74583-169">`[Uri <String>]`: Disk mallens plats.</span><span class="sxs-lookup"><span data-stu-id="74583-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="74583-170">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="74583-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74583-171">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="74583-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="74583-172">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="74583-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74583-173">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="74583-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="74583-174">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="74583-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="74583-175">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="74583-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="74583-176">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="74583-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="74583-177">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="74583-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="74583-178">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="74583-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="74583-179">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="74583-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="74583-180">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="74583-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="74583-181">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="74583-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="74583-182">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="74583-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="74583-183">NEWIMAGE <IPlatformImageParameters> : parametrar som används för att skapa en ny plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="74583-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="74583-184">`[DataDisk <IDataDisk[]>]`: Data diskar som används av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="74583-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="74583-185">`[Lun <Int32?>]`: Logiskt enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="74583-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="74583-186">`[Uri <String>]`: Disk mallens plats.</span><span class="sxs-lookup"><span data-stu-id="74583-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="74583-187">`[DetailBillingPartNumber <String>]`: Artikel numret används för att debitera program varu kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="74583-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="74583-188">`[OSDiskOstype <OSType?>]`: Operativ system typ.</span><span class="sxs-lookup"><span data-stu-id="74583-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="74583-189">`[OSDiskUri <String>]`: Diskens plats.</span><span class="sxs-lookup"><span data-stu-id="74583-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="74583-190">`[ProvisioningState <ProvisioningState?>]`: Konfigurations status för plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="74583-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="74583-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74583-191">RELATED LINKS</span></span>

