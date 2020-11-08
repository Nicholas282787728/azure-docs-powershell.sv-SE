---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093377"
---
# <span data-ttu-id="54106-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54106-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="54106-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54106-102">SYNOPSIS</span></span>
<span data-ttu-id="54106-103">Hämtar Azure data-diskar.</span><span class="sxs-lookup"><span data-stu-id="54106-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="54106-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54106-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54106-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54106-105">DESCRIPTION</span></span>
<span data-ttu-id="54106-106">Cmdleten **Get-AzureDataDisk** hämtar ett objekt som representerar data diskarna på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="54106-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="54106-107">Om du vill hämta ett specifikt data disk objekt anger du diskens logiska enhets nummer (LUN).</span><span class="sxs-lookup"><span data-stu-id="54106-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="54106-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54106-108">EXAMPLES</span></span>

### <span data-ttu-id="54106-109">Exempel 1: Hämta alla data diskar för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="54106-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="54106-110">Det här kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="54106-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="54106-111">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="54106-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54106-112">Den aktuella cmdleten får alla data diskar för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="54106-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="54106-113">Exempel 2: Hämta en särskild data disk för en vituralvirtual machinevirtual</span><span class="sxs-lookup"><span data-stu-id="54106-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="54106-114">Det här kommandot får den virtuella datorn med namnet VirtualMachine07 i tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="54106-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="54106-115">Kommandot skickar den virtuella datorn till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54106-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="54106-116">Den aktuella cmdleten får den data disk som har LUN 2.</span><span class="sxs-lookup"><span data-stu-id="54106-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="54106-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54106-117">PARAMETERS</span></span>

### <span data-ttu-id="54106-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="54106-118">-InformationAction</span></span>
<span data-ttu-id="54106-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="54106-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54106-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="54106-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54106-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="54106-121">Continue</span></span>
- <span data-ttu-id="54106-122">Över</span><span class="sxs-lookup"><span data-stu-id="54106-122">Ignore</span></span>
- <span data-ttu-id="54106-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="54106-123">Inquire</span></span>
- <span data-ttu-id="54106-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="54106-124">SilentlyContinue</span></span>
- <span data-ttu-id="54106-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="54106-125">Stop</span></span>
- <span data-ttu-id="54106-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="54106-126">Suspend</span></span>

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

### <span data-ttu-id="54106-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="54106-127">-InformationVariable</span></span>
<span data-ttu-id="54106-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="54106-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="54106-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="54106-129">-Lun</span></span>
<span data-ttu-id="54106-130">Anger LUN för data enheten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="54106-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="54106-131">Giltiga värden är: 0 till 15.</span><span class="sxs-lookup"><span data-stu-id="54106-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54106-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="54106-132">-Profile</span></span>
<span data-ttu-id="54106-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="54106-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54106-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="54106-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54106-135">-VM</span><span class="sxs-lookup"><span data-stu-id="54106-135">-VM</span></span>
<span data-ttu-id="54106-136">Anger det virtuella datorobjektet för vilket denna cmdlet hämtar data diskar.</span><span class="sxs-lookup"><span data-stu-id="54106-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="54106-137">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="54106-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="54106-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54106-138">CommonParameters</span></span>
<span data-ttu-id="54106-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54106-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54106-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54106-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54106-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54106-141">INPUTS</span></span>

## <span data-ttu-id="54106-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54106-142">OUTPUTS</span></span>

## <span data-ttu-id="54106-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54106-143">NOTES</span></span>

## <span data-ttu-id="54106-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54106-144">RELATED LINKS</span></span>

[<span data-ttu-id="54106-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54106-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="54106-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="54106-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="54106-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54106-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="54106-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54106-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


