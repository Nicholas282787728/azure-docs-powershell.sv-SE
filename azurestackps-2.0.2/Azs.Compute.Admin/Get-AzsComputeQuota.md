---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099921"
---
# <span data-ttu-id="3e0f5-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3e0f5-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="3e0f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0f5-103">Skaffa en befintlig Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="3e0f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e0f5-104">SYNTAX</span></span>

### <span data-ttu-id="3e0f5-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="3e0f5-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e0f5-106">Lära</span><span class="sxs-lookup"><span data-stu-id="3e0f5-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e0f5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e0f5-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e0f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e0f5-108">DESCRIPTION</span></span>
<span data-ttu-id="3e0f5-109">Skaffa en befintlig Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="3e0f5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e0f5-110">EXAMPLES</span></span>

### <span data-ttu-id="3e0f5-111">Exempel 1: Hämta alla beräknings kvoter</span><span class="sxs-lookup"><span data-stu-id="3e0f5-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="3e0f5-112">Kör `Get-AzsComputeQuota` utan parametrar för att få en lista över alla beräknings kvoter.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="3e0f5-113">Exempel 2: beräkna kvot efter namn</span><span class="sxs-lookup"><span data-stu-id="3e0f5-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="3e0f5-114">Ange kvotens namn på kommando raden för att hämta en specifik kvot.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="3e0f5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e0f5-115">PARAMETERS</span></span>

### <span data-ttu-id="3e0f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0f5-116">-DefaultProfile</span></span>
<span data-ttu-id="3e0f5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e0f5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e0f5-118">-InputObject</span></span>
<span data-ttu-id="3e0f5-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e0f5-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e0f5-120">-Location</span></span>
<span data-ttu-id="3e0f5-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e0f5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e0f5-122">-Name</span></span>
<span data-ttu-id="3e0f5-123">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e0f5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e0f5-124">-SubscriptionId</span></span>
<span data-ttu-id="3e0f5-125">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e0f5-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e0f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0f5-127">CommonParameters</span></span>
<span data-ttu-id="3e0f5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0f5-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e0f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0f5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e0f5-130">INPUTS</span></span>

### <span data-ttu-id="3e0f5-131">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3e0f5-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3e0f5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e0f5-132">OUTPUTS</span></span>

### <span data-ttu-id="3e0f5-133">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="3e0f5-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="3e0f5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e0f5-134">NOTES</span></span>

<span data-ttu-id="3e0f5-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e0f5-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e0f5-137">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3e0f5-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e0f5-138">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3e0f5-139">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3e0f5-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e0f5-140">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3e0f5-141">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3e0f5-142">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3e0f5-143">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3e0f5-144">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3e0f5-145">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3e0f5-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e0f5-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e0f5-148">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3e0f5-149">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="3e0f5-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3e0f5-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e0f5-150">RELATED LINKS</span></span>

