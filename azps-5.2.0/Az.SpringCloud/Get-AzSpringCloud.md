---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395152"
---
# <span data-ttu-id="b895f-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="b895f-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="b895f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b895f-102">SYNOPSIS</span></span>
<span data-ttu-id="b895f-103">Skaffa en tjänst och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b895f-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="b895f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b895f-104">SYNTAX</span></span>

### <span data-ttu-id="b895f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b895f-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b895f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b895f-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b895f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b895f-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b895f-108">List1</span><span class="sxs-lookup"><span data-stu-id="b895f-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b895f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b895f-109">DESCRIPTION</span></span>
<span data-ttu-id="b895f-110">Skaffa en tjänst och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b895f-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="b895f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b895f-111">EXAMPLES</span></span>

### <span data-ttu-id="b895f-112">Exempel 1: skaffa vår moln tjänst efter namn</span><span class="sxs-lookup"><span data-stu-id="b895f-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="b895f-113">Skaffa vår moln tjänst med namn</span><span class="sxs-lookup"><span data-stu-id="b895f-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="b895f-114">Exempel 2: lista alla våren-moln tjänster under resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b895f-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="b895f-115">Lista alla våren-moln tjänster under resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b895f-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="b895f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b895f-116">PARAMETERS</span></span>

### <span data-ttu-id="b895f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b895f-117">-DefaultProfile</span></span>
<span data-ttu-id="b895f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b895f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b895f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b895f-119">-InputObject</span></span>
<span data-ttu-id="b895f-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b895f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b895f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b895f-121">-Name</span></span>
<span data-ttu-id="b895f-122">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b895f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b895f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b895f-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b895f-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b895f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b895f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b895f-126">-SubscriptionId</span></span>
<span data-ttu-id="b895f-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b895f-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b895f-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b895f-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b895f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b895f-129">CommonParameters</span></span>
<span data-ttu-id="b895f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b895f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b895f-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b895f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b895f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b895f-132">INPUTS</span></span>

### <span data-ttu-id="b895f-133">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b895f-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b895f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b895f-134">OUTPUTS</span></span>

### <span data-ttu-id="b895f-135">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="b895f-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="b895f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b895f-136">NOTES</span></span>

<span data-ttu-id="b895f-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b895f-137">ALIASES</span></span>

<span data-ttu-id="b895f-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b895f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b895f-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b895f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b895f-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b895f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b895f-141">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b895f-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b895f-142">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b895f-143">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b895f-144">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b895f-145">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b895f-146">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b895f-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b895f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b895f-148">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="b895f-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b895f-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b895f-150">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b895f-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b895f-151">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="b895f-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b895f-152">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b895f-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b895f-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b895f-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b895f-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b895f-154">RELATED LINKS</span></span>

