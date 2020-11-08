---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261654"
---
# <span data-ttu-id="159f9-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="159f9-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="159f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="159f9-102">SYNOPSIS</span></span>
<span data-ttu-id="159f9-103">Åtgärd att ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="159f9-103">Operation to delete an App.</span></span>

## <span data-ttu-id="159f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="159f9-104">SYNTAX</span></span>

### <span data-ttu-id="159f9-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="159f9-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="159f9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="159f9-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="159f9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="159f9-107">DESCRIPTION</span></span>
<span data-ttu-id="159f9-108">Åtgärd att ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="159f9-108">Operation to delete an App.</span></span>

## <span data-ttu-id="159f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="159f9-109">EXAMPLES</span></span>

### <span data-ttu-id="159f9-110">Exempel 1: ta bort programmet våren med namn.</span><span class="sxs-lookup"><span data-stu-id="159f9-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="159f9-111">Ta bort vår moln app efter namn.</span><span class="sxs-lookup"><span data-stu-id="159f9-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="159f9-112">Exempel 2: ta bort programmet våren från en pipe.</span><span class="sxs-lookup"><span data-stu-id="159f9-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="159f9-113">Ta bort programmet våren från en pipe.</span><span class="sxs-lookup"><span data-stu-id="159f9-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="159f9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="159f9-114">PARAMETERS</span></span>

### <span data-ttu-id="159f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159f9-115">-DefaultProfile</span></span>
<span data-ttu-id="159f9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="159f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="159f9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="159f9-117">-InputObject</span></span>
<span data-ttu-id="159f9-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="159f9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="159f9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="159f9-119">-Name</span></span>
<span data-ttu-id="159f9-120">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-120">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159f9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="159f9-121">-PassThru</span></span>
<span data-ttu-id="159f9-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="159f9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="159f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="159f9-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="159f9-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="159f9-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159f9-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="159f9-126">-ServiceName</span></span>
<span data-ttu-id="159f9-127">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-127">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159f9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="159f9-128">-SubscriptionId</span></span>
<span data-ttu-id="159f9-129">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="159f9-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="159f9-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="159f9-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159f9-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="159f9-131">-Confirm</span></span>
<span data-ttu-id="159f9-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="159f9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="159f9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="159f9-133">-WhatIf</span></span>
<span data-ttu-id="159f9-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="159f9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="159f9-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="159f9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="159f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159f9-136">CommonParameters</span></span>
<span data-ttu-id="159f9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159f9-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="159f9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159f9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="159f9-139">INPUTS</span></span>

### <span data-ttu-id="159f9-140">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="159f9-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="159f9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="159f9-141">OUTPUTS</span></span>

### <span data-ttu-id="159f9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="159f9-142">System.Boolean</span></span>

## <span data-ttu-id="159f9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="159f9-143">NOTES</span></span>

<span data-ttu-id="159f9-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="159f9-144">ALIASES</span></span>

<span data-ttu-id="159f9-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="159f9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="159f9-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="159f9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="159f9-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="159f9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="159f9-148">INPUTOBJECT <ISpringCloudIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="159f9-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="159f9-149">`[AppName <String>]`: Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="159f9-150">`[BindingName <String>]`: Namnet på bindnings resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="159f9-151">`[CertificateName <String>]`: Namnet på certifikat resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="159f9-152">`[DeploymentName <String>]`: Namnet på distributions resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="159f9-153">`[DomainName <String>]`: Namnet på den anpassade domän resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="159f9-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="159f9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="159f9-155">`[Location <String>]`: regionen</span><span class="sxs-lookup"><span data-stu-id="159f9-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="159f9-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="159f9-157">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="159f9-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="159f9-158">`[ServiceName <String>]`: Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="159f9-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="159f9-159">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="159f9-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="159f9-160">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="159f9-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="159f9-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="159f9-161">RELATED LINKS</span></span>

