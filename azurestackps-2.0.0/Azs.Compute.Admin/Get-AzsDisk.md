---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925469"
---
# <span data-ttu-id="e2505-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="e2505-101">Get-AzsDisk</span></span>

## <span data-ttu-id="e2505-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2505-102">SYNOPSIS</span></span>
<span data-ttu-id="e2505-103">Returnerar disketten.</span><span class="sxs-lookup"><span data-stu-id="e2505-103">Returns the disk.</span></span>

## <span data-ttu-id="e2505-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2505-104">SYNTAX</span></span>

### <span data-ttu-id="e2505-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e2505-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2505-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e2505-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2505-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2505-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e2505-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2505-108">DESCRIPTION</span></span>
<span data-ttu-id="e2505-109">Returnerar disketten.</span><span class="sxs-lookup"><span data-stu-id="e2505-109">Returns the disk.</span></span>

## <span data-ttu-id="e2505-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2505-110">EXAMPLES</span></span>

### <span data-ttu-id="e2505-111">Exempel 1: Hämta alla diskar</span><span class="sxs-lookup"><span data-stu-id="e2505-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="e2505-112">Utan parametrar visas `Get-AzsDisk` alla diskar.</span><span class="sxs-lookup"><span data-stu-id="e2505-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="e2505-113">Exempel 2: Hämta en diskett med namn</span><span class="sxs-lookup"><span data-stu-id="e2505-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="e2505-114">Ange en disk genom `Name` att hämta den.</span><span class="sxs-lookup"><span data-stu-id="e2505-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="e2505-115">Exempel 3: Hämta ett angivet antal diskar</span><span class="sxs-lookup"><span data-stu-id="e2505-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="e2505-116">Använd `Count` parametern för att hämta ett specifikt antal diskar.</span><span class="sxs-lookup"><span data-stu-id="e2505-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="e2505-117">Exempel 4: Hämta alla diskar på en viss plats</span><span class="sxs-lookup"><span data-stu-id="e2505-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="e2505-118">Använd `ScaleUnit` parametern eller `VolumeLabel` för att lista alla diskar på en viss plats</span><span class="sxs-lookup"><span data-stu-id="e2505-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="e2505-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2505-119">PARAMETERS</span></span>

### <span data-ttu-id="e2505-120">-Antal</span><span class="sxs-lookup"><span data-stu-id="e2505-120">-Count</span></span>
<span data-ttu-id="e2505-121">Det högsta antalet diskar som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="e2505-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2505-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2505-122">-DefaultProfile</span></span>
<span data-ttu-id="e2505-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2505-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2505-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2505-124">-InputObject</span></span>
<span data-ttu-id="e2505-125">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e2505-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2505-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="e2505-126">-Location</span></span>
<span data-ttu-id="e2505-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e2505-127">Location of the resource.</span></span>

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

### <span data-ttu-id="e2505-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2505-128">-Name</span></span>
<span data-ttu-id="e2505-129">GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="e2505-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2505-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e2505-130">-ScaleUnit</span></span>
<span data-ttu-id="e2505-131">Den enhet som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2505-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="e2505-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="e2505-132">-SharePath</span></span>
<span data-ttu-id="e2505-133">Resursen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2505-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="e2505-134">-Start</span><span class="sxs-lookup"><span data-stu-id="e2505-134">-Start</span></span>
<span data-ttu-id="e2505-135">Start indexet för diskar i Query.</span><span class="sxs-lookup"><span data-stu-id="e2505-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2505-136">-Status</span><span class="sxs-lookup"><span data-stu-id="e2505-136">-Status</span></span>
<span data-ttu-id="e2505-137">Parametrar för disk status.</span><span class="sxs-lookup"><span data-stu-id="e2505-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="e2505-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2505-138">-SubscriptionId</span></span>
<span data-ttu-id="e2505-139">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e2505-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2505-140">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e2505-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2505-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2505-141">-UserSubscriptionId</span></span>
<span data-ttu-id="e2505-142">ID för användar abonnemang som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2505-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="e2505-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="e2505-143">-VolumeLabel</span></span>
<span data-ttu-id="e2505-144">Volym etiketten för den volym som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2505-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="e2505-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2505-145">CommonParameters</span></span>
<span data-ttu-id="e2505-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2505-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2505-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2505-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2505-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2505-148">INPUTS</span></span>

### <span data-ttu-id="e2505-149">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e2505-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="e2505-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2505-150">OUTPUTS</span></span>

### <span data-ttu-id="e2505-151">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="e2505-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="e2505-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2505-152">NOTES</span></span>

<span data-ttu-id="e2505-153">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e2505-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2505-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2505-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e2505-155">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e2505-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2505-156">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="e2505-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="e2505-157">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e2505-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2505-158">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="e2505-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e2505-159">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="e2505-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="e2505-160">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="e2505-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e2505-161">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="e2505-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="e2505-162">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="e2505-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e2505-163">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="e2505-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="e2505-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e2505-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2505-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e2505-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e2505-166">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="e2505-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="e2505-167">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="e2505-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="e2505-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2505-168">RELATED LINKS</span></span>

