---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099762"
---
# <span data-ttu-id="6142d-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6142d-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="6142d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6142d-102">SYNOPSIS</span></span>
<span data-ttu-id="6142d-103">Hämtar egenskaperna för en eller flera listor med operativ system eller en virtuell dator bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="6142d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6142d-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6142d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6142d-105">DESCRIPTION</span></span>
<span data-ttu-id="6142d-106">Cmdleten **Get-AzureVMImage** hämtar egenskaper för en eller flera listor med operativ system eller en virtuell dator bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="6142d-107">Cmdleten returnerar information för alla bilder i databasen, eller om en viss bild visas om bild namnet anges.</span><span class="sxs-lookup"><span data-stu-id="6142d-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="6142d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6142d-108">EXAMPLES</span></span>

### <span data-ttu-id="6142d-109">Exempel 1: Hämta ett specifikt bild objekt från den aktuella bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="6142d-110">Det här kommandot hämtar bild objekt med namnet Image001 från den aktuella bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="6142d-111">Exempel 2: Hämta alla bilder från den aktuella bild databasen</span><span class="sxs-lookup"><span data-stu-id="6142d-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="6142d-112">Det här kommandot hämtar alla bilder från den aktuella bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="6142d-113">Exempel 3: Ange prenumerationens kontext och hämta sedan alla bilder</span><span class="sxs-lookup"><span data-stu-id="6142d-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="6142d-114">Det här kommandot anger prenumerationens kontext och hämtar sedan alla bilder från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="6142d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6142d-115">PARAMETERS</span></span>

### <span data-ttu-id="6142d-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6142d-116">-ImageName</span></span>
<span data-ttu-id="6142d-117">Anger namnet på operativ system eller virtuell dator bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="6142d-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="6142d-118">Om du inte anger den här parametern returneras alla bilder.</span><span class="sxs-lookup"><span data-stu-id="6142d-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6142d-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6142d-119">-InformationAction</span></span>
<span data-ttu-id="6142d-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6142d-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6142d-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6142d-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6142d-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="6142d-122">Continue</span></span>
- <span data-ttu-id="6142d-123">Över</span><span class="sxs-lookup"><span data-stu-id="6142d-123">Ignore</span></span>
- <span data-ttu-id="6142d-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="6142d-124">Inquire</span></span>
- <span data-ttu-id="6142d-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6142d-125">SilentlyContinue</span></span>
- <span data-ttu-id="6142d-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="6142d-126">Stop</span></span>
- <span data-ttu-id="6142d-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6142d-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6142d-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6142d-128">-InformationVariable</span></span>
<span data-ttu-id="6142d-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6142d-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6142d-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="6142d-130">-Profile</span></span>
<span data-ttu-id="6142d-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6142d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6142d-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6142d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6142d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6142d-133">CommonParameters</span></span>
<span data-ttu-id="6142d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6142d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6142d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6142d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6142d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6142d-136">INPUTS</span></span>

## <span data-ttu-id="6142d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6142d-137">OUTPUTS</span></span>

## <span data-ttu-id="6142d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6142d-138">NOTES</span></span>

## <span data-ttu-id="6142d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6142d-139">RELATED LINKS</span></span>

[<span data-ttu-id="6142d-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6142d-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="6142d-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6142d-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="6142d-142">Spara – AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6142d-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="6142d-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6142d-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


