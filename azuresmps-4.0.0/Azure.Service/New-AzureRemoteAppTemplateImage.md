---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099225"
---
# <span data-ttu-id="12d6c-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="12d6c-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="12d6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="12d6c-103">Laddar upp eller importerar en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="12d6c-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="12d6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12d6c-104">SYNTAX</span></span>

### <span data-ttu-id="12d6c-105">UploadLocalVhd (standard)</span><span class="sxs-lookup"><span data-stu-id="12d6c-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="12d6c-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="12d6c-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="12d6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="12d6c-108">**New-AzureRemoteAppTemplateImage** cmdlet laddar eller importerar en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="12d6c-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="12d6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12d6c-109">EXAMPLES</span></span>

### <span data-ttu-id="12d6c-110">Exempel 1: Ladda upp en VHD-fil för att skapa en mall</span><span class="sxs-lookup"><span data-stu-id="12d6c-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="12d6c-111">Det här kommandot laddar upp C:\RemoteAppImages\ContosoApps.vhd och skapar en mall med namnet ContosoApps i Nord Europe Data Center.</span><span class="sxs-lookup"><span data-stu-id="12d6c-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="12d6c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12d6c-112">PARAMETERS</span></span>

### <span data-ttu-id="12d6c-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="12d6c-113">-AzureVmImageName</span></span>
<span data-ttu-id="12d6c-114">Anger namnet på en virtuell Azure-dator som ska användas som mall.</span><span class="sxs-lookup"><span data-stu-id="12d6c-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d6c-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="12d6c-115">-ImageName</span></span>
<span data-ttu-id="12d6c-116">Anger namnet på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="12d6c-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12d6c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="12d6c-117">-Location</span></span>
<span data-ttu-id="12d6c-118">Anger mallens Azure-region.</span><span class="sxs-lookup"><span data-stu-id="12d6c-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d6c-119">-Path</span><span class="sxs-lookup"><span data-stu-id="12d6c-119">-Path</span></span>
<span data-ttu-id="12d6c-120">Anger sökvägen till mallen.</span><span class="sxs-lookup"><span data-stu-id="12d6c-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d6c-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="12d6c-121">-Profile</span></span>
<span data-ttu-id="12d6c-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="12d6c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12d6c-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="12d6c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12d6c-124">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="12d6c-124">-Resume</span></span>
<span data-ttu-id="12d6c-125">Anger att denna cmdlet fortsätter om uppladdning av en mallfil avbryts.</span><span class="sxs-lookup"><span data-stu-id="12d6c-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d6c-126">CommonParameters</span></span>
<span data-ttu-id="12d6c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d6c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d6c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12d6c-129">INPUTS</span></span>

## <span data-ttu-id="12d6c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12d6c-130">OUTPUTS</span></span>

## <span data-ttu-id="12d6c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12d6c-131">NOTES</span></span>

## <span data-ttu-id="12d6c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12d6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="12d6c-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="12d6c-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="12d6c-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="12d6c-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="12d6c-135">Rename – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="12d6c-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


