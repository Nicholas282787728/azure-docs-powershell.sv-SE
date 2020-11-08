---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099430"
---
# <span data-ttu-id="ea087-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ea087-101">New-AzureVM</span></span>

## <span data-ttu-id="ea087-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea087-102">SYNOPSIS</span></span>
<span data-ttu-id="ea087-103">Skapar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ea087-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="ea087-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea087-104">SYNTAX</span></span>

### <span data-ttu-id="ea087-105">ExistingService (standard)</span><span class="sxs-lookup"><span data-stu-id="ea087-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea087-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="ea087-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea087-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea087-107">DESCRIPTION</span></span>
<span data-ttu-id="ea087-108">Cmdleten **New-AzureVM** lägger till en ny virtuell dator i en befintlig Azure-tjänst eller skapar en virtuell dator och tjänst i det aktuella abonnemanget om antingen *location* eller *AffinityGroup* har angetts.</span><span class="sxs-lookup"><span data-stu-id="ea087-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="ea087-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea087-109">EXAMPLES</span></span>

### <span data-ttu-id="ea087-110">Exempel 1: skapa en virtuell dator för en Windows-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ea087-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="ea087-111">Det här kommandot skapar en konfiguration för etableringen baserat på en virtuell dator konfiguration för operativ systemet Windows och använder den för att skapa en virtuell dator i en angiven tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="ea087-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="ea087-112">Exempel 2: skapa en virtuell dator för en Linux-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ea087-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="ea087-113">Det här kommandot skapar en konfiguration för etableringen baserat på en virtuell dator konfiguration för Linux och använder den för att skapa en virtuell dator i en angiven tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="ea087-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="ea087-114">Exempel 3: skapa en virtuell dator och lägga till en data skiva</span><span class="sxs-lookup"><span data-stu-id="ea087-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="ea087-115">De första två kommandona får tillgängliga bilder med cmdleten **Get-AzureVMImage** och lagrar en av dem i variabeln $image.</span><span class="sxs-lookup"><span data-stu-id="ea087-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="ea087-116">Det här kommandot skapar en konfiguration för etableringen baserat på en virtuell dator konfiguration för operativ systemet Windows och använder den för att skapa en virtuell dator med en Azure data-disk.</span><span class="sxs-lookup"><span data-stu-id="ea087-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="ea087-117">Exempel 4: skapa en virtuell dator med en reserverad IP-adress</span><span class="sxs-lookup"><span data-stu-id="ea087-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="ea087-118">Det här kommandot skapar en konfiguration för etableringen baserat på en virtuell dator konfiguration för operativ systemet Windows och använder den för att skapa en virtuell dator med en reserverad IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ea087-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="ea087-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea087-119">PARAMETERS</span></span>

### <span data-ttu-id="ea087-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ea087-120">-AffinityGroup</span></span>
<span data-ttu-id="ea087-121">Anger den Azure Affinity-grupp som moln tjänsten finns i.</span><span class="sxs-lookup"><span data-stu-id="ea087-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="ea087-122">Den här parametern är endast nödvändig när denna cmdlet skapar en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="ea087-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="ea087-123">-DeploymentLabel</span></span>
<span data-ttu-id="ea087-124">Anger en etikett för distributionen.</span><span class="sxs-lookup"><span data-stu-id="ea087-124">Specifies a label for the deployment.</span></span>

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

### <span data-ttu-id="ea087-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ea087-125">-DeploymentName</span></span>
<span data-ttu-id="ea087-126">Anger ett distributions namn.</span><span class="sxs-lookup"><span data-stu-id="ea087-126">Specifies a deployment name.</span></span>
<span data-ttu-id="ea087-127">Om det inte anges använder denna cmdlet tjänst namnet som distributions namn.</span><span class="sxs-lookup"><span data-stu-id="ea087-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

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

### <span data-ttu-id="ea087-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="ea087-128">-DnsSettings</span></span>
<span data-ttu-id="ea087-129">Anger ett DNS-serverobjektet som definierar DNS-inställningarna för den nya distributionen.</span><span class="sxs-lookup"><span data-stu-id="ea087-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea087-130">-InformationAction</span></span>
<span data-ttu-id="ea087-131">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ea087-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea087-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ea087-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea087-133">Vidare</span><span class="sxs-lookup"><span data-stu-id="ea087-133">Continue</span></span>
- <span data-ttu-id="ea087-134">Över</span><span class="sxs-lookup"><span data-stu-id="ea087-134">Ignore</span></span>
- <span data-ttu-id="ea087-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea087-135">Inquire</span></span>
- <span data-ttu-id="ea087-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea087-136">SilentlyContinue</span></span>
- <span data-ttu-id="ea087-137">Stanna</span><span class="sxs-lookup"><span data-stu-id="ea087-137">Stop</span></span>
- <span data-ttu-id="ea087-138">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ea087-138">Suspend</span></span>

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

### <span data-ttu-id="ea087-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea087-139">-InformationVariable</span></span>
<span data-ttu-id="ea087-140">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ea087-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea087-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="ea087-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="ea087-142">Anger en intern belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="ea087-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="ea087-143">Denna parameter används inte.</span><span class="sxs-lookup"><span data-stu-id="ea087-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="ea087-144">-Location</span></span>
<span data-ttu-id="ea087-145">Anger platsen som är värd för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ea087-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="ea087-146">Ange inte den här parametern om tjänsten redan finns.</span><span class="sxs-lookup"><span data-stu-id="ea087-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="ea087-147">-Profile</span></span>
<span data-ttu-id="ea087-148">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ea087-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea087-149">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ea087-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea087-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="ea087-150">-ReservedIPName</span></span>
<span data-ttu-id="ea087-151">Anger namnet på den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="ea087-151">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="ea087-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="ea087-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="ea087-153">Anger det fullständigt kvalificerade domän namnet för omvänd DNS.</span><span class="sxs-lookup"><span data-stu-id="ea087-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ea087-154">-ServiceDescription</span></span>
<span data-ttu-id="ea087-155">Anger en beskrivning för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ea087-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="ea087-156">-ServiceLabel</span></span>
<span data-ttu-id="ea087-157">Anger en etikett för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ea087-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ea087-158">-ServiceName</span></span>
<span data-ttu-id="ea087-159">Anger det nya eller befintliga tjänst namnet.</span><span class="sxs-lookup"><span data-stu-id="ea087-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="ea087-160">Om tjänsten inte finns skapar den här cmdlet den för dig.</span><span class="sxs-lookup"><span data-stu-id="ea087-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="ea087-161">Använd parametern *location* eller *AffinityGroup* för att ange var tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ea087-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="ea087-162">Om tjänsten finns behövs inte parametern *location* eller *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="ea087-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-163">-VMs</span><span class="sxs-lookup"><span data-stu-id="ea087-163">-VMs</span></span>
<span data-ttu-id="ea087-164">Anger en lista över virtuella dator objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ea087-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea087-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ea087-165">-VNetName</span></span>
<span data-ttu-id="ea087-166">Anger det virtuella nätverks namnet där den här cmdleten distribuerar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea087-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

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

### <span data-ttu-id="ea087-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="ea087-167">-WaitForBoot</span></span>
<span data-ttu-id="ea087-168">Anger att denna cmdlet väntar på att den virtuella datorn ska nå **ReadyRole** -tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ea087-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="ea087-169">Denna cmdlet fungerar inte om den virtuella datorn ingår i något av följande lägen när du väntar: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="ea087-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="ea087-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea087-170">CommonParameters</span></span>
<span data-ttu-id="ea087-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea087-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea087-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea087-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea087-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea087-173">INPUTS</span></span>

## <span data-ttu-id="ea087-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea087-174">OUTPUTS</span></span>

## <span data-ttu-id="ea087-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea087-175">NOTES</span></span>

## <span data-ttu-id="ea087-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea087-176">RELATED LINKS</span></span>

[<span data-ttu-id="ea087-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ea087-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="ea087-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="ea087-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="ea087-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ea087-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="ea087-180">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea087-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


