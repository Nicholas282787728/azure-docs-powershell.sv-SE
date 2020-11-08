---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099584"
---
# <span data-ttu-id="6c8e3-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-101">Get-AzureDisk</span></span>

## <span data-ttu-id="6c8e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8e3-103">Hämtar information om diskar i Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="6c8e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c8e3-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c8e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c8e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8e3-106">Cmdleten **Get-AzureDisk** hämtar information om de diskar som lagras i Azure-lagringsplatsen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="6c8e3-107">Denna cmdlet returnerar en lista med information för alla diskar i databasen.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="6c8e3-108">Om du vill visa information om en viss disk anger du namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="6c8e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c8e3-109">EXAMPLES</span></span>

### <span data-ttu-id="6c8e3-110">Exempel 1: Hämta information om en disk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="6c8e3-111">Det här kommandot hämtar information om den disk som heter ContosoDataDisk från diskens lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="6c8e3-112">Exempel 2: få information om alla diskar</span><span class="sxs-lookup"><span data-stu-id="6c8e3-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="6c8e3-113">Med det här kommandot får du information om alla diskar i disk lagringen.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="6c8e3-114">Exempel 3: Hämta information om en disk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="6c8e3-115">Det här kommandot hämtar data för alla diskar i disk lagrings platsen som för närvarande inte är anslutna till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="6c8e3-116">Med kommandot får du information om alla diskar och skickar objekten till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="6c8e3-117">Denna cmdlet tar alla diskar som inte har värdet $Null för egenskapen **AttachedTo** .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="6c8e3-118">Kommandot formaterar listan som en tabell med hjälp av cmdleten **Format-Table** .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="6c8e3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c8e3-119">PARAMETERS</span></span>

### <span data-ttu-id="6c8e3-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="6c8e3-120">-DiskName</span></span>
<span data-ttu-id="6c8e3-121">Anger namnet på den disk i disk lagringen där denna cmdlet hämtar information.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="6c8e3-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6c8e3-122">-InformationAction</span></span>
<span data-ttu-id="6c8e3-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6c8e3-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6c8e3-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c8e3-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="6c8e3-125">Continue</span></span>
- <span data-ttu-id="6c8e3-126">Över</span><span class="sxs-lookup"><span data-stu-id="6c8e3-126">Ignore</span></span>
- <span data-ttu-id="6c8e3-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="6c8e3-127">Inquire</span></span>
- <span data-ttu-id="6c8e3-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6c8e3-128">SilentlyContinue</span></span>
- <span data-ttu-id="6c8e3-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="6c8e3-129">Stop</span></span>
- <span data-ttu-id="6c8e3-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6c8e3-130">Suspend</span></span>

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

### <span data-ttu-id="6c8e3-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6c8e3-131">-InformationVariable</span></span>
<span data-ttu-id="6c8e3-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6c8e3-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c8e3-133">-Profile</span></span>
<span data-ttu-id="6c8e3-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c8e3-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c8e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8e3-136">CommonParameters</span></span>
<span data-ttu-id="6c8e3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8e3-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8e3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c8e3-139">INPUTS</span></span>

## <span data-ttu-id="6c8e3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c8e3-140">OUTPUTS</span></span>

## <span data-ttu-id="6c8e3-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c8e3-141">NOTES</span></span>

## <span data-ttu-id="6c8e3-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c8e3-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c8e3-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="6c8e3-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="6c8e3-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="6c8e3-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


