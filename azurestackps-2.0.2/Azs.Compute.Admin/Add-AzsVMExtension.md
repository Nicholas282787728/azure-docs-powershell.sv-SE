---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100159"
---
# <span data-ttu-id="43d85-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="43d85-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="43d85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43d85-102">SYNOPSIS</span></span>
<span data-ttu-id="43d85-103">Skapa en tilläggs bild för virtuell dator med Publisher och version.</span><span class="sxs-lookup"><span data-stu-id="43d85-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="43d85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43d85-104">SYNTAX</span></span>

### <span data-ttu-id="43d85-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="43d85-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="43d85-106">Göra</span><span class="sxs-lookup"><span data-stu-id="43d85-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="43d85-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43d85-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43d85-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43d85-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43d85-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43d85-109">DESCRIPTION</span></span>
<span data-ttu-id="43d85-110">Skapa en tilläggs bild för virtuell dator med Publisher och version.</span><span class="sxs-lookup"><span data-stu-id="43d85-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="43d85-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43d85-111">EXAMPLES</span></span>

### <span data-ttu-id="43d85-112">Exempel 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="43d85-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="43d85-113">Använd en allmänt tillgänglig länk för att ange platsen för tillägget, eller URI till en Azure Blob med SasUri.</span><span class="sxs-lookup"><span data-stu-id="43d85-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="43d85-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43d85-114">PARAMETERS</span></span>

### <span data-ttu-id="43d85-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="43d85-115">-ComputeRole</span></span>
<span data-ttu-id="43d85-116">Beräknings roll</span><span class="sxs-lookup"><span data-stu-id="43d85-116">Compute role</span></span>

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

### <span data-ttu-id="43d85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d85-117">-DefaultProfile</span></span>
<span data-ttu-id="43d85-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43d85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d85-119">-Anknytning</span><span class="sxs-lookup"><span data-stu-id="43d85-119">-Extension</span></span>
<span data-ttu-id="43d85-120">Parametrar som används för att skapa en ny tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="43d85-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="43d85-121">Om du vill skapa läser du avsnittet anteckningar för tilläggs egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="43d85-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d85-122">-InputObject</span></span>
<span data-ttu-id="43d85-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="43d85-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d85-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="43d85-124">-IsSystemExtension</span></span>
<span data-ttu-id="43d85-125">Anger om fil namns tillägget är för systemet.</span><span class="sxs-lookup"><span data-stu-id="43d85-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="43d85-126">-Location</span></span>
<span data-ttu-id="43d85-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="43d85-127">Location of the resource.</span></span>

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

### <span data-ttu-id="43d85-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="43d85-128">-PropertiesPublisher</span></span>
<span data-ttu-id="43d85-129">Utgivaren av VM-tillägget</span><span class="sxs-lookup"><span data-stu-id="43d85-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="43d85-130">-ProvisioningState</span></span>
<span data-ttu-id="43d85-131">Etablerings status för tillägget.</span><span class="sxs-lookup"><span data-stu-id="43d85-131">Provisioning state of extension.</span></span>

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

### <span data-ttu-id="43d85-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="43d85-132">-Publisher</span></span>
<span data-ttu-id="43d85-133">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="43d85-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="43d85-134">-SourceBlob</span></span>
<span data-ttu-id="43d85-135">URI till Azure eller AzureStack blob.</span><span class="sxs-lookup"><span data-stu-id="43d85-135">URI to Azure or AzureStack blob.</span></span>

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

### <span data-ttu-id="43d85-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43d85-136">-SubscriptionId</span></span>
<span data-ttu-id="43d85-137">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="43d85-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43d85-138">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="43d85-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43d85-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="43d85-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="43d85-140">True om det har stöd för flera tillägg.</span><span class="sxs-lookup"><span data-stu-id="43d85-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-141">– Skriv</span><span class="sxs-lookup"><span data-stu-id="43d85-141">-Type</span></span>
<span data-ttu-id="43d85-142">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="43d85-142">Type of extension.</span></span>

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

### <span data-ttu-id="43d85-143">-Version</span><span class="sxs-lookup"><span data-stu-id="43d85-143">-Version</span></span>
<span data-ttu-id="43d85-144">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="43d85-144">The version of the resource.</span></span>

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

### <span data-ttu-id="43d85-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="43d85-145">-VmOsType</span></span>
<span data-ttu-id="43d85-146">Typ av operativ system för virtuell dator som behövs för att distribuera tilläggs hanteraren.</span><span class="sxs-lookup"><span data-stu-id="43d85-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="43d85-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="43d85-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="43d85-148">Värde som anger om tillägget är aktiverat för stöd för virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="43d85-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43d85-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43d85-149">-Confirm</span></span>
<span data-ttu-id="43d85-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43d85-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d85-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d85-151">-WhatIf</span></span>
<span data-ttu-id="43d85-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43d85-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d85-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43d85-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d85-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d85-154">CommonParameters</span></span>
<span data-ttu-id="43d85-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d85-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d85-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43d85-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d85-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43d85-157">INPUTS</span></span>

### <span data-ttu-id="43d85-158">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="43d85-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="43d85-159">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="43d85-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="43d85-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43d85-160">OUTPUTS</span></span>

### <span data-ttu-id="43d85-161">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="43d85-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="43d85-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43d85-162">NOTES</span></span>

<span data-ttu-id="43d85-163">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="43d85-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d85-164">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43d85-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="43d85-165">TILLÄGG <IVMExtensionParameters> : parametrar som används för att skapa en ny virtuell dator tilläggs bild.</span><span class="sxs-lookup"><span data-stu-id="43d85-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="43d85-166">`[ComputeRole <String>]`: Compute Role</span><span class="sxs-lookup"><span data-stu-id="43d85-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="43d85-167">`[IsSystemExtension <Boolean?>]`: Anger om fil namns tillägget är för systemet.</span><span class="sxs-lookup"><span data-stu-id="43d85-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="43d85-168">`[ProvisioningState <ProvisioningState?>]`: Etablerings tillståndet för tillägget.</span><span class="sxs-lookup"><span data-stu-id="43d85-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="43d85-169">`[Publisher <String>]`: Utgivaren av VM-tillägget</span><span class="sxs-lookup"><span data-stu-id="43d85-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="43d85-170">`[SourceBlobUri <String>]`: URI till Azure eller AzureStack blob.</span><span class="sxs-lookup"><span data-stu-id="43d85-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="43d85-171">`[SupportMultipleExtension <Boolean?>]`: Sant om stöder flera tillägg.</span><span class="sxs-lookup"><span data-stu-id="43d85-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="43d85-172">`[VMScaleSetEnabled <Boolean?>]`: Värde som anger om tillägget är aktiverat för stöd för virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="43d85-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="43d85-173">`[VmosType <OSType?>]`: Operativ system typ för mål virtuell dator som behövs för att distribuera tilläggs hanteraren.</span><span class="sxs-lookup"><span data-stu-id="43d85-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="43d85-174">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="43d85-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d85-175">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="43d85-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="43d85-176">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="43d85-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d85-177">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="43d85-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="43d85-178">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="43d85-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="43d85-179">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="43d85-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="43d85-180">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="43d85-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="43d85-181">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="43d85-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="43d85-182">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="43d85-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="43d85-183">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="43d85-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43d85-184">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="43d85-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="43d85-185">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="43d85-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="43d85-186">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="43d85-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="43d85-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43d85-187">RELATED LINKS</span></span>

