---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271671"
---
# <span data-ttu-id="4df96-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="4df96-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="4df96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4df96-102">SYNOPSIS</span></span>
<span data-ttu-id="4df96-103">Skaffa ett kluster med namn i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="4df96-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="4df96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4df96-104">SYNTAX</span></span>

### <span data-ttu-id="4df96-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4df96-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4df96-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4df96-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4df96-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4df96-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4df96-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4df96-108">DESCRIPTION</span></span>
<span data-ttu-id="4df96-109">Skaffa ett kluster med namn i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="4df96-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="4df96-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4df96-110">EXAMPLES</span></span>

### <span data-ttu-id="4df96-111">Exempel 1: skaffa kluster</span><span class="sxs-lookup"><span data-stu-id="4df96-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="4df96-112">Skaffa kluster</span><span class="sxs-lookup"><span data-stu-id="4df96-112">Get cluster</span></span>

### <span data-ttu-id="4df96-113">Exempel 2: lista kluster</span><span class="sxs-lookup"><span data-stu-id="4df96-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="4df96-114">Lista kluster</span><span class="sxs-lookup"><span data-stu-id="4df96-114">List clusters</span></span>

## <span data-ttu-id="4df96-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4df96-115">PARAMETERS</span></span>

### <span data-ttu-id="4df96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df96-116">-DefaultProfile</span></span>
<span data-ttu-id="4df96-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4df96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df96-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4df96-118">-InputObject</span></span>
<span data-ttu-id="4df96-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4df96-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4df96-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4df96-120">-Name</span></span>
<span data-ttu-id="4df96-121">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df96-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="4df96-122">-PrivateCloudName</span></span>
<span data-ttu-id="4df96-123">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="4df96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df96-124">-ResourceGroupName</span></span>
<span data-ttu-id="4df96-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4df96-125">The name of the resource group.</span></span>
<span data-ttu-id="4df96-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4df96-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4df96-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4df96-127">-SubscriptionId</span></span>
<span data-ttu-id="4df96-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4df96-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4df96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df96-129">CommonParameters</span></span>
<span data-ttu-id="4df96-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df96-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4df96-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df96-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4df96-132">INPUTS</span></span>

### <span data-ttu-id="4df96-133">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="4df96-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4df96-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4df96-134">OUTPUTS</span></span>

### <span data-ttu-id="4df96-135">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="4df96-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="4df96-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4df96-136">NOTES</span></span>

<span data-ttu-id="4df96-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4df96-137">ALIASES</span></span>

<span data-ttu-id="4df96-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4df96-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4df96-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4df96-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4df96-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4df96-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4df96-141">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4df96-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4df96-142">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4df96-143">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4df96-144">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4df96-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4df96-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4df96-146">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="4df96-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4df96-147">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4df96-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4df96-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4df96-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4df96-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4df96-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="4df96-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="4df96-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4df96-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4df96-151">RELATED LINKS</span></span>

