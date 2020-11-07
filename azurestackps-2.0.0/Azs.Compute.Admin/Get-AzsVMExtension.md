---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925458"
---
# <span data-ttu-id="d5789-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d5789-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="d5789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5789-102">SYNOPSIS</span></span>
<span data-ttu-id="d5789-103">Returnerar den begärda virtuella dator tilläggs avbildningen som matchar Publisher, typ, version.</span><span class="sxs-lookup"><span data-stu-id="d5789-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="d5789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5789-104">SYNTAX</span></span>

### <span data-ttu-id="d5789-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="d5789-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5789-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d5789-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d5789-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5789-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d5789-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5789-108">DESCRIPTION</span></span>
<span data-ttu-id="d5789-109">Returnerar den begärda virtuella dator tilläggs avbildningen som matchar Publisher, typ, version.</span><span class="sxs-lookup"><span data-stu-id="d5789-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="d5789-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5789-110">EXAMPLES</span></span>

### <span data-ttu-id="d5789-111">Exempel 1: Hämta alla virtuella dator tillägg</span><span class="sxs-lookup"><span data-stu-id="d5789-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="d5789-112">Få en lista över alla VMExtensions genom att lämna alla parametrar tomma.</span><span class="sxs-lookup"><span data-stu-id="d5789-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="d5789-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5789-113">PARAMETERS</span></span>

### <span data-ttu-id="d5789-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5789-114">-DefaultProfile</span></span>
<span data-ttu-id="d5789-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5789-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5789-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5789-116">-InputObject</span></span>
<span data-ttu-id="d5789-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d5789-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5789-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="d5789-118">-Location</span></span>
<span data-ttu-id="d5789-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="d5789-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d5789-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d5789-120">-Publisher</span></span>
<span data-ttu-id="d5789-121">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="d5789-121">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5789-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5789-122">-SubscriptionId</span></span>
<span data-ttu-id="d5789-123">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d5789-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5789-124">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d5789-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5789-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d5789-125">-Type</span></span>
<span data-ttu-id="d5789-126">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="d5789-126">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5789-127">-Version</span><span class="sxs-lookup"><span data-stu-id="d5789-127">-Version</span></span>
<span data-ttu-id="d5789-128">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="d5789-128">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5789-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5789-129">CommonParameters</span></span>
<span data-ttu-id="d5789-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5789-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5789-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5789-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5789-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5789-132">INPUTS</span></span>

### <span data-ttu-id="d5789-133">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d5789-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="d5789-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5789-134">OUTPUTS</span></span>

### <span data-ttu-id="d5789-135">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="d5789-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="d5789-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5789-136">NOTES</span></span>

<span data-ttu-id="d5789-137">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d5789-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5789-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5789-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d5789-139">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d5789-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5789-140">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="d5789-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="d5789-141">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d5789-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5789-142">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="d5789-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d5789-143">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="d5789-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="d5789-144">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="d5789-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d5789-145">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="d5789-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="d5789-146">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="d5789-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d5789-147">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="d5789-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="d5789-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d5789-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d5789-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d5789-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d5789-150">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="d5789-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="d5789-151">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="d5789-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="d5789-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5789-152">RELATED LINKS</span></span>

