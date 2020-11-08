---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093441"
---
# <span data-ttu-id="36c12-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="36c12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36c12-102">SYNOPSIS</span></span>
<span data-ttu-id="36c12-103">Lägger till en ny operativ Systems bild eller en ny virtuell dator bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="36c12-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="36c12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36c12-104">SYNTAX</span></span>

### <span data-ttu-id="36c12-105">OSImage (standard)</span><span class="sxs-lookup"><span data-stu-id="36c12-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="36c12-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="36c12-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36c12-107">DESCRIPTION</span></span>
<span data-ttu-id="36c12-108">Cmdleten **Add-AzureVMImage** lägger till en ny operativ Systems bild eller en ny virtuell dator bild i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="36c12-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="36c12-109">Bilden är en generaliserande operativ Systems bild, antingen via Sysprep för Windows eller, för Linux, med lämpligt verktyg för distribution.</span><span class="sxs-lookup"><span data-stu-id="36c12-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="36c12-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36c12-110">EXAMPLES</span></span>

### <span data-ttu-id="36c12-111">Exempel 1: lägga till en operativ Systems bild i databasen</span><span class="sxs-lookup"><span data-stu-id="36c12-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="36c12-112">I det här exemplet läggs en operativ system bild till i databasen.</span><span class="sxs-lookup"><span data-stu-id="36c12-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="36c12-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36c12-113">PARAMETERS</span></span>

### <span data-ttu-id="36c12-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="36c12-114">-Description</span></span>
<span data-ttu-id="36c12-115">Anger beskrivningen av operativ system bilden.</span><span class="sxs-lookup"><span data-stu-id="36c12-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="36c12-116">-DiskConfig</span></span>
<span data-ttu-id="36c12-117">Anger operativ systemets disk konfiguration för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="36c12-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="36c12-118">-Eula</span></span>
<span data-ttu-id="36c12-119">Anger licens avtalet för slutanvändare.</span><span class="sxs-lookup"><span data-stu-id="36c12-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="36c12-120">Vi rekommenderar att du använder en URL för det här värdet.</span><span class="sxs-lookup"><span data-stu-id="36c12-120">It is recommended that you use an URL for this value.</span></span>

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

### <span data-ttu-id="36c12-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="36c12-121">-IconName</span></span>
<span data-ttu-id="36c12-122">Anger namnet på den ikon som används när bilden läggs till i databasen.</span><span class="sxs-lookup"><span data-stu-id="36c12-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="36c12-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="36c12-123">-ImageFamily</span></span>
<span data-ttu-id="36c12-124">Anger ett värde som används för att gruppera operativ system bilder.</span><span class="sxs-lookup"><span data-stu-id="36c12-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="36c12-125">-ImageName</span></span>
<span data-ttu-id="36c12-126">Anger namnet på den bild som läggs till i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="36c12-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="36c12-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="36c12-127">-InformationAction</span></span>
<span data-ttu-id="36c12-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="36c12-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="36c12-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36c12-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36c12-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="36c12-130">Continue</span></span>
- <span data-ttu-id="36c12-131">Över</span><span class="sxs-lookup"><span data-stu-id="36c12-131">Ignore</span></span>
- <span data-ttu-id="36c12-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="36c12-132">Inquire</span></span>
- <span data-ttu-id="36c12-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="36c12-133">SilentlyContinue</span></span>
- <span data-ttu-id="36c12-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="36c12-134">Stop</span></span>
- <span data-ttu-id="36c12-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="36c12-135">Suspend</span></span>

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

### <span data-ttu-id="36c12-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="36c12-136">-InformationVariable</span></span>
<span data-ttu-id="36c12-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="36c12-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="36c12-138">-Etikett</span><span class="sxs-lookup"><span data-stu-id="36c12-138">-Label</span></span>
<span data-ttu-id="36c12-139">Anger en etikett för att ge bilden.</span><span class="sxs-lookup"><span data-stu-id="36c12-139">Specifies a label to give the image.</span></span>

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

### <span data-ttu-id="36c12-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="36c12-140">-MediaLocation</span></span>
<span data-ttu-id="36c12-141">Anger platsen för den fysiska BLOB-sidan där bilden finns.</span><span class="sxs-lookup"><span data-stu-id="36c12-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="36c12-142">Det här är en länk till en BLOB-sida i det aktuella abonnemangets lagring.</span><span class="sxs-lookup"><span data-stu-id="36c12-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-143">-OS</span><span class="sxs-lookup"><span data-stu-id="36c12-143">-OS</span></span>
<span data-ttu-id="36c12-144">Anger operativ system versionen för bilden.</span><span class="sxs-lookup"><span data-stu-id="36c12-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="36c12-145">-PrivacyUri</span></span>
<span data-ttu-id="36c12-146">Anger URL-adressen som pekar på ett dokument som innehåller integritets policyn för operativ system bilden.</span><span class="sxs-lookup"><span data-stu-id="36c12-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="36c12-147">-Profile</span></span>
<span data-ttu-id="36c12-148">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="36c12-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36c12-149">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="36c12-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36c12-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="36c12-150">-PublishedDate</span></span>
<span data-ttu-id="36c12-151">Anger det datum då operativ system bilden lades till i bild lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="36c12-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c12-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="36c12-152">-RecommendedVMSize</span></span>
<span data-ttu-id="36c12-153">Anger storleken som ska användas för den virtuella datorn som skapas från operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="36c12-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="36c12-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36c12-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36c12-155">Risk</span><span class="sxs-lookup"><span data-stu-id="36c12-155">Medium</span></span>
- <span data-ttu-id="36c12-156">Höga</span><span class="sxs-lookup"><span data-stu-id="36c12-156">Large</span></span>
- <span data-ttu-id="36c12-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="36c12-157">ExtraLarge</span></span>
- <span data-ttu-id="36c12-158">A5</span><span class="sxs-lookup"><span data-stu-id="36c12-158">A5</span></span>
- <span data-ttu-id="36c12-159">A6</span><span class="sxs-lookup"><span data-stu-id="36c12-159">A6</span></span>
- <span data-ttu-id="36c12-160">A7</span><span class="sxs-lookup"><span data-stu-id="36c12-160">A7</span></span>

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

### <span data-ttu-id="36c12-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="36c12-161">-ShowInGui</span></span>
<span data-ttu-id="36c12-162">Anger att den här cmdleten visar bilden i det grafiska användar gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="36c12-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

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

### <span data-ttu-id="36c12-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="36c12-163">-SmallIconName</span></span>
<span data-ttu-id="36c12-164">Anger namnet på den små ikonen som används när bilden läggs till i databasen.</span><span class="sxs-lookup"><span data-stu-id="36c12-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="36c12-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c12-165">CommonParameters</span></span>
<span data-ttu-id="36c12-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c12-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c12-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c12-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c12-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36c12-168">INPUTS</span></span>

## <span data-ttu-id="36c12-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36c12-169">OUTPUTS</span></span>

### <span data-ttu-id="36c12-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="36c12-170">OSImageContext</span></span>

## <span data-ttu-id="36c12-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36c12-171">NOTES</span></span>

## <span data-ttu-id="36c12-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36c12-172">RELATED LINKS</span></span>

[<span data-ttu-id="36c12-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="36c12-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="36c12-175">Spara – AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="36c12-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="36c12-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


