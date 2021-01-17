---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419723"
---
# <span data-ttu-id="6a38e-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="6a38e-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="6a38e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a38e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a38e-103">Åtgärd för att uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="6a38e-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="6a38e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a38e-104">SYNTAX</span></span>

### <span data-ttu-id="6a38e-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6a38e-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a38e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a38e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a38e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a38e-107">DESCRIPTION</span></span>
<span data-ttu-id="6a38e-108">Åtgärd för att uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="6a38e-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="6a38e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a38e-109">EXAMPLES</span></span>

### <span data-ttu-id="6a38e-110">Exempel 1: uppdatera vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="6a38e-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="6a38e-111">Uppdatera vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="6a38e-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="6a38e-112">Exempel 2: uppdatera vår moln app från en pipe.</span><span class="sxs-lookup"><span data-stu-id="6a38e-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="6a38e-113">Uppdatera vår moln app från pipe.</span><span class="sxs-lookup"><span data-stu-id="6a38e-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="6a38e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a38e-114">PARAMETERS</span></span>

### <span data-ttu-id="6a38e-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="6a38e-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="6a38e-116">Namnet på den aktiva distributionen av programmet</span><span class="sxs-lookup"><span data-stu-id="6a38e-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="6a38e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a38e-117">-AsJob</span></span>
<span data-ttu-id="6a38e-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="6a38e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6a38e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a38e-119">-DefaultProfile</span></span>
<span data-ttu-id="6a38e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a38e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a38e-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="6a38e-121">-Fqdn</span></span>
<span data-ttu-id="6a38e-122">Fullständigt kvalificerat DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="6a38e-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="6a38e-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6a38e-123">-HttpsOnly</span></span>
<span data-ttu-id="6a38e-124">Ange om endast https tillåts.</span><span class="sxs-lookup"><span data-stu-id="6a38e-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="6a38e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a38e-125">-InputObject</span></span>
<span data-ttu-id="6a38e-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6a38e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a38e-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a38e-127">-Location</span></span>
<span data-ttu-id="6a38e-128">GEO-platsen för programmet, alltid samma som den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="6a38e-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="6a38e-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a38e-129">-Name</span></span>
<span data-ttu-id="6a38e-130">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a38e-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6a38e-131">-NoWait</span></span>
<span data-ttu-id="6a38e-132">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="6a38e-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a38e-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="6a38e-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="6a38e-134">Monterings vägen för den beständiga disken</span><span class="sxs-lookup"><span data-stu-id="6a38e-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="6a38e-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="6a38e-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="6a38e-136">Den beständiga diskens storlek i GB</span><span class="sxs-lookup"><span data-stu-id="6a38e-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="6a38e-137">-Offentlig</span><span class="sxs-lookup"><span data-stu-id="6a38e-137">-Public</span></span>
<span data-ttu-id="6a38e-138">Anger om programmet exponerar en offentlig slut punkt</span><span class="sxs-lookup"><span data-stu-id="6a38e-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="6a38e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a38e-139">-ResourceGroupName</span></span>
<span data-ttu-id="6a38e-140">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6a38e-141">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6a38e-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6a38e-142">-ServiceName</span></span>
<span data-ttu-id="6a38e-143">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6a38e-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a38e-144">-SubscriptionId</span></span>
<span data-ttu-id="6a38e-145">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a38e-146">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a38e-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a38e-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="6a38e-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="6a38e-148">Monterings vägen för den tillfälliga disken</span><span class="sxs-lookup"><span data-stu-id="6a38e-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="6a38e-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="6a38e-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="6a38e-150">Storleken på den tillfälliga disken i GB</span><span class="sxs-lookup"><span data-stu-id="6a38e-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="6a38e-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a38e-151">-Confirm</span></span>
<span data-ttu-id="6a38e-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a38e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a38e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a38e-153">-WhatIf</span></span>
<span data-ttu-id="6a38e-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a38e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a38e-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a38e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a38e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a38e-156">CommonParameters</span></span>
<span data-ttu-id="6a38e-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a38e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a38e-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a38e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a38e-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a38e-159">INPUTS</span></span>

### <span data-ttu-id="6a38e-160">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6a38e-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6a38e-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a38e-161">OUTPUTS</span></span>

### <span data-ttu-id="6a38e-162">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="6a38e-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="6a38e-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a38e-163">NOTES</span></span>

<span data-ttu-id="6a38e-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6a38e-164">ALIASES</span></span>

<span data-ttu-id="6a38e-165">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6a38e-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a38e-166">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6a38e-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a38e-167">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a38e-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a38e-168">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6a38e-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a38e-169">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6a38e-170">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6a38e-171">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6a38e-172">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6a38e-173">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6a38e-174">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6a38e-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a38e-175">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="6a38e-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6a38e-176">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6a38e-177">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6a38e-178">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6a38e-179">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6a38e-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6a38e-180">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a38e-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6a38e-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a38e-181">RELATED LINKS</span></span>

