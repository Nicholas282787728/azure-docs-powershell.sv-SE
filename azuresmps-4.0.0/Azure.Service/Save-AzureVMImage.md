---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093177"
---
# <span data-ttu-id="97b38-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="97b38-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="97b38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97b38-102">SYNOPSIS</span></span>
<span data-ttu-id="97b38-103">Avbildningen av den stoppade virtuella Azure-datorn sparas.</span><span class="sxs-lookup"><span data-stu-id="97b38-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="97b38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97b38-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="97b38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97b38-105">DESCRIPTION</span></span>
<span data-ttu-id="97b38-106">Cmdleten **Save-AzureVMImage** fångar in och sparar bilden av en stoppad Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="97b38-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="97b38-107">Kör verktyget Sysprep för att förbereda bilden innan den sparas.</span><span class="sxs-lookup"><span data-stu-id="97b38-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="97b38-108">När bilden har tagits bort raderas den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97b38-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="97b38-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97b38-109">EXAMPLES</span></span>

### <span data-ttu-id="97b38-110">Exempel 1: Spara en befintlig virtuell dator och ta sedan bort den från en distribution</span><span class="sxs-lookup"><span data-stu-id="97b38-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="97b38-111">Det här kommandot fångar en befintlig virtuell dator och tar bort den från distributionen.</span><span class="sxs-lookup"><span data-stu-id="97b38-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="97b38-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97b38-112">PARAMETERS</span></span>

### <span data-ttu-id="97b38-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="97b38-113">-ImageLabel</span></span>
<span data-ttu-id="97b38-114">Anger etiketten för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="97b38-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b38-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="97b38-115">-ImageName</span></span>
<span data-ttu-id="97b38-116">Anger namnet på den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="97b38-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b38-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="97b38-117">-InformationAction</span></span>
<span data-ttu-id="97b38-118">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="97b38-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="97b38-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="97b38-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97b38-120">Vidare</span><span class="sxs-lookup"><span data-stu-id="97b38-120">Continue</span></span>
- <span data-ttu-id="97b38-121">Över</span><span class="sxs-lookup"><span data-stu-id="97b38-121">Ignore</span></span>
- <span data-ttu-id="97b38-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="97b38-122">Inquire</span></span>
- <span data-ttu-id="97b38-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="97b38-123">SilentlyContinue</span></span>
- <span data-ttu-id="97b38-124">Stanna</span><span class="sxs-lookup"><span data-stu-id="97b38-124">Stop</span></span>
- <span data-ttu-id="97b38-125">Avbryt</span><span class="sxs-lookup"><span data-stu-id="97b38-125">Suspend</span></span>

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

### <span data-ttu-id="97b38-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="97b38-126">-InformationVariable</span></span>
<span data-ttu-id="97b38-127">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="97b38-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97b38-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="97b38-128">-Name</span></span>
<span data-ttu-id="97b38-129">Anger namnet på den virtuella käll datorn.</span><span class="sxs-lookup"><span data-stu-id="97b38-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="97b38-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="97b38-130">-OSState</span></span>
<span data-ttu-id="97b38-131">Anger system tillstånd för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="97b38-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="97b38-132">Använd den här parametern om du tänker avbilda en virtuell dator bild till Azure.</span><span class="sxs-lookup"><span data-stu-id="97b38-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="97b38-133">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="97b38-133">Valid values are:</span></span>

- <span data-ttu-id="97b38-134">Generalized</span><span class="sxs-lookup"><span data-stu-id="97b38-134">Generalized</span></span>
- <span data-ttu-id="97b38-135">Specialverktyg</span><span class="sxs-lookup"><span data-stu-id="97b38-135">Specialized</span></span>

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

### <span data-ttu-id="97b38-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="97b38-136">-Profile</span></span>
<span data-ttu-id="97b38-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="97b38-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97b38-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="97b38-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97b38-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="97b38-139">-ServiceName</span></span>
<span data-ttu-id="97b38-140">Anger namnet på Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97b38-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="97b38-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b38-141">CommonParameters</span></span>
<span data-ttu-id="97b38-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b38-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b38-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b38-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b38-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97b38-144">INPUTS</span></span>

## <span data-ttu-id="97b38-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97b38-145">OUTPUTS</span></span>

## <span data-ttu-id="97b38-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97b38-146">NOTES</span></span>

## <span data-ttu-id="97b38-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97b38-147">RELATED LINKS</span></span>

[<span data-ttu-id="97b38-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="97b38-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="97b38-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="97b38-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="97b38-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="97b38-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="97b38-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="97b38-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


