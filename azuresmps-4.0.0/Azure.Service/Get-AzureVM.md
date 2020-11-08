---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099777"
---
# <span data-ttu-id="28849-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-101">Get-AzureVM</span></span>

## <span data-ttu-id="28849-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28849-102">SYNOPSIS</span></span>
<span data-ttu-id="28849-103">Hämtar information från en eller flera virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="28849-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="28849-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28849-104">SYNTAX</span></span>

### <span data-ttu-id="28849-105">ListAllVMs (standard)</span><span class="sxs-lookup"><span data-stu-id="28849-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="28849-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="28849-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="28849-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28849-107">DESCRIPTION</span></span>
<span data-ttu-id="28849-108">Cmdleten **Get-AzureVM** hämtar information om virtuella datorer som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="28849-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="28849-109">Den returnerar ett objekt med information om en specifik virtuell dator, eller om ingen virtuell dator har angetts, för alla virtuella datorer i den aktuella prenumerationens tjänst.</span><span class="sxs-lookup"><span data-stu-id="28849-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="28849-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28849-110">EXAMPLES</span></span>

### <span data-ttu-id="28849-111">Exempel 1: Hämta information på en angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="28849-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="28849-112">Det här kommandot returnerar ett objekt med information om den virtuella VirtualMachine02-datorn som körs i ContosoService01-moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="28849-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="28849-113">Exempel 2: Hämta information på alla virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="28849-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="28849-114">Det här kommandot hämtar ett List objekt med information om alla virtuella datorer som körs i ContosoService01-moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="28849-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="28849-115">Exempel 3: Visa en tabell med status för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="28849-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="28849-116">Det här kommandot visar en tabell som visar de virtuella datorerna som körs på ContosoService01-tjänsten, deras uppgraderings domän och aktuell status för varje virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="28849-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="28849-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28849-117">PARAMETERS</span></span>

### <span data-ttu-id="28849-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="28849-118">-InformationAction</span></span>
<span data-ttu-id="28849-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="28849-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28849-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="28849-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28849-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="28849-121">Continue</span></span>
- <span data-ttu-id="28849-122">Över</span><span class="sxs-lookup"><span data-stu-id="28849-122">Ignore</span></span>
- <span data-ttu-id="28849-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="28849-123">Inquire</span></span>
- <span data-ttu-id="28849-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="28849-124">SilentlyContinue</span></span>
- <span data-ttu-id="28849-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="28849-125">Stop</span></span>
- <span data-ttu-id="28849-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="28849-126">Suspend</span></span>

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

### <span data-ttu-id="28849-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="28849-127">-InformationVariable</span></span>
<span data-ttu-id="28849-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="28849-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28849-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="28849-129">-Name</span></span>
<span data-ttu-id="28849-130">Anger namnet på den virtuella dator som du vill hämta information för.</span><span class="sxs-lookup"><span data-stu-id="28849-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="28849-131">Om den här parametern inte anges returnerar cmdleten ett List objekt med information om alla virtuella datorer i den angivna tjänsten.</span><span class="sxs-lookup"><span data-stu-id="28849-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28849-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="28849-132">-Profile</span></span>
<span data-ttu-id="28849-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="28849-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28849-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="28849-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28849-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28849-135">-ServiceName</span></span>
<span data-ttu-id="28849-136">Anger namnet på den moln tjänst där information om virtuell dator ska returneras.</span><span class="sxs-lookup"><span data-stu-id="28849-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28849-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28849-137">CommonParameters</span></span>
<span data-ttu-id="28849-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28849-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28849-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28849-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28849-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28849-140">INPUTS</span></span>

## <span data-ttu-id="28849-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28849-141">OUTPUTS</span></span>

## <span data-ttu-id="28849-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28849-142">NOTES</span></span>

## <span data-ttu-id="28849-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28849-143">RELATED LINKS</span></span>

[<span data-ttu-id="28849-144">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="28849-145">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="28849-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="28849-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="28849-147">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="28849-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="28849-149">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="28849-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28849-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


