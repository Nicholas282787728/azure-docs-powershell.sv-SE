---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099387"
---
# <span data-ttu-id="52889-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="52889-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="52889-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52889-102">SYNOPSIS</span></span>
<span data-ttu-id="52889-103">Tar bort en disk från Azure disk-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="52889-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="52889-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52889-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="52889-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52889-105">DESCRIPTION</span></span>
<span data-ttu-id="52889-106">Cmdleten **Remove-AzureDisk** tar bort en disk från Azure disk-lagringsplatsen i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="52889-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="52889-107">Standardinställningen är att denna cmdlet inte tar bort den virtuella hård disk filen (VHD) från Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="52889-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="52889-108">Om du vill ta bort VHD-disken anger du parametern *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="52889-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="52889-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52889-109">EXAMPLES</span></span>

### <span data-ttu-id="52889-110">Exempel 1: ta bort en disk</span><span class="sxs-lookup"><span data-stu-id="52889-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="52889-111">Det här kommandot tar bort disketten med namnet ContosoDataDisk från disk lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="52889-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="52889-112">Kommandot tar inte bort VHD.</span><span class="sxs-lookup"><span data-stu-id="52889-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="52889-113">Exempel 2: ta bort och ta bort en disk</span><span class="sxs-lookup"><span data-stu-id="52889-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="52889-114">Det här kommandot tar bort disketten med namnet ContosoDataDisk från disk lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="52889-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="52889-115">Det här kommandot anger parametern DeleteVHD.</span><span class="sxs-lookup"><span data-stu-id="52889-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="52889-116">Därför tar kommandot bort VHD från Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="52889-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="52889-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52889-117">PARAMETERS</span></span>

### <span data-ttu-id="52889-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="52889-118">-DeleteVHD</span></span>
<span data-ttu-id="52889-119">Anger att denna cmdlet tar bort VHD från Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="52889-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52889-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="52889-120">-DiskName</span></span>
<span data-ttu-id="52889-121">Anger namnet på data disken i disk lagringen där denna cmdlet ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="52889-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="52889-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="52889-122">-InformationAction</span></span>
<span data-ttu-id="52889-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="52889-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="52889-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="52889-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52889-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="52889-125">Continue</span></span>
- <span data-ttu-id="52889-126">Över</span><span class="sxs-lookup"><span data-stu-id="52889-126">Ignore</span></span>
- <span data-ttu-id="52889-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="52889-127">Inquire</span></span>
- <span data-ttu-id="52889-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="52889-128">SilentlyContinue</span></span>
- <span data-ttu-id="52889-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="52889-129">Stop</span></span>
- <span data-ttu-id="52889-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="52889-130">Suspend</span></span>

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

### <span data-ttu-id="52889-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="52889-131">-InformationVariable</span></span>
<span data-ttu-id="52889-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="52889-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="52889-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="52889-133">-Profile</span></span>
<span data-ttu-id="52889-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="52889-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52889-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="52889-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52889-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52889-136">CommonParameters</span></span>
<span data-ttu-id="52889-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52889-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52889-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52889-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52889-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52889-139">INPUTS</span></span>

## <span data-ttu-id="52889-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52889-140">OUTPUTS</span></span>

## <span data-ttu-id="52889-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52889-141">NOTES</span></span>

## <span data-ttu-id="52889-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52889-142">RELATED LINKS</span></span>

[<span data-ttu-id="52889-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="52889-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="52889-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="52889-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="52889-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="52889-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


