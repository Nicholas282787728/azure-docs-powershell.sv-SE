---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: e4d7d502d96245291fce001f4706ae44f21f5fed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261013"
---
# <span data-ttu-id="8f170-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="8f170-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="8f170-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f170-102">SYNOPSIS</span></span>
<span data-ttu-id="8f170-103">Åtgärd för att uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="8f170-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="8f170-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f170-104">SYNTAX</span></span>

### <span data-ttu-id="8f170-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="8f170-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f170-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f170-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f170-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f170-107">DESCRIPTION</span></span>
<span data-ttu-id="8f170-108">Åtgärd för att uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="8f170-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="8f170-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f170-109">EXAMPLES</span></span>

### <span data-ttu-id="8f170-110">Exempel 1: uppdatera vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="8f170-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="8f170-111">Uppdatera vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="8f170-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="8f170-112">Exempel 2: uppdatera vår moln app från en pipe.</span><span class="sxs-lookup"><span data-stu-id="8f170-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="8f170-113">Uppdatera vår moln app från pipe.</span><span class="sxs-lookup"><span data-stu-id="8f170-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="8f170-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f170-114">PARAMETERS</span></span>

### <span data-ttu-id="8f170-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="8f170-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="8f170-116">Namnet på den aktiva distributionen av programmet</span><span class="sxs-lookup"><span data-stu-id="8f170-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="8f170-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f170-117">-AsJob</span></span>
<span data-ttu-id="8f170-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="8f170-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8f170-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f170-119">-DefaultProfile</span></span>
<span data-ttu-id="8f170-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f170-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f170-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="8f170-121">-Fqdn</span></span>
<span data-ttu-id="8f170-122">Fullständigt kvalificerat DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="8f170-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="8f170-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8f170-123">-HttpsOnly</span></span>
<span data-ttu-id="8f170-124">Ange om endast https tillåts.</span><span class="sxs-lookup"><span data-stu-id="8f170-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="8f170-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f170-125">-InputObject</span></span>
<span data-ttu-id="8f170-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8f170-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f170-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="8f170-127">-Location</span></span>
<span data-ttu-id="8f170-128">GEO-platsen för programmet, alltid samma som den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="8f170-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="8f170-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f170-129">-Name</span></span>
<span data-ttu-id="8f170-130">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="8f170-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8f170-131">-NoWait</span></span>
<span data-ttu-id="8f170-132">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="8f170-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f170-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="8f170-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="8f170-134">Monterings vägen för den beständiga disken</span><span class="sxs-lookup"><span data-stu-id="8f170-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="8f170-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="8f170-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="8f170-136">Den beständiga diskens storlek i GB</span><span class="sxs-lookup"><span data-stu-id="8f170-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="8f170-137">-Offentlig</span><span class="sxs-lookup"><span data-stu-id="8f170-137">-Public</span></span>
<span data-ttu-id="8f170-138">Anger om programmet exponerar en offentlig slut punkt</span><span class="sxs-lookup"><span data-stu-id="8f170-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="8f170-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f170-139">-ResourceGroupName</span></span>
<span data-ttu-id="8f170-140">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8f170-141">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8f170-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8f170-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f170-142">-ServiceName</span></span>
<span data-ttu-id="8f170-143">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8f170-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f170-144">-SubscriptionId</span></span>
<span data-ttu-id="8f170-145">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8f170-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f170-146">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8f170-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8f170-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="8f170-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="8f170-148">Monterings vägen för den tillfälliga disken</span><span class="sxs-lookup"><span data-stu-id="8f170-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="8f170-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="8f170-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="8f170-150">Storleken på den tillfälliga disken i GB</span><span class="sxs-lookup"><span data-stu-id="8f170-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="8f170-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f170-151">-Confirm</span></span>
<span data-ttu-id="8f170-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f170-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f170-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f170-153">-WhatIf</span></span>
<span data-ttu-id="8f170-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f170-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f170-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f170-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f170-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f170-156">CommonParameters</span></span>
<span data-ttu-id="8f170-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f170-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f170-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f170-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f170-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f170-159">INPUTS</span></span>

### <span data-ttu-id="8f170-160">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8f170-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8f170-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f170-161">OUTPUTS</span></span>

### <span data-ttu-id="8f170-162">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="8f170-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="8f170-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f170-163">NOTES</span></span>

<span data-ttu-id="8f170-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8f170-164">ALIASES</span></span>

<span data-ttu-id="8f170-165">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8f170-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f170-166">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8f170-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f170-167">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f170-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f170-168">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8f170-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f170-169">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8f170-170">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8f170-171">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8f170-172">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8f170-173">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8f170-174">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8f170-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f170-175">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="8f170-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8f170-176">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8f170-177">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8f170-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8f170-178">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="8f170-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8f170-179">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8f170-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8f170-180">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8f170-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f170-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f170-181">RELATED LINKS</span></span>
