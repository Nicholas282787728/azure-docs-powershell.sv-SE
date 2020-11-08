---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099623"
---
# <span data-ttu-id="a09ea-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a09ea-101">Add-AzureDisk</span></span>

## <span data-ttu-id="a09ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a09ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a09ea-103">Lägger till en disk i Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="a09ea-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="a09ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a09ea-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a09ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a09ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a09ea-106">Cmdleten **Add-AzureDisk** lägger till en disk i Azure disk-lagringsplatsen i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a09ea-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="a09ea-107">Denna cmdlet kan lägga till en system diskett eller en data skiva.</span><span class="sxs-lookup"><span data-stu-id="a09ea-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="a09ea-108">Om du vill lägga till en system diskett anger du en operativ system typ genom att använda *OS* -parametern.</span><span class="sxs-lookup"><span data-stu-id="a09ea-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="a09ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a09ea-109">EXAMPLES</span></span>

### <span data-ttu-id="a09ea-110">Exempel 1: lägga till en start diskett med operativ systemet Windows</span><span class="sxs-lookup"><span data-stu-id="a09ea-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="a09ea-111">Det här kommandot lägger till en system disk till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a09ea-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="a09ea-112">System disken använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="a09ea-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="a09ea-113">Exempel 2: lägga till en data disk</span><span class="sxs-lookup"><span data-stu-id="a09ea-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="a09ea-114">Det här kommandot lägger till en data disk.</span><span class="sxs-lookup"><span data-stu-id="a09ea-114">This command adds a data disk.</span></span>

### <span data-ttu-id="a09ea-115">Exempel 3: lägga till en system disk för Linux</span><span class="sxs-lookup"><span data-stu-id="a09ea-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="a09ea-116">Det här kommandot lägger till en system disk för Linux.</span><span class="sxs-lookup"><span data-stu-id="a09ea-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="a09ea-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a09ea-117">PARAMETERS</span></span>

### <span data-ttu-id="a09ea-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a09ea-118">-DiskName</span></span>
<span data-ttu-id="a09ea-119">Anger namnet på den disk som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="a09ea-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a09ea-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a09ea-120">-InformationAction</span></span>
<span data-ttu-id="a09ea-121">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a09ea-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a09ea-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09ea-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09ea-123">Vidare</span><span class="sxs-lookup"><span data-stu-id="a09ea-123">Continue</span></span>
- <span data-ttu-id="a09ea-124">Över</span><span class="sxs-lookup"><span data-stu-id="a09ea-124">Ignore</span></span>
- <span data-ttu-id="a09ea-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="a09ea-125">Inquire</span></span>
- <span data-ttu-id="a09ea-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a09ea-126">SilentlyContinue</span></span>
- <span data-ttu-id="a09ea-127">Stanna</span><span class="sxs-lookup"><span data-stu-id="a09ea-127">Stop</span></span>
- <span data-ttu-id="a09ea-128">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a09ea-128">Suspend</span></span>

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

### <span data-ttu-id="a09ea-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a09ea-129">-InformationVariable</span></span>
<span data-ttu-id="a09ea-130">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a09ea-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a09ea-131">-Etikett</span><span class="sxs-lookup"><span data-stu-id="a09ea-131">-Label</span></span>
<span data-ttu-id="a09ea-132">Anger en disk etikett för disken där denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="a09ea-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09ea-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="a09ea-133">-MediaLocation</span></span>
<span data-ttu-id="a09ea-134">Anger den fysiska platsen för disken i Azure-lagringen.</span><span class="sxs-lookup"><span data-stu-id="a09ea-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="a09ea-135">Det här värdet refererar till en BLOB-sida i det aktuella abonnemanget och lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a09ea-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="a09ea-136">-OS</span><span class="sxs-lookup"><span data-stu-id="a09ea-136">-OS</span></span>
<span data-ttu-id="a09ea-137">Anger operativ system typen för en system disk.</span><span class="sxs-lookup"><span data-stu-id="a09ea-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="a09ea-138">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a09ea-138">Valid values are:</span></span> 

- <span data-ttu-id="a09ea-139">Windows</span><span class="sxs-lookup"><span data-stu-id="a09ea-139">Windows</span></span> 
- <span data-ttu-id="a09ea-140">Linux</span><span class="sxs-lookup"><span data-stu-id="a09ea-140">Linux</span></span> 

<span data-ttu-id="a09ea-141">Om du inte anger den här parametern lägger cmdleten till disken som en data skiva.</span><span class="sxs-lookup"><span data-stu-id="a09ea-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09ea-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="a09ea-142">-Profile</span></span>
<span data-ttu-id="a09ea-143">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a09ea-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a09ea-144">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a09ea-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a09ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09ea-145">CommonParameters</span></span>
<span data-ttu-id="a09ea-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09ea-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09ea-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09ea-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a09ea-148">INPUTS</span></span>

## <span data-ttu-id="a09ea-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a09ea-149">OUTPUTS</span></span>

### <span data-ttu-id="a09ea-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="a09ea-150">DiskContext</span></span>

## <span data-ttu-id="a09ea-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a09ea-151">NOTES</span></span>

## <span data-ttu-id="a09ea-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a09ea-152">RELATED LINKS</span></span>

[<span data-ttu-id="a09ea-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a09ea-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="a09ea-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a09ea-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="a09ea-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a09ea-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


