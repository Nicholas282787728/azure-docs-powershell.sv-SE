---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099268"
---
# <span data-ttu-id="d2807-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2807-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d2807-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2807-102">SYNOPSIS</span></span>
<span data-ttu-id="d2807-103">Konfigurerar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2807-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d2807-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2807-104">SYNTAX</span></span>

### <span data-ttu-id="d2807-105">SetDiagnosticsExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="d2807-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d2807-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="d2807-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d2807-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2807-107">DESCRIPTION</span></span>
<span data-ttu-id="d2807-108">Cmdleten **set-AzureVMDiagnosticsExtension** konfigurerar Microsoft Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2807-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d2807-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2807-109">EXAMPLES</span></span>

### <span data-ttu-id="d2807-110">Exempel 1: skapa en virtuell dator med Azure Diagnostics-tillägget installerat</span><span class="sxs-lookup"><span data-stu-id="d2807-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="d2807-111">De här kommandona aktiverar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2807-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="d2807-112">Exempel 2: aktivera ett Azure Diagnostics-tillägg på en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d2807-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="d2807-113">Det första kommandot använder cmdleten **Get-AzureVM** för att hämta en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2807-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="d2807-114">Det andra kommandot använder cmdleten **set-AzureVMDiagnosticsExtension** för att uppdatera den virtuella dator konfigurationen så att den inkluderar Azure Diagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d2807-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="d2807-115">Det sista kommandot tillämpar den uppdaterade konfigurationen på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2807-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="d2807-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2807-116">PARAMETERS</span></span>

### <span data-ttu-id="d2807-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d2807-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d2807-118">Anger en sökväg för diagnostikverktyget.</span><span class="sxs-lookup"><span data-stu-id="d2807-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-119">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="d2807-119">-Disable</span></span>
<span data-ttu-id="d2807-120">Anger att denna cmdlet inaktiverar tillägget Diagnostics på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2807-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d2807-121">-InformationAction</span></span>
<span data-ttu-id="d2807-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d2807-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d2807-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d2807-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2807-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="d2807-124">Continue</span></span>
- <span data-ttu-id="d2807-125">Över</span><span class="sxs-lookup"><span data-stu-id="d2807-125">Ignore</span></span>
- <span data-ttu-id="d2807-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="d2807-126">Inquire</span></span>
- <span data-ttu-id="d2807-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d2807-127">SilentlyContinue</span></span>
- <span data-ttu-id="d2807-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="d2807-128">Stop</span></span>
- <span data-ttu-id="d2807-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d2807-129">Suspend</span></span>

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

### <span data-ttu-id="d2807-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d2807-130">-InformationVariable</span></span>
<span data-ttu-id="d2807-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d2807-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d2807-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2807-132">-Profile</span></span>
<span data-ttu-id="d2807-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d2807-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2807-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d2807-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2807-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="d2807-135">-ReferenceName</span></span>
<span data-ttu-id="d2807-136">Anger referens namnet för tillägget.</span><span class="sxs-lookup"><span data-stu-id="d2807-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2807-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d2807-138">Anger en slut punkt för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2807-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d2807-139">-StorageAccountKey</span></span>
<span data-ttu-id="d2807-140">Anger en lagrings konto profil.</span><span class="sxs-lookup"><span data-stu-id="d2807-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2807-141">-StorageAccountName</span></span>
<span data-ttu-id="d2807-142">Anger ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="d2807-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d2807-143">-StorageContext</span></span>
<span data-ttu-id="d2807-144">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="d2807-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-145">-Version</span><span class="sxs-lookup"><span data-stu-id="d2807-145">-Version</span></span>
<span data-ttu-id="d2807-146">Anger tilläggs versionen som en sträng.</span><span class="sxs-lookup"><span data-stu-id="d2807-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2807-147">-VM</span><span class="sxs-lookup"><span data-stu-id="d2807-147">-VM</span></span>
<span data-ttu-id="d2807-148">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="d2807-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d2807-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2807-149">CommonParameters</span></span>
<span data-ttu-id="d2807-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2807-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2807-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2807-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2807-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2807-152">INPUTS</span></span>

## <span data-ttu-id="d2807-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2807-153">OUTPUTS</span></span>

## <span data-ttu-id="d2807-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2807-154">NOTES</span></span>

## <span data-ttu-id="d2807-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2807-155">RELATED LINKS</span></span>

[<span data-ttu-id="d2807-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2807-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d2807-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2807-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d2807-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d2807-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


