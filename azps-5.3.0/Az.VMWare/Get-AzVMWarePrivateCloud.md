---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423752"
---
# <span data-ttu-id="92f5d-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="92f5d-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="92f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="92f5d-103">Skaffa ett privat moln</span><span class="sxs-lookup"><span data-stu-id="92f5d-103">Get a private cloud</span></span>

## <span data-ttu-id="92f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92f5d-104">SYNTAX</span></span>

### <span data-ttu-id="92f5d-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="92f5d-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92f5d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="92f5d-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92f5d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92f5d-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92f5d-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="92f5d-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="92f5d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92f5d-109">DESCRIPTION</span></span>
<span data-ttu-id="92f5d-110">Skaffa ett privat moln</span><span class="sxs-lookup"><span data-stu-id="92f5d-110">Get a private cloud</span></span>

## <span data-ttu-id="92f5d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92f5d-111">EXAMPLES</span></span>

### <span data-ttu-id="92f5d-112">Exempel 1: lista privata moln under abonnemang</span><span class="sxs-lookup"><span data-stu-id="92f5d-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="92f5d-113">Lista privata moln under prenumeration</span><span class="sxs-lookup"><span data-stu-id="92f5d-113">List private cloud under subscription</span></span>

### <span data-ttu-id="92f5d-114">Exempel 2: lista privata moln under resurs grupp</span><span class="sxs-lookup"><span data-stu-id="92f5d-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="92f5d-115">Lista privat moln under resurs grupp</span><span class="sxs-lookup"><span data-stu-id="92f5d-115">List private cloud under resource group</span></span>

### <span data-ttu-id="92f5d-116">Exempel 3: skaffa privat moln</span><span class="sxs-lookup"><span data-stu-id="92f5d-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="92f5d-117">Skaffa privat moln</span><span class="sxs-lookup"><span data-stu-id="92f5d-117">Get private cloud</span></span>

## <span data-ttu-id="92f5d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92f5d-118">PARAMETERS</span></span>

### <span data-ttu-id="92f5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f5d-119">-DefaultProfile</span></span>
<span data-ttu-id="92f5d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92f5d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f5d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f5d-121">-InputObject</span></span>
<span data-ttu-id="92f5d-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="92f5d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92f5d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="92f5d-123">-Name</span></span>
<span data-ttu-id="92f5d-124">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="92f5d-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="92f5d-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="92f5d-126">The name of the resource group.</span></span>
<span data-ttu-id="92f5d-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="92f5d-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="92f5d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92f5d-128">-SubscriptionId</span></span>
<span data-ttu-id="92f5d-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="92f5d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="92f5d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f5d-130">CommonParameters</span></span>
<span data-ttu-id="92f5d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f5d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f5d-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f5d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f5d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92f5d-133">INPUTS</span></span>

### <span data-ttu-id="92f5d-134">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="92f5d-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="92f5d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92f5d-135">OUTPUTS</span></span>

### <span data-ttu-id="92f5d-136">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="92f5d-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="92f5d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92f5d-137">NOTES</span></span>

<span data-ttu-id="92f5d-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="92f5d-138">ALIASES</span></span>

<span data-ttu-id="92f5d-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="92f5d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92f5d-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="92f5d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92f5d-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92f5d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92f5d-142">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="92f5d-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92f5d-143">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="92f5d-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="92f5d-144">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="92f5d-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="92f5d-145">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="92f5d-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="92f5d-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="92f5d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92f5d-147">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="92f5d-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="92f5d-148">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="92f5d-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="92f5d-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="92f5d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92f5d-150">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="92f5d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="92f5d-151">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="92f5d-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="92f5d-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92f5d-152">RELATED LINKS</span></span>

