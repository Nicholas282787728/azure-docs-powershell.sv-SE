---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099243"
---
# <span data-ttu-id="ade8a-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-101">Update-AzureVM</span></span>

## <span data-ttu-id="ade8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ade8a-102">SYNOPSIS</span></span>
<span data-ttu-id="ade8a-103">Ändrar konfigurationen för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ade8a-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="ade8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ade8a-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ade8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ade8a-105">DESCRIPTION</span></span>
<span data-ttu-id="ade8a-106">Cmdleten **Update-AzureVM** accepterar uppdaterings information för angiven virtuell dator och initierar uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="ade8a-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="ade8a-107">Du kan lägga till och ta bort data diskar, ändra cacheläge för data eller operativ system diskar, ändra nätverks slut punkter eller ändra storleken på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ade8a-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="ade8a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ade8a-108">EXAMPLES</span></span>

### <span data-ttu-id="ade8a-109">Exempel 1: uppdatera storleken på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ade8a-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="ade8a-110">Det här kommandot ändrar storleken på den virtuella datorn med namnet VirtualMachine04, som körs i tjänsten ContosoService03, till medel.</span><span class="sxs-lookup"><span data-stu-id="ade8a-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="ade8a-111">Exempel 2: lägga till en datadisk på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ade8a-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="ade8a-112">Det här kommandot lägger till en ny datadisk till den virtuella datorn med namnet VirtualMachine05, som körs i tjänsten ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="ade8a-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="ade8a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ade8a-113">PARAMETERS</span></span>

### <span data-ttu-id="ade8a-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ade8a-114">-InformationAction</span></span>
<span data-ttu-id="ade8a-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ade8a-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ade8a-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ade8a-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ade8a-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="ade8a-117">Continue</span></span>
- <span data-ttu-id="ade8a-118">Över</span><span class="sxs-lookup"><span data-stu-id="ade8a-118">Ignore</span></span>
- <span data-ttu-id="ade8a-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="ade8a-119">Inquire</span></span>
- <span data-ttu-id="ade8a-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ade8a-120">SilentlyContinue</span></span>
- <span data-ttu-id="ade8a-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="ade8a-121">Stop</span></span>
- <span data-ttu-id="ade8a-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ade8a-122">Suspend</span></span>

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

### <span data-ttu-id="ade8a-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ade8a-123">-InformationVariable</span></span>
<span data-ttu-id="ade8a-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ade8a-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ade8a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ade8a-125">-Name</span></span>
<span data-ttu-id="ade8a-126">Anger namnet på den virtuella dator som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ade8a-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="ade8a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="ade8a-127">-Profile</span></span>
<span data-ttu-id="ade8a-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ade8a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ade8a-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ade8a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ade8a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ade8a-130">-ServiceName</span></span>
<span data-ttu-id="ade8a-131">Anger namnet på Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ade8a-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="ade8a-132">-VM</span><span class="sxs-lookup"><span data-stu-id="ade8a-132">-VM</span></span>
<span data-ttu-id="ade8a-133">Anger det virtuella dator objekt som innehåller uppdaterade inställningar.</span><span class="sxs-lookup"><span data-stu-id="ade8a-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ade8a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade8a-134">CommonParameters</span></span>
<span data-ttu-id="ade8a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade8a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade8a-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade8a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade8a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ade8a-137">INPUTS</span></span>

## <span data-ttu-id="ade8a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ade8a-138">OUTPUTS</span></span>

## <span data-ttu-id="ade8a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ade8a-139">NOTES</span></span>

## <span data-ttu-id="ade8a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ade8a-140">RELATED LINKS</span></span>

[<span data-ttu-id="ade8a-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ade8a-142">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ade8a-143">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ade8a-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ade8a-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="ade8a-145">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ade8a-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="ade8a-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="ade8a-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="ade8a-148">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade8a-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


