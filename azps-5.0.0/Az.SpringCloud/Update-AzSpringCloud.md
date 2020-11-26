---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262947"
---
# <span data-ttu-id="935ce-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="935ce-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="935ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="935ce-102">SYNOPSIS</span></span>
<span data-ttu-id="935ce-103">Åtgärd för att uppdatera en utgångs tjänst.</span><span class="sxs-lookup"><span data-stu-id="935ce-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="935ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="935ce-104">SYNTAX</span></span>

### <span data-ttu-id="935ce-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="935ce-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="935ce-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="935ce-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="935ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="935ce-107">DESCRIPTION</span></span>
<span data-ttu-id="935ce-108">Åtgärd för att uppdatera en utgångs tjänst.</span><span class="sxs-lookup"><span data-stu-id="935ce-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="935ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="935ce-109">EXAMPLES</span></span>

### <span data-ttu-id="935ce-110">Exempel 1: uppdatera vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="935ce-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="935ce-111">Uppdatera vår moln tjänst efter namn.</span><span class="sxs-lookup"><span data-stu-id="935ce-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="935ce-112">Exempel 2: uppdatera vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="935ce-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="935ce-113">Uppdatera vår moln tjänst från en pipe.</span><span class="sxs-lookup"><span data-stu-id="935ce-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="935ce-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="935ce-114">PARAMETERS</span></span>

### <span data-ttu-id="935ce-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="935ce-115">-AsJob</span></span>
<span data-ttu-id="935ce-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="935ce-116">Run the command as a job</span></span>

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

### <span data-ttu-id="935ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935ce-117">-DefaultProfile</span></span>
<span data-ttu-id="935ce-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="935ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="935ce-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="935ce-119">-GitPropertyUri</span></span>
<span data-ttu-id="935ce-120">URI för databasen</span><span class="sxs-lookup"><span data-stu-id="935ce-120">URI of the repository</span></span>

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

### <span data-ttu-id="935ce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="935ce-121">-InputObject</span></span>
<span data-ttu-id="935ce-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="935ce-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="935ce-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="935ce-123">-Location</span></span>
<span data-ttu-id="935ce-124">GEO-platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="935ce-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="935ce-125">-Name</span></span>
<span data-ttu-id="935ce-126">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935ce-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="935ce-127">-NoWait</span></span>
<span data-ttu-id="935ce-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="935ce-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="935ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="935ce-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="935ce-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="935ce-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="935ce-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="935ce-132">-SkuName</span></span>
<span data-ttu-id="935ce-133">Namn på SKU</span><span class="sxs-lookup"><span data-stu-id="935ce-133">Name of the Sku</span></span>

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

### <span data-ttu-id="935ce-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="935ce-134">-SkuTier</span></span>
<span data-ttu-id="935ce-135">SKU</span><span class="sxs-lookup"><span data-stu-id="935ce-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="935ce-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="935ce-136">-SubscriptionId</span></span>
<span data-ttu-id="935ce-137">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="935ce-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="935ce-138">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="935ce-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="935ce-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="935ce-139">-Tag</span></span>
<span data-ttu-id="935ce-140">Taggar för tjänsten som är en lista över de värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935ce-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="935ce-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="935ce-142">Huvud instrument för mål program</span><span class="sxs-lookup"><span data-stu-id="935ce-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="935ce-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="935ce-143">-TraceEnabled</span></span>
<span data-ttu-id="935ce-144">Anger om spårningsfunktionen ska aktive ras</span><span class="sxs-lookup"><span data-stu-id="935ce-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="935ce-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="935ce-145">-Confirm</span></span>
<span data-ttu-id="935ce-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="935ce-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935ce-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935ce-147">-WhatIf</span></span>
<span data-ttu-id="935ce-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="935ce-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935ce-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="935ce-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935ce-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935ce-150">CommonParameters</span></span>
<span data-ttu-id="935ce-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935ce-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935ce-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935ce-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935ce-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="935ce-153">INPUTS</span></span>

### <span data-ttu-id="935ce-154">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="935ce-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="935ce-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="935ce-155">OUTPUTS</span></span>

### <span data-ttu-id="935ce-156">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="935ce-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="935ce-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="935ce-157">NOTES</span></span>

<span data-ttu-id="935ce-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="935ce-158">ALIASES</span></span>

<span data-ttu-id="935ce-159">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="935ce-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="935ce-160">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="935ce-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="935ce-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="935ce-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="935ce-162">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="935ce-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="935ce-163">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="935ce-164">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="935ce-165">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="935ce-166">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="935ce-167">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="935ce-168">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="935ce-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="935ce-169">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="935ce-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="935ce-170">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="935ce-171">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="935ce-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="935ce-172">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="935ce-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="935ce-173">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="935ce-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="935ce-174">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="935ce-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="935ce-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="935ce-175">RELATED LINKS</span></span>
