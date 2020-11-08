---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099427"
---
# <span data-ttu-id="7e846-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="7e846-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="7e846-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e846-102">SYNOPSIS</span></span>
<span data-ttu-id="7e846-103">Skapar ett konfigurations objekt för Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="7e846-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="7e846-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e846-104">SYNTAX</span></span>

### <span data-ttu-id="7e846-105">ImageName (standard)</span><span class="sxs-lookup"><span data-stu-id="7e846-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e846-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="7e846-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7e846-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e846-107">DESCRIPTION</span></span>
<span data-ttu-id="7e846-108">Cmdleten **New-AzureVMConfig** skapar ett konfigurations objekt för Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="7e846-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="7e846-109">Du kan använda det här objektet för att utföra en ny distribution och lägga till en ny virtuell dator i en befintlig distribution.</span><span class="sxs-lookup"><span data-stu-id="7e846-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="7e846-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e846-110">EXAMPLES</span></span>

### <span data-ttu-id="7e846-111">Exempel 1: skapa en konfiguration för en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="7e846-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="7e846-112">Det här kommandot skapar en konfiguration för Windows virtuell dator med operativ system disk, data disk och konfiguration av etableringen.</span><span class="sxs-lookup"><span data-stu-id="7e846-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="7e846-113">Denna konfiguration används sedan för att skapa en ny virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7e846-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="7e846-114">Exempel 2: skapa en konfiguration för virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="7e846-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="7e846-115">Det här kommandot skapar en ny konfiguration för virtuella Linux-datorer med operativ system disk, data disk och konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7e846-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="7e846-116">Denna konfiguration används sedan för att skapa en ny virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7e846-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="7e846-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e846-117">PARAMETERS</span></span>

### <span data-ttu-id="7e846-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="7e846-118">-AvailabilitySetName</span></span>
<span data-ttu-id="7e846-119">Anger namnet på tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7e846-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7e846-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="7e846-121">Anger att konfigurationen inaktiverar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="7e846-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="7e846-122">Standardinställningen är att startdiagnostik är aktive rad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7e846-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="7e846-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="7e846-123">-DiskLabel</span></span>
<span data-ttu-id="7e846-124">Anger en etikett för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7e846-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7e846-125">-DiskName</span></span>
<span data-ttu-id="7e846-126">Anger ett namn för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7e846-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="7e846-127">-HostCaching</span></span>
<span data-ttu-id="7e846-128">Anger läget för cachelagring av värden för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7e846-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="7e846-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7e846-129">Valid values are:</span></span>

- <span data-ttu-id="7e846-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7e846-130">ReadOnly</span></span>
- <span data-ttu-id="7e846-131">Läs</span><span class="sxs-lookup"><span data-stu-id="7e846-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7e846-132">-ImageName</span></span>
<span data-ttu-id="7e846-133">Anger namnet på den virtuella dator avbildning som ska användas för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7e846-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7e846-134">-InformationAction</span></span>
<span data-ttu-id="7e846-135">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="7e846-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e846-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7e846-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e846-137">Vidare</span><span class="sxs-lookup"><span data-stu-id="7e846-137">Continue</span></span>
- <span data-ttu-id="7e846-138">Över</span><span class="sxs-lookup"><span data-stu-id="7e846-138">Ignore</span></span>
- <span data-ttu-id="7e846-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="7e846-139">Inquire</span></span>
- <span data-ttu-id="7e846-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7e846-140">SilentlyContinue</span></span>
- <span data-ttu-id="7e846-141">Stanna</span><span class="sxs-lookup"><span data-stu-id="7e846-141">Stop</span></span>
- <span data-ttu-id="7e846-142">Avbryt</span><span class="sxs-lookup"><span data-stu-id="7e846-142">Suspend</span></span>

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

### <span data-ttu-id="7e846-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7e846-143">-InformationVariable</span></span>
<span data-ttu-id="7e846-144">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="7e846-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e846-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="7e846-145">-InstanceSize</span></span>
<span data-ttu-id="7e846-146">Anger förekomstens storlek.</span><span class="sxs-lookup"><span data-stu-id="7e846-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="7e846-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7e846-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e846-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="7e846-148">ExtraSmall</span></span>
- <span data-ttu-id="7e846-149">Eld</span><span class="sxs-lookup"><span data-stu-id="7e846-149">Small</span></span>
- <span data-ttu-id="7e846-150">Risk</span><span class="sxs-lookup"><span data-stu-id="7e846-150">Medium</span></span>
- <span data-ttu-id="7e846-151">Höga</span><span class="sxs-lookup"><span data-stu-id="7e846-151">Large</span></span>
- <span data-ttu-id="7e846-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="7e846-152">ExtraLarge</span></span>
- <span data-ttu-id="7e846-153">A5</span><span class="sxs-lookup"><span data-stu-id="7e846-153">A5</span></span>
- <span data-ttu-id="7e846-154">A6</span><span class="sxs-lookup"><span data-stu-id="7e846-154">A6</span></span>
- <span data-ttu-id="7e846-155">A7</span><span class="sxs-lookup"><span data-stu-id="7e846-155">A7</span></span>
- <span data-ttu-id="7e846-156">A8</span><span class="sxs-lookup"><span data-stu-id="7e846-156">A8</span></span>
- <span data-ttu-id="7e846-157">A9</span><span class="sxs-lookup"><span data-stu-id="7e846-157">A9</span></span>
- <span data-ttu-id="7e846-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="7e846-158">Basic_A0</span></span>
- <span data-ttu-id="7e846-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="7e846-159">Basic_A1</span></span>
- <span data-ttu-id="7e846-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="7e846-160">Basic_A2</span></span>
- <span data-ttu-id="7e846-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="7e846-161">Basic_A3</span></span>
- <span data-ttu-id="7e846-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="7e846-162">Basic_A4</span></span>
- <span data-ttu-id="7e846-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="7e846-163">Standard_D1</span></span>
- <span data-ttu-id="7e846-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="7e846-164">Standard_D2</span></span>
- <span data-ttu-id="7e846-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="7e846-165">Standard_D3</span></span>
- <span data-ttu-id="7e846-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="7e846-166">Standard_D4</span></span>
- <span data-ttu-id="7e846-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="7e846-167">Standard_D11</span></span>
- <span data-ttu-id="7e846-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="7e846-168">Standard_D12</span></span>
- <span data-ttu-id="7e846-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="7e846-169">Standard_D13</span></span>
- <span data-ttu-id="7e846-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="7e846-170">Standard_D14</span></span>

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

### <span data-ttu-id="7e846-171">-Etikett</span><span class="sxs-lookup"><span data-stu-id="7e846-171">-Label</span></span>
<span data-ttu-id="7e846-172">Anger en etikett som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7e846-172">Specifies a label to assign to the virtual machine.</span></span>

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

### <span data-ttu-id="7e846-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7e846-173">-LicenseType</span></span>
<span data-ttu-id="7e846-174">Anger licens typen för en bild eller disk som är licensierad lokalt.</span><span class="sxs-lookup"><span data-stu-id="7e846-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="7e846-175">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7e846-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e846-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="7e846-176">Windows_Client</span></span>
- <span data-ttu-id="7e846-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="7e846-177">Windows_Server</span></span> 

<span data-ttu-id="7e846-178">Ange endast den här parametern för bilder som innehåller operativ systemet Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7e846-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="7e846-179">-MediaLocation</span></span>
<span data-ttu-id="7e846-180">Anger Azure Storage-platsen för den nya virtuella dator disken.</span><span class="sxs-lookup"><span data-stu-id="7e846-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e846-181">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e846-181">-Name</span></span>
<span data-ttu-id="7e846-182">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7e846-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7e846-183">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e846-183">-Profile</span></span>
<span data-ttu-id="7e846-184">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7e846-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e846-185">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7e846-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e846-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e846-186">CommonParameters</span></span>
<span data-ttu-id="7e846-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e846-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e846-188">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e846-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e846-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e846-189">INPUTS</span></span>

## <span data-ttu-id="7e846-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e846-190">OUTPUTS</span></span>

## <span data-ttu-id="7e846-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e846-191">NOTES</span></span>

## <span data-ttu-id="7e846-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e846-192">RELATED LINKS</span></span>

