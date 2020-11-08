---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262963"
---
# <span data-ttu-id="96de6-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="96de6-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="96de6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96de6-102">SYNOPSIS</span></span>
<span data-ttu-id="96de6-103">Skapa en ny app eller uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="96de6-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="96de6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96de6-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96de6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96de6-105">DESCRIPTION</span></span>
<span data-ttu-id="96de6-106">Skapa en ny app eller uppdatera ett avslutat program.</span><span class="sxs-lookup"><span data-stu-id="96de6-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="96de6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96de6-107">EXAMPLES</span></span>

### <span data-ttu-id="96de6-108">Exempel 1: skapa ett fjäder moln program.</span><span class="sxs-lookup"><span data-stu-id="96de6-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="96de6-109">Skapa ett program för vår moln.</span><span class="sxs-lookup"><span data-stu-id="96de6-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="96de6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96de6-110">PARAMETERS</span></span>

### <span data-ttu-id="96de6-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="96de6-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="96de6-112">Namnet på den aktiva distributionen av programmet</span><span class="sxs-lookup"><span data-stu-id="96de6-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="96de6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96de6-113">-AsJob</span></span>
<span data-ttu-id="96de6-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="96de6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="96de6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96de6-115">-DefaultProfile</span></span>
<span data-ttu-id="96de6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96de6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96de6-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="96de6-117">-Fqdn</span></span>
<span data-ttu-id="96de6-118">Fullständigt kvalificerat DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="96de6-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="96de6-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="96de6-119">-HttpsOnly</span></span>
<span data-ttu-id="96de6-120">Ange om endast https tillåts.</span><span class="sxs-lookup"><span data-stu-id="96de6-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="96de6-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="96de6-121">-Location</span></span>
<span data-ttu-id="96de6-122">GEO-platsen för programmet, alltid samma som den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="96de6-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="96de6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="96de6-123">-Name</span></span>
<span data-ttu-id="96de6-124">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="96de6-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96de6-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="96de6-125">-NoWait</span></span>
<span data-ttu-id="96de6-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="96de6-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96de6-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="96de6-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="96de6-128">Monterings vägen för den beständiga disken</span><span class="sxs-lookup"><span data-stu-id="96de6-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="96de6-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="96de6-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="96de6-130">Den beständiga diskens storlek i GB</span><span class="sxs-lookup"><span data-stu-id="96de6-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="96de6-131">-Offentlig</span><span class="sxs-lookup"><span data-stu-id="96de6-131">-Public</span></span>
<span data-ttu-id="96de6-132">Anger om programmet exponerar en offentlig slut punkt</span><span class="sxs-lookup"><span data-stu-id="96de6-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="96de6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96de6-133">-ResourceGroupName</span></span>
<span data-ttu-id="96de6-134">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="96de6-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="96de6-135">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="96de6-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="96de6-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="96de6-136">-ServiceName</span></span>
<span data-ttu-id="96de6-137">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="96de6-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="96de6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96de6-138">-SubscriptionId</span></span>
<span data-ttu-id="96de6-139">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="96de6-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96de6-140">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="96de6-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96de6-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="96de6-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="96de6-142">Monterings vägen för den tillfälliga disken</span><span class="sxs-lookup"><span data-stu-id="96de6-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="96de6-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="96de6-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="96de6-144">Storleken på den tillfälliga disken i GB</span><span class="sxs-lookup"><span data-stu-id="96de6-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="96de6-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96de6-145">-Confirm</span></span>
<span data-ttu-id="96de6-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96de6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96de6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96de6-147">-WhatIf</span></span>
<span data-ttu-id="96de6-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96de6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96de6-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96de6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96de6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96de6-150">CommonParameters</span></span>
<span data-ttu-id="96de6-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96de6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96de6-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96de6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96de6-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96de6-153">INPUTS</span></span>

## <span data-ttu-id="96de6-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96de6-154">OUTPUTS</span></span>

### <span data-ttu-id="96de6-155">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="96de6-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="96de6-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96de6-156">NOTES</span></span>

<span data-ttu-id="96de6-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="96de6-157">ALIASES</span></span>

## <span data-ttu-id="96de6-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96de6-158">RELATED LINKS</span></span>

