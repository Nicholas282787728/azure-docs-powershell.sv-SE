---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093001"
---
# <span data-ttu-id="b5457-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b5457-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="b5457-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5457-102">SYNOPSIS</span></span>
<span data-ttu-id="b5457-103">Returnerar det begärda migreringsjobbet.</span><span class="sxs-lookup"><span data-stu-id="b5457-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b5457-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5457-104">SYNTAX</span></span>

### <span data-ttu-id="b5457-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b5457-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5457-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b5457-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5457-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5457-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5457-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5457-108">DESCRIPTION</span></span>
<span data-ttu-id="b5457-109">Returnerar det begärda migreringsjobbet.</span><span class="sxs-lookup"><span data-stu-id="b5457-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b5457-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5457-110">EXAMPLES</span></span>

### <span data-ttu-id="b5457-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="b5457-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="b5457-112">Returnerar en lista med hanterade diskallokering på platsen lokal.</span><span class="sxs-lookup"><span data-stu-id="b5457-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="b5457-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="b5457-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="b5457-114">Hämta ett specifikt jobb för hanterad migrering.</span><span class="sxs-lookup"><span data-stu-id="b5457-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="b5457-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5457-115">PARAMETERS</span></span>

### <span data-ttu-id="b5457-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5457-116">-DefaultProfile</span></span>
<span data-ttu-id="b5457-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5457-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5457-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5457-118">-InputObject</span></span>
<span data-ttu-id="b5457-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b5457-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5457-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="b5457-120">-Location</span></span>
<span data-ttu-id="b5457-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b5457-121">Location of the resource.</span></span>

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

### <span data-ttu-id="b5457-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5457-122">-Name</span></span>
<span data-ttu-id="b5457-123">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="b5457-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b5457-124">-Status</span><span class="sxs-lookup"><span data-stu-id="b5457-124">-Status</span></span>
<span data-ttu-id="b5457-125">Parametrarna för jobb status för diskallokering.</span><span class="sxs-lookup"><span data-stu-id="b5457-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b5457-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5457-126">-SubscriptionId</span></span>
<span data-ttu-id="b5457-127">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b5457-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5457-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b5457-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5457-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5457-129">CommonParameters</span></span>
<span data-ttu-id="b5457-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5457-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5457-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5457-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5457-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5457-132">INPUTS</span></span>

### <span data-ttu-id="b5457-133">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b5457-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="b5457-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5457-134">OUTPUTS</span></span>

### <span data-ttu-id="b5457-135">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b5457-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="b5457-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5457-136">NOTES</span></span>

<span data-ttu-id="b5457-137">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b5457-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5457-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5457-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b5457-139">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b5457-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5457-140">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="b5457-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="b5457-141">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b5457-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5457-142">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="b5457-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b5457-143">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="b5457-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="b5457-144">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="b5457-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b5457-145">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="b5457-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="b5457-146">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="b5457-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b5457-147">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="b5457-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="b5457-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b5457-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b5457-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b5457-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b5457-150">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="b5457-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="b5457-151">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="b5457-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="b5457-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5457-152">RELATED LINKS</span></span>

