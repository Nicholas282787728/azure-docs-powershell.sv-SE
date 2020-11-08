---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099813"
---
# <span data-ttu-id="3818a-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3818a-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="3818a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3818a-102">SYNOPSIS</span></span>
<span data-ttu-id="3818a-103">Uppdaterar etiketten för en operativ Systems bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="3818a-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="3818a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3818a-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3818a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3818a-105">DESCRIPTION</span></span>
<span data-ttu-id="3818a-106">Cmdleten **Update-AzureVMImage** uppdaterar etiketten på en operativ Systems bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="3818a-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="3818a-107">Den returnerar ett bild objekt med information om den uppdaterade bilden.</span><span class="sxs-lookup"><span data-stu-id="3818a-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="3818a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3818a-108">EXAMPLES</span></span>

### <span data-ttu-id="3818a-109">Exempel 1: uppdatera en bild genom att ändra bild etiketten</span><span class="sxs-lookup"><span data-stu-id="3818a-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="3818a-110">Det här kommandot uppdaterar bilden med namnet Windows-Server-2008-SP2 genom att ändra bild etiketten till DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="3818a-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="3818a-111">Exempel 2: Hämta alla operativ system efter etikett och uppdatera sedan etiketten</span><span class="sxs-lookup"><span data-stu-id="3818a-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="3818a-112">Det här kommandot får alla operativ system bilder med etiketten DoNotUse och ändrar etiketten till uppdaterad.</span><span class="sxs-lookup"><span data-stu-id="3818a-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="3818a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3818a-113">PARAMETERS</span></span>

### <span data-ttu-id="3818a-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3818a-114">-Description</span></span>
<span data-ttu-id="3818a-115">Anger beskrivningen av operativ system bilden.</span><span class="sxs-lookup"><span data-stu-id="3818a-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="3818a-116">-DiskConfig</span></span>
<span data-ttu-id="3818a-117">Anger operativ system disk och data disk konfiguration för den virtuella dator avbildningen som har skapats med cmdletarna **New-AzureVMImageDiskConfigSet** , **set-AzureVMImageOSDiskConfig** och **set-AzureVMImageDataDiskConfig** .</span><span class="sxs-lookup"><span data-stu-id="3818a-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="3818a-118">-DontShowInGui</span></span>
<span data-ttu-id="3818a-119">Anger att denna cmdlet inte visar bilden i det grafiska användar gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3818a-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="3818a-120">-Eula</span></span>
<span data-ttu-id="3818a-121">Anger licens avtalet för slutanvändare.</span><span class="sxs-lookup"><span data-stu-id="3818a-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="3818a-122">Vi rekommenderar att värdet är en URL-adress.</span><span class="sxs-lookup"><span data-stu-id="3818a-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="3818a-123">-IconName</span></span>
<span data-ttu-id="3818a-124">Anger standard ikonen för operativ systemet eller den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="3818a-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="3818a-125">-ImageFamily</span></span>
<span data-ttu-id="3818a-126">Anger ett värde som kan användas för att gruppera operativ system eller virtuella dator bilder.</span><span class="sxs-lookup"><span data-stu-id="3818a-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3818a-127">-ImageName</span></span>
<span data-ttu-id="3818a-128">Anger namnet på den bild som ska uppdateras i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="3818a-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="3818a-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3818a-129">-InformationAction</span></span>
<span data-ttu-id="3818a-130">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3818a-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3818a-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3818a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3818a-132">Vidare</span><span class="sxs-lookup"><span data-stu-id="3818a-132">Continue</span></span>
- <span data-ttu-id="3818a-133">Över</span><span class="sxs-lookup"><span data-stu-id="3818a-133">Ignore</span></span>
- <span data-ttu-id="3818a-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="3818a-134">Inquire</span></span>
- <span data-ttu-id="3818a-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3818a-135">SilentlyContinue</span></span>
- <span data-ttu-id="3818a-136">Stanna</span><span class="sxs-lookup"><span data-stu-id="3818a-136">Stop</span></span>
- <span data-ttu-id="3818a-137">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3818a-137">Suspend</span></span>

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

### <span data-ttu-id="3818a-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3818a-138">-InformationVariable</span></span>
<span data-ttu-id="3818a-139">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3818a-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3818a-140">-Etikett</span><span class="sxs-lookup"><span data-stu-id="3818a-140">-Label</span></span>
<span data-ttu-id="3818a-141">Anger bildens nya etikett.</span><span class="sxs-lookup"><span data-stu-id="3818a-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-142">-Språk</span><span class="sxs-lookup"><span data-stu-id="3818a-142">-Language</span></span>
<span data-ttu-id="3818a-143">Anger språket för operativ systemet på den virtuella datorn eller operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="3818a-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="3818a-144">-PrivacyUri</span></span>
<span data-ttu-id="3818a-145">Anger URI: n som pekar på ett dokument som innehåller integritets policyn för operativ system bilden.</span><span class="sxs-lookup"><span data-stu-id="3818a-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="3818a-146">-Profile</span></span>
<span data-ttu-id="3818a-147">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3818a-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3818a-148">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3818a-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3818a-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="3818a-149">-PublishedDate</span></span>
<span data-ttu-id="3818a-150">Anger det datum då operativ system bilden lades till i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="3818a-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="3818a-151">-RecommendedVMSize</span></span>
<span data-ttu-id="3818a-152">Anger storleken på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3818a-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="3818a-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3818a-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3818a-154">Risk</span><span class="sxs-lookup"><span data-stu-id="3818a-154">Medium</span></span>
- <span data-ttu-id="3818a-155">Höga</span><span class="sxs-lookup"><span data-stu-id="3818a-155">Large</span></span>
- <span data-ttu-id="3818a-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="3818a-156">ExtraLarge</span></span>
- <span data-ttu-id="3818a-157">A5</span><span class="sxs-lookup"><span data-stu-id="3818a-157">A5</span></span>
- <span data-ttu-id="3818a-158">A6</span><span class="sxs-lookup"><span data-stu-id="3818a-158">A6</span></span>
- <span data-ttu-id="3818a-159">A7</span><span class="sxs-lookup"><span data-stu-id="3818a-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="3818a-160">-SmallIconName</span></span>
<span data-ttu-id="3818a-161">Anger namnet på den lilla ikonen för operativ systemet eller den virtuella dator bilden.</span><span class="sxs-lookup"><span data-stu-id="3818a-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3818a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3818a-162">CommonParameters</span></span>
<span data-ttu-id="3818a-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3818a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3818a-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3818a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3818a-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3818a-165">INPUTS</span></span>

## <span data-ttu-id="3818a-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3818a-166">OUTPUTS</span></span>

### <span data-ttu-id="3818a-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="3818a-167">OSImageContext</span></span>

## <span data-ttu-id="3818a-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3818a-168">NOTES</span></span>

## <span data-ttu-id="3818a-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3818a-169">RELATED LINKS</span></span>

[<span data-ttu-id="3818a-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3818a-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="3818a-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3818a-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="3818a-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3818a-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="3818a-173">Spara – AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3818a-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="3818a-174">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="3818a-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="3818a-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="3818a-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="3818a-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="3818a-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


