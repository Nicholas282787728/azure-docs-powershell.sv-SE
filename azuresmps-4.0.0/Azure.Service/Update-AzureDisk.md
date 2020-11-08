---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093151"
---
# <span data-ttu-id="a01df-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a01df-101">Update-AzureDisk</span></span>

## <span data-ttu-id="a01df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a01df-102">SYNOPSIS</span></span>
<span data-ttu-id="a01df-103">Ändrar etiketten för en disk i Azure disk-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="a01df-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="a01df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a01df-104">SYNTAX</span></span>

### <span data-ttu-id="a01df-105">Ändra storlek på</span><span class="sxs-lookup"><span data-stu-id="a01df-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a01df-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="a01df-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a01df-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a01df-107">DESCRIPTION</span></span>
<span data-ttu-id="a01df-108">Cmdleten **Update-AzureDisk** ändrar etiketten som är kopplad till en disk i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a01df-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="a01df-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a01df-109">EXAMPLES</span></span>

### <span data-ttu-id="a01df-110">Exempel 1: ändra etiketten för en disk</span><span class="sxs-lookup"><span data-stu-id="a01df-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="a01df-111">Det här kommandot ändrar etiketten för den disk som heter ContosoOSDisk till DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="a01df-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="a01df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a01df-112">PARAMETERS</span></span>

### <span data-ttu-id="a01df-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a01df-113">-DiskName</span></span>
<span data-ttu-id="a01df-114">Anger namnet på den disk som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a01df-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a01df-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a01df-115">-InformationAction</span></span>
<span data-ttu-id="a01df-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a01df-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a01df-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a01df-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a01df-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="a01df-118">Continue</span></span>
- <span data-ttu-id="a01df-119">Över</span><span class="sxs-lookup"><span data-stu-id="a01df-119">Ignore</span></span>
- <span data-ttu-id="a01df-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="a01df-120">Inquire</span></span>
- <span data-ttu-id="a01df-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a01df-121">SilentlyContinue</span></span>
- <span data-ttu-id="a01df-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="a01df-122">Stop</span></span>
- <span data-ttu-id="a01df-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a01df-123">Suspend</span></span>

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

### <span data-ttu-id="a01df-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a01df-124">-InformationVariable</span></span>
<span data-ttu-id="a01df-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a01df-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a01df-126">-Etikett</span><span class="sxs-lookup"><span data-stu-id="a01df-126">-Label</span></span>
<span data-ttu-id="a01df-127">Anger den nya etiketten för disken.</span><span class="sxs-lookup"><span data-stu-id="a01df-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01df-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a01df-128">-Profile</span></span>
<span data-ttu-id="a01df-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a01df-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a01df-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a01df-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a01df-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a01df-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="a01df-132">Anger den nya storleken i GB på disken.</span><span class="sxs-lookup"><span data-stu-id="a01df-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01df-133">CommonParameters</span></span>
<span data-ttu-id="a01df-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01df-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01df-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01df-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a01df-136">INPUTS</span></span>

## <span data-ttu-id="a01df-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a01df-137">OUTPUTS</span></span>

### <span data-ttu-id="a01df-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="a01df-138">DiskContext</span></span>

## <span data-ttu-id="a01df-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a01df-139">NOTES</span></span>

## <span data-ttu-id="a01df-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a01df-140">RELATED LINKS</span></span>

[<span data-ttu-id="a01df-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a01df-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="a01df-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a01df-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="a01df-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a01df-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


