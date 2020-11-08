---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 1e5af469f92c07f7223ba95715bd32b22b4eb66f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261671"
---
# <span data-ttu-id="7c6e6-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="7c6e6-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="7c6e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6e6-103">Hämta en app och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-103">Get an App and its properties.</span></span>

## <span data-ttu-id="7c6e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c6e6-104">SYNTAX</span></span>

### <span data-ttu-id="7c6e6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7c6e6-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c6e6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7c6e6-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c6e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c6e6-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c6e6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c6e6-108">DESCRIPTION</span></span>
<span data-ttu-id="7c6e6-109">Hämta en app och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-109">Get an App and its properties.</span></span>

## <span data-ttu-id="7c6e6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c6e6-110">EXAMPLES</span></span>

### <span data-ttu-id="7c6e6-111">Exempel 1: Hämta vår moln app via namn.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="7c6e6-112">Skaffa vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="7c6e6-113">Exempel 2: Visa alla program under en viss fjäder moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="7c6e6-114">Visa alla program under en viss fjäder moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="7c6e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c6e6-115">PARAMETERS</span></span>

### <span data-ttu-id="7c6e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6e6-116">-DefaultProfile</span></span>
<span data-ttu-id="7c6e6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c6e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c6e6-118">-InputObject</span></span>
<span data-ttu-id="7c6e6-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7c6e6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c6e6-120">-Name</span></span>
<span data-ttu-id="7c6e6-121">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c6e6-123">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7c6e6-124">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e6-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c6e6-125">-ServiceName</span></span>
<span data-ttu-id="7c6e6-126">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c6e6-127">-SubscriptionId</span></span>
<span data-ttu-id="7c6e6-128">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c6e6-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e6-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="7c6e6-130">-SyncStatus</span></span>
<span data-ttu-id="7c6e6-131">Anger om synkroniseringsstatus</span><span class="sxs-lookup"><span data-stu-id="7c6e6-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6e6-132">CommonParameters</span></span>
<span data-ttu-id="7c6e6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6e6-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c6e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6e6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c6e6-135">INPUTS</span></span>

### <span data-ttu-id="7c6e6-136">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7c6e6-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7c6e6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c6e6-137">OUTPUTS</span></span>

### <span data-ttu-id="7c6e6-138">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="7c6e6-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="7c6e6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c6e6-139">NOTES</span></span>

<span data-ttu-id="7c6e6-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7c6e6-140">ALIASES</span></span>

<span data-ttu-id="7c6e6-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7c6e6-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c6e6-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c6e6-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c6e6-144">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7c6e6-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c6e6-145">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7c6e6-146">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7c6e6-147">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7c6e6-148">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7c6e6-149">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7c6e6-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7c6e6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c6e6-151">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="7c6e6-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7c6e6-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7c6e6-153">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7c6e6-154">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7c6e6-155">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7c6e6-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7c6e6-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7c6e6-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c6e6-157">RELATED LINKS</span></span>

