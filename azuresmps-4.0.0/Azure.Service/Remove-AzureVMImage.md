---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099684"
---
# <span data-ttu-id="a79e9-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a79e9-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="a79e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a79e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a79e9-103">Tar bort en operativ Systems bild från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a79e9-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="a79e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a79e9-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a79e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a79e9-105">DESCRIPTION</span></span>
<span data-ttu-id="a79e9-106">Cmdleten **Remove-AzureVMImage** tar bort en avbildning från avbildnings lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a79e9-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="a79e9-107">Denna cmdlet tar som standard inte bort den associerade fysiska avbildnings-blobben från lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a79e9-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="a79e9-108">Använd parametern **DeleteVHD** för att ta bort den anslutna virtuella hård disken.</span><span class="sxs-lookup"><span data-stu-id="a79e9-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="a79e9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a79e9-109">EXAMPLES</span></span>

### <span data-ttu-id="a79e9-110">Exempel 1: ta bort en bild från bild databasen</span><span class="sxs-lookup"><span data-stu-id="a79e9-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="a79e9-111">Det här kommandot tar bort bilden med namnet Image001 från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a79e9-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="a79e9-112">Exempel 2: ta bort en bild från bild lagrings platsen och en VHD</span><span class="sxs-lookup"><span data-stu-id="a79e9-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="a79e9-113">Det här kommandot tar bort bilden med namnet Image001 från bild lagrings platsen och tar också bort den fysiska VHD-avbildningen från lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a79e9-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="a79e9-114">Exempel 3: Ange en prenumerations kontext och ta sedan bort alla bilder</span><span class="sxs-lookup"><span data-stu-id="a79e9-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="a79e9-115">Det här kommandot anger prenumerationens kontext och tar sedan bort alla bilder från bild databasen vars etikett innehåller namnet beta.</span><span class="sxs-lookup"><span data-stu-id="a79e9-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="a79e9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a79e9-116">PARAMETERS</span></span>

### <span data-ttu-id="a79e9-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a79e9-117">-DeleteVHD</span></span>
<span data-ttu-id="a79e9-118">Anger att denna cmdlet tar bort BLOB för fysisk VHD-avbildning från lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a79e9-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a79e9-119">-ImageName</span></span>
<span data-ttu-id="a79e9-120">Anger det operativ system eller den virtuella dator avbildning som ska tas bort från bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a79e9-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a79e9-121">-InformationAction</span></span>
<span data-ttu-id="a79e9-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a79e9-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a79e9-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a79e9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a79e9-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="a79e9-124">Continue</span></span>
- <span data-ttu-id="a79e9-125">Över</span><span class="sxs-lookup"><span data-stu-id="a79e9-125">Ignore</span></span>
- <span data-ttu-id="a79e9-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="a79e9-126">Inquire</span></span>
- <span data-ttu-id="a79e9-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a79e9-127">SilentlyContinue</span></span>
- <span data-ttu-id="a79e9-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="a79e9-128">Stop</span></span>
- <span data-ttu-id="a79e9-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a79e9-129">Suspend</span></span>

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

### <span data-ttu-id="a79e9-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a79e9-130">-InformationVariable</span></span>
<span data-ttu-id="a79e9-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a79e9-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a79e9-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="a79e9-132">-Profile</span></span>
<span data-ttu-id="a79e9-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a79e9-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a79e9-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a79e9-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a79e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79e9-135">CommonParameters</span></span>
<span data-ttu-id="a79e9-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79e9-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79e9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79e9-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a79e9-138">INPUTS</span></span>

## <span data-ttu-id="a79e9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a79e9-139">OUTPUTS</span></span>

## <span data-ttu-id="a79e9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a79e9-140">NOTES</span></span>

## <span data-ttu-id="a79e9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a79e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="a79e9-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a79e9-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="a79e9-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a79e9-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="a79e9-144">Spara – AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a79e9-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="a79e9-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a79e9-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


