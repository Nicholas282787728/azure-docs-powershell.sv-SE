---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092915"
---
# <span data-ttu-id="5d517-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5d517-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="5d517-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d517-102">SYNOPSIS</span></span>
<span data-ttu-id="5d517-103">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="5d517-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="5d517-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d517-104">SYNTAX</span></span>

### <span data-ttu-id="5d517-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="5d517-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d517-106">Göra</span><span class="sxs-lookup"><span data-stu-id="5d517-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d517-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d517-107">DESCRIPTION</span></span>
<span data-ttu-id="5d517-108">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="5d517-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="5d517-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d517-109">EXAMPLES</span></span>

### <span data-ttu-id="5d517-110">Exempel 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5d517-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="5d517-111">Laddar upp TestUbuntu. test. 1.0.0 i galleriet.</span><span class="sxs-lookup"><span data-stu-id="5d517-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="5d517-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d517-112">PARAMETERS</span></span>

### <span data-ttu-id="5d517-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d517-113">-DefaultProfile</span></span>
<span data-ttu-id="5d517-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d517-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d517-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="5d517-115">-GalleryItemUri</span></span>
<span data-ttu-id="5d517-116">URI för ditt Galleri paket som redan har laddats upp online.</span><span class="sxs-lookup"><span data-stu-id="5d517-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d517-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="5d517-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="5d517-118">Plats för nytto last för Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="5d517-118">Location of gallery item payload.</span></span>
<span data-ttu-id="5d517-119">För att konstruera kan du läsa avsnittet anteckningar för GALLERYITEMURIPAYLOAD-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5d517-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5d517-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d517-120">-SubscriptionId</span></span>
<span data-ttu-id="5d517-121">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5d517-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d517-122">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5d517-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d517-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d517-123">-Confirm</span></span>
<span data-ttu-id="5d517-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d517-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d517-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d517-125">-WhatIf</span></span>
<span data-ttu-id="5d517-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d517-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d517-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d517-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d517-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d517-128">CommonParameters</span></span>
<span data-ttu-id="5d517-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d517-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d517-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d517-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d517-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d517-131">INPUTS</span></span>

### <span data-ttu-id="5d517-132">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="5d517-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="5d517-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d517-133">OUTPUTS</span></span>

### <span data-ttu-id="5d517-134">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5d517-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="5d517-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d517-135">NOTES</span></span>

<span data-ttu-id="5d517-136">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5d517-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d517-137">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d517-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5d517-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : plats för nytto last för Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="5d517-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="5d517-139">`[GalleryItemUri <String>]`: URI för ditt Galleri paket som redan har laddats upp online.</span><span class="sxs-lookup"><span data-stu-id="5d517-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="5d517-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d517-140">RELATED LINKS</span></span>
