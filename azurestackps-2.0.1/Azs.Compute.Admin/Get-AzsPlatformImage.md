---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092996"
---
# <span data-ttu-id="5492a-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5492a-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="5492a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5492a-102">SYNOPSIS</span></span>
<span data-ttu-id="5492a-103">Returnerar den specifika plattforms bild som matchar utgivare, utbud, SKU: er och version.</span><span class="sxs-lookup"><span data-stu-id="5492a-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="5492a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5492a-104">SYNTAX</span></span>

### <span data-ttu-id="5492a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5492a-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5492a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5492a-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5492a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5492a-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5492a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5492a-108">DESCRIPTION</span></span>
<span data-ttu-id="5492a-109">Returnerar den specifika plattforms bild som matchar utgivare, utbud, SKU: er och version.</span><span class="sxs-lookup"><span data-stu-id="5492a-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="5492a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5492a-110">EXAMPLES</span></span>

### <span data-ttu-id="5492a-111">Exempel 1: Hämta alla plattforms bilder</span><span class="sxs-lookup"><span data-stu-id="5492a-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="5492a-112">Få en lista över alla plattforms bilder genom att lämna alla parametrar tomma.</span><span class="sxs-lookup"><span data-stu-id="5492a-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="5492a-113">Exempel 2: Hämta specifik plattforms bild</span><span class="sxs-lookup"><span data-stu-id="5492a-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="5492a-114">Ange ett utbud, Publisher, plats, SKU och version för att hämta en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="5492a-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="5492a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5492a-115">PARAMETERS</span></span>

### <span data-ttu-id="5492a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5492a-116">-DefaultProfile</span></span>
<span data-ttu-id="5492a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5492a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5492a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5492a-118">-InputObject</span></span>
<span data-ttu-id="5492a-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5492a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5492a-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="5492a-120">-Location</span></span>
<span data-ttu-id="5492a-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5492a-121">Location of the resource.</span></span>

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

### <span data-ttu-id="5492a-122">-Ge</span><span class="sxs-lookup"><span data-stu-id="5492a-122">-Offer</span></span>
<span data-ttu-id="5492a-123">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="5492a-123">Name of the offer.</span></span>

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

### <span data-ttu-id="5492a-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5492a-124">-Publisher</span></span>
<span data-ttu-id="5492a-125">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="5492a-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="5492a-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="5492a-126">-Sku</span></span>
<span data-ttu-id="5492a-127">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="5492a-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="5492a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5492a-128">-SubscriptionId</span></span>
<span data-ttu-id="5492a-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5492a-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5492a-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5492a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5492a-131">-Version</span><span class="sxs-lookup"><span data-stu-id="5492a-131">-Version</span></span>
<span data-ttu-id="5492a-132">Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="5492a-132">The version of the resource.</span></span>

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

### <span data-ttu-id="5492a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5492a-133">CommonParameters</span></span>
<span data-ttu-id="5492a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5492a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5492a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5492a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5492a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5492a-136">INPUTS</span></span>

### <span data-ttu-id="5492a-137">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5492a-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="5492a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5492a-138">OUTPUTS</span></span>

### <span data-ttu-id="5492a-139">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5492a-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="5492a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5492a-140">NOTES</span></span>

<span data-ttu-id="5492a-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5492a-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5492a-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5492a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5492a-143">INPUTOBJECT <IComputeAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5492a-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5492a-144">`[DiskId <String>]`: Diskens GUID som identitet.</span><span class="sxs-lookup"><span data-stu-id="5492a-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="5492a-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5492a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5492a-146">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="5492a-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5492a-147">`[MigrationId <String>]`: GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="5492a-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="5492a-148">`[Offer <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="5492a-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="5492a-149">`[Publisher <String>]`: Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="5492a-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="5492a-150">`[QuotaName <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="5492a-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5492a-151">`[Sku <String>]`: SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="5492a-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="5492a-152">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5492a-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5492a-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5492a-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5492a-154">`[Type <String>]`: Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="5492a-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="5492a-155">`[Version <String>]`: Den här versionen av resursen.</span><span class="sxs-lookup"><span data-stu-id="5492a-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="5492a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5492a-156">RELATED LINKS</span></span>

