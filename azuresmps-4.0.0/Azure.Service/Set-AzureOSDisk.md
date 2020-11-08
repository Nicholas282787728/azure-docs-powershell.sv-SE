---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099058"
---
# <span data-ttu-id="c535b-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="c535b-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="c535b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c535b-102">SYNOPSIS</span></span>
<span data-ttu-id="c535b-103">Ändrar Host cacheläge för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="c535b-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="c535b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c535b-104">SYNTAX</span></span>

### <span data-ttu-id="c535b-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="c535b-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c535b-106">Ändra storlek på</span><span class="sxs-lookup"><span data-stu-id="c535b-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c535b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c535b-107">DESCRIPTION</span></span>
<span data-ttu-id="c535b-108">Cmdleten **set-AzureOSDisk** ändrar cacheminnet på operativ systemets disk för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="c535b-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="c535b-109">De cachealternativ som stöds är ReadOnly och ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c535b-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="c535b-110">Om du kör denna cmdlet på en virtuell dator som körs startas den om.</span><span class="sxs-lookup"><span data-stu-id="c535b-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="c535b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c535b-111">EXAMPLES</span></span>

### <span data-ttu-id="c535b-112">Exempel 1: Ställ in värdet för cacheminnet på ReadOnly genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="c535b-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="c535b-113">Det här kommandot får den virtuella datorn som heter VirtualMachine02 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c535b-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c535b-114">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="c535b-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c535b-115">Den aktuella cmdleten anger att den virtuella datorns operativ system disk är skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="c535b-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="c535b-116">Exempel 2: Ange Host cacheläge-läget för att ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c535b-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="c535b-117">Det första kommandot får den virtuella datorn som heter VirtualMachine02 i tjänsten ContosoService och lagrar den sedan i variabeln.</span><span class="sxs-lookup"><span data-stu-id="c535b-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="c535b-118">Det andra kommandot ställer in värdet för värd-cachen på operativ system disken på den virtuella datorn för att kunna ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c535b-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="c535b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c535b-119">PARAMETERS</span></span>

### <span data-ttu-id="c535b-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="c535b-120">-HostCaching</span></span>
<span data-ttu-id="c535b-121">Anger attributet Host cache för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="c535b-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="c535b-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="c535b-122">Valid values are:</span></span> 

- <span data-ttu-id="c535b-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c535b-123">ReadOnly</span></span> 
- <span data-ttu-id="c535b-124">Läs</span><span class="sxs-lookup"><span data-stu-id="c535b-124">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c535b-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c535b-125">-InformationAction</span></span>
<span data-ttu-id="c535b-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c535b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c535b-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c535b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c535b-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="c535b-128">Continue</span></span>
- <span data-ttu-id="c535b-129">Över</span><span class="sxs-lookup"><span data-stu-id="c535b-129">Ignore</span></span>
- <span data-ttu-id="c535b-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="c535b-130">Inquire</span></span>
- <span data-ttu-id="c535b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c535b-131">SilentlyContinue</span></span>
- <span data-ttu-id="c535b-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="c535b-132">Stop</span></span>
- <span data-ttu-id="c535b-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c535b-133">Suspend</span></span>

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

### <span data-ttu-id="c535b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c535b-134">-InformationVariable</span></span>
<span data-ttu-id="c535b-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c535b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c535b-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="c535b-136">-Profile</span></span>
<span data-ttu-id="c535b-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c535b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c535b-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c535b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c535b-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c535b-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="c535b-140">Anger en ny storlek i GB för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="c535b-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="c535b-141">Storleken måste vara större än den aktuella storleken.</span><span class="sxs-lookup"><span data-stu-id="c535b-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c535b-142">-VM</span><span class="sxs-lookup"><span data-stu-id="c535b-142">-VM</span></span>
<span data-ttu-id="c535b-143">Anger den virtuella dator för vilken den här cmdleten ändrar operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="c535b-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="c535b-144">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="c535b-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c535b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c535b-145">CommonParameters</span></span>
<span data-ttu-id="c535b-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c535b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c535b-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c535b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c535b-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c535b-148">INPUTS</span></span>

## <span data-ttu-id="c535b-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c535b-149">OUTPUTS</span></span>

## <span data-ttu-id="c535b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c535b-150">NOTES</span></span>

## <span data-ttu-id="c535b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c535b-151">RELATED LINKS</span></span>

[<span data-ttu-id="c535b-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c535b-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="c535b-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="c535b-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="c535b-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c535b-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c535b-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c535b-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="c535b-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c535b-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="c535b-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c535b-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


