---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423763"
---
# <span data-ttu-id="d95bf-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="d95bf-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="d95bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d95bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d95bf-103">Skaffa en ExpressRoute-krets efter namn i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="d95bf-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="d95bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d95bf-104">SYNTAX</span></span>

### <span data-ttu-id="d95bf-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="d95bf-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d95bf-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d95bf-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d95bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d95bf-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d95bf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d95bf-108">DESCRIPTION</span></span>
<span data-ttu-id="d95bf-109">Skaffa en ExpressRoute-krets efter namn i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="d95bf-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="d95bf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d95bf-110">EXAMPLES</span></span>

### <span data-ttu-id="d95bf-111">Exempel 1: få ett godkännande</span><span class="sxs-lookup"><span data-stu-id="d95bf-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="d95bf-112">Denna cmdlet får tillstånd `azps-test-auth` under privata moln `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="d95bf-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="d95bf-113">Exempel 2: lista godkännande</span><span class="sxs-lookup"><span data-stu-id="d95bf-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="d95bf-114">Denna cmdlet visar auktorisering `azps-test-auth` under privat moln `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="d95bf-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="d95bf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d95bf-115">PARAMETERS</span></span>

### <span data-ttu-id="d95bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95bf-116">-DefaultProfile</span></span>
<span data-ttu-id="d95bf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d95bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d95bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d95bf-118">-InputObject</span></span>
<span data-ttu-id="d95bf-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d95bf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d95bf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d95bf-120">-Name</span></span>
<span data-ttu-id="d95bf-121">Namn på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95bf-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d95bf-122">-PrivateCloudName</span></span>
<span data-ttu-id="d95bf-123">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="d95bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="d95bf-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d95bf-125">The name of the resource group.</span></span>
<span data-ttu-id="d95bf-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d95bf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d95bf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d95bf-127">-SubscriptionId</span></span>
<span data-ttu-id="d95bf-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d95bf-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d95bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95bf-129">CommonParameters</span></span>
<span data-ttu-id="d95bf-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95bf-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d95bf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95bf-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d95bf-132">INPUTS</span></span>

### <span data-ttu-id="d95bf-133">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d95bf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d95bf-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d95bf-134">OUTPUTS</span></span>

### <span data-ttu-id="d95bf-135">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="d95bf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="d95bf-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d95bf-136">NOTES</span></span>

<span data-ttu-id="d95bf-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d95bf-137">ALIASES</span></span>

<span data-ttu-id="d95bf-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d95bf-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d95bf-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d95bf-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d95bf-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d95bf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d95bf-141">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d95bf-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d95bf-142">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d95bf-143">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d95bf-144">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d95bf-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d95bf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d95bf-146">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="d95bf-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d95bf-147">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="d95bf-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d95bf-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d95bf-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d95bf-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d95bf-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="d95bf-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d95bf-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d95bf-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d95bf-151">RELATED LINKS</span></span>

