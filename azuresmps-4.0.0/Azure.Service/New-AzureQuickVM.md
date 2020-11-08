---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099139"
---
# <span data-ttu-id="4b7bb-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="4b7bb-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="4b7bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7bb-103">Konfigurerar och skapar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="4b7bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b7bb-104">SYNTAX</span></span>

### <span data-ttu-id="4b7bb-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="4b7bb-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4b7bb-106">Linux</span><span class="sxs-lookup"><span data-stu-id="4b7bb-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4b7bb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b7bb-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7bb-108">**New-AzureQuickVM** cmdlet konfigurerar och skapar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="4b7bb-109">Denna cmdlet kan distribuera en virtuell dator till en befintlig Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="4b7bb-110">Denna cmdlet kan alternativt skapa en Azure-tjänst som är värd för den nya virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="4b7bb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b7bb-111">EXAMPLES</span></span>

### <span data-ttu-id="4b7bb-112">Exempel 1: skapa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4b7bb-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="4b7bb-113">Det här kommandot skapar en virtuell dator som kör operativ systemet Windows i en befintlig tjänst.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="4b7bb-114">Cmdleten baserar den virtuella datorn på den angivna bilden.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="4b7bb-115">Kommandot anger parametern *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="4b7bb-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="4b7bb-116">Därför väntar cmdleten på att den virtuella datorn ska starta.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="4b7bb-117">Exempel 2: skapa en virtuell dator som använder certifikat</span><span class="sxs-lookup"><span data-stu-id="4b7bb-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="4b7bb-118">Det första kommandot får certifikat från en butik och lagrar dem i $certs variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="4b7bb-119">Det andra kommandot skapar en virtuell dator som kör operativ systemet Windows i en befintlig tjänst från en bild.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="4b7bb-120">Http https-lyssnaren är aktive rad som standard på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="4b7bb-121">Kommandot anger parametern *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="4b7bb-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="4b7bb-122">Därför väntar cmdleten på att den virtuella datorn ska starta.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="4b7bb-123">Kommandot laddar upp ett WinRM-certifikat och X509Certificates till den värdbaserade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="4b7bb-124">Exempel 3: skapa en virtuell dator som kör Linux-operativsystemet</span><span class="sxs-lookup"><span data-stu-id="4b7bb-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="4b7bb-125">Det här kommandot skapar en virtuell dator som kör Linux-operativsystemet från en bild.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="4b7bb-126">Det här kommandot skapar en tjänst som ska vara värd för den nya virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="4b7bb-127">Kommandot anger en plats för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="4b7bb-128">Exempel 4: skapa en virtuell dator och skapa en tjänst som värd för den nya virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="4b7bb-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="4b7bb-129">Det första kommandot får plats genom att använda cmdleten **Get-AzureLocation** och lagrar dem sedan i $locations mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="4b7bb-130">Med det andra kommandot hämtas tillgängliga bilder med cmdleten **Get-AzureVMImage** och sparas sedan i $images mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="4b7bb-131">Med kommandot slut skapas en stor virtuell dator med namnet VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="4b7bb-132">Den virtuella datorn kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="4b7bb-133">Den är baserad på en av bilderna i $Images.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="4b7bb-134">Kommandot skapar en tjänst med namnet ContosoService03 för den nya virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="4b7bb-135">Tjänsten är på en plats i $Locations.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="4b7bb-136">Exempel 5: skapa en virtuell dator som har ett reserverat IP-namn</span><span class="sxs-lookup"><span data-stu-id="4b7bb-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="4b7bb-137">Det första kommandot får plats och lagrar dem sedan i $Locations mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="4b7bb-138">Det andra kommandot hämtar tillgängliga bilder och lagrar dem sedan i $Images mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="4b7bb-139">Med kommandot slut skapas en virtuell dator med namnet VirtualMachine27 baserat på en av bilderna i $Images.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="4b7bb-140">Kommandot skapar en tjänst på en plats i $Locations.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="4b7bb-141">Den virtuella datorn har ett reserverat IP-namn som tidigare lagrats i $ipName variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="4b7bb-142">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b7bb-142">PARAMETERS</span></span>

### <span data-ttu-id="4b7bb-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="4b7bb-143">-AdminUsername</span></span>
<span data-ttu-id="4b7bb-144">Anger användar namnet på det administratörs konto som den här cmdleten skapar på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4b7bb-145">-AffinityGroup</span></span>
<span data-ttu-id="4b7bb-146">Anger tillhörighets gruppen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="4b7bb-147">Ange den här parametern eller parametern *plats* om den här cmdleten skapar en Azure-tjänst för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="4b7bb-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="4b7bb-148">-AvailabilitySetName</span></span>
<span data-ttu-id="4b7bb-149">Anger namnet på den tillgänglighets uppsättning där den här cmdleten skapar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="4b7bb-150">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="4b7bb-150">-Certificates</span></span>
<span data-ttu-id="4b7bb-151">Anger en lista över de certifikat som används i den här cmdleten för att skapa tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="4b7bb-152">-CustomDataFile</span></span>
<span data-ttu-id="4b7bb-153">Anger en datafil för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="4b7bb-154">Denna cmdlet kodar innehållet i filen som base64.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="4b7bb-155">Filen måste vara mindre än 64 kilobyte lång.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="4b7bb-156">Om gäst operativ systemet är Windows-operativsystem sparar denna cmdlet dessa data som en binärfil som heter%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="4b7bb-157">Om gäst operativ systemet är Linux skickar denna cmdlet data med hjälp av ovf-env.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="4b7bb-158">Installationen kopierar filen till/var/lib/waagent-katalogen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="4b7bb-159">Agenten lagrar också base64-kodade data i/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="4b7bb-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="4b7bb-160">-DisableGuestAgent</span></span>
<span data-ttu-id="4b7bb-161">Anger att denna cmdlet inaktiverar infrastrukturen som en tjänst (IaaS).</span><span class="sxs-lookup"><span data-stu-id="4b7bb-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="4b7bb-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="4b7bb-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="4b7bb-163">Anger att denna cmdlet inaktiverar Windows Remote Management (WinRM) på HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="4b7bb-164">WinRM är aktiverat som standard via HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="4b7bb-165">-DnsSettings</span></span>
<span data-ttu-id="4b7bb-166">Anger en matris med DNS-Server objekt som definierar DNS-inställningarna för den nya distributionen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="4b7bb-167">Om du vill skapa ett **DnsServer** -objekt använder du cmdleten **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="4b7bb-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="4b7bb-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="4b7bb-169">Anger att denna cmdlet aktiverar WinRM över HTTP.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="4b7bb-170">-HostCaching</span></span>
<span data-ttu-id="4b7bb-171">Anger läget för cachelagring av värden för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="4b7bb-172">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4b7bb-172">Valid values are:</span></span> 

- <span data-ttu-id="4b7bb-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4b7bb-173">ReadOnly</span></span>
- <span data-ttu-id="4b7bb-174">Läs</span><span class="sxs-lookup"><span data-stu-id="4b7bb-174">ReadWrite</span></span>

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

### <span data-ttu-id="4b7bb-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4b7bb-175">-ImageName</span></span>
<span data-ttu-id="4b7bb-176">Anger namnet på den disk avbildning som används för att skapa disketten för operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4b7bb-177">-InformationAction</span></span>
<span data-ttu-id="4b7bb-178">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4b7bb-179">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4b7bb-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b7bb-180">Vidare</span><span class="sxs-lookup"><span data-stu-id="4b7bb-180">Continue</span></span>
- <span data-ttu-id="4b7bb-181">Över</span><span class="sxs-lookup"><span data-stu-id="4b7bb-181">Ignore</span></span>
- <span data-ttu-id="4b7bb-182">Inquire</span><span class="sxs-lookup"><span data-stu-id="4b7bb-182">Inquire</span></span>
- <span data-ttu-id="4b7bb-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4b7bb-183">SilentlyContinue</span></span>
- <span data-ttu-id="4b7bb-184">Stanna</span><span class="sxs-lookup"><span data-stu-id="4b7bb-184">Stop</span></span>
- <span data-ttu-id="4b7bb-185">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4b7bb-185">Suspend</span></span>

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

### <span data-ttu-id="4b7bb-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4b7bb-186">-InformationVariable</span></span>
<span data-ttu-id="4b7bb-187">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4b7bb-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="4b7bb-188">-InstanceSize</span></span>
<span data-ttu-id="4b7bb-189">Anger förekomstens storlek.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="4b7bb-190">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4b7bb-190">Valid values are:</span></span> 

- <span data-ttu-id="4b7bb-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="4b7bb-191">ExtraSmall</span></span>
- <span data-ttu-id="4b7bb-192">Eld</span><span class="sxs-lookup"><span data-stu-id="4b7bb-192">Small</span></span>
- <span data-ttu-id="4b7bb-193">Risk</span><span class="sxs-lookup"><span data-stu-id="4b7bb-193">Medium</span></span>
- <span data-ttu-id="4b7bb-194">Höga</span><span class="sxs-lookup"><span data-stu-id="4b7bb-194">Large</span></span>
- <span data-ttu-id="4b7bb-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="4b7bb-195">ExtraLarge</span></span>
- <span data-ttu-id="4b7bb-196">A5</span><span class="sxs-lookup"><span data-stu-id="4b7bb-196">A5</span></span>
- <span data-ttu-id="4b7bb-197">A6</span><span class="sxs-lookup"><span data-stu-id="4b7bb-197">A6</span></span>
- <span data-ttu-id="4b7bb-198">A7</span><span class="sxs-lookup"><span data-stu-id="4b7bb-198">A7</span></span>
- <span data-ttu-id="4b7bb-199">A8</span><span class="sxs-lookup"><span data-stu-id="4b7bb-199">A8</span></span>
- <span data-ttu-id="4b7bb-200">A9</span><span class="sxs-lookup"><span data-stu-id="4b7bb-200">A9</span></span>
- <span data-ttu-id="4b7bb-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="4b7bb-201">Basic_A0</span></span>
- <span data-ttu-id="4b7bb-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="4b7bb-202">Basic_A1</span></span>
- <span data-ttu-id="4b7bb-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="4b7bb-203">Basic_A2</span></span>
- <span data-ttu-id="4b7bb-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="4b7bb-204">Basic_A3</span></span>
- <span data-ttu-id="4b7bb-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="4b7bb-205">Basic_A4</span></span>
- <span data-ttu-id="4b7bb-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="4b7bb-206">Standard_D1</span></span>
- <span data-ttu-id="4b7bb-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="4b7bb-207">Standard_D2</span></span>
- <span data-ttu-id="4b7bb-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="4b7bb-208">Standard_D3</span></span>
- <span data-ttu-id="4b7bb-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="4b7bb-209">Standard_D4</span></span>
- <span data-ttu-id="4b7bb-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="4b7bb-210">Standard_D11</span></span>
- <span data-ttu-id="4b7bb-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="4b7bb-211">Standard_D12</span></span>
- <span data-ttu-id="4b7bb-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="4b7bb-212">Standard_D13</span></span>
- <span data-ttu-id="4b7bb-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="4b7bb-213">Standard_D14</span></span>

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

### <span data-ttu-id="4b7bb-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="4b7bb-214">-Linux</span></span>
<span data-ttu-id="4b7bb-215">Anger att denna cmdlet skapar en Linux-baserad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="4b7bb-216">-LinuxUser</span></span>
<span data-ttu-id="4b7bb-217">Anger användar namnet på det administratörs konto för Linux som den här cmdleten skapar på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-218">-Plats</span><span class="sxs-lookup"><span data-stu-id="4b7bb-218">-Location</span></span>
<span data-ttu-id="4b7bb-219">Anger Azure-datacentret som är värd för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="4b7bb-220">Om du anger den här parametern skapar cmdleten en Azure-tjänst på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="4b7bb-221">Ange den här parametern eller parametern *AffinityGroup* endast om den här cmdleten skapar en Azure-tjänst för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="4b7bb-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="4b7bb-222">-MediaLocation</span></span>
<span data-ttu-id="4b7bb-223">Anger plats för Azure-lagring där den här cmdleten skapar diskarna för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="4b7bb-224">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b7bb-224">-Name</span></span>
<span data-ttu-id="4b7bb-225">Anger namnet på den virtuella dator som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4b7bb-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="4b7bb-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="4b7bb-227">Anger att den här konfigurationen inte laddar upp den privata knappen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b7bb-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="4b7bb-229">Anger att denna cmdlet inte lägger till en WinRM-slutpunkt för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-230">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="4b7bb-230">-Password</span></span>
<span data-ttu-id="4b7bb-231">Anger lösen ordet för administratörs kontot.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="4b7bb-232">-Profil</span><span class="sxs-lookup"><span data-stu-id="4b7bb-232">-Profile</span></span>
<span data-ttu-id="4b7bb-233">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b7bb-234">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b7bb-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="4b7bb-235">-ReservedIPName</span></span>
<span data-ttu-id="4b7bb-236">Anger det reserverade IP-namnet.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="4b7bb-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="4b7bb-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="4b7bb-238">Anger det fullständigt kvalificerade domän namnet för omvänd DNS-uppkoppling.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="4b7bb-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4b7bb-239">-ServiceName</span></span>
<span data-ttu-id="4b7bb-240">Anger namnet på en ny eller befintlig Azure-tjänst dit den här cmdleten lägger till den nya virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="4b7bb-241">Om du anger en ny tjänst skapar denna cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="4b7bb-242">För att skapa en ny tjänst måste du ange *plats* -eller *AffinityGroup* -parameter.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="4b7bb-243">Om du anger en befintlig tjänst ska du inte ange *plats* eller *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="4b7bb-244">-SSHKeyPairs</span></span>
<span data-ttu-id="4b7bb-245">Anger SSH-nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="4b7bb-246">-SSHPublicKeys</span></span>
<span data-ttu-id="4b7bb-247">Anger offentliga nycklar för SSH.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="4b7bb-248">-SubnetNames</span></span>
<span data-ttu-id="4b7bb-249">Anger en matris med namn på en nätmask för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4b7bb-250">-VNetName</span></span>
<span data-ttu-id="4b7bb-251">Anger namnet på ett virtuellt nätverk för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="4b7bb-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="4b7bb-252">-WaitForBoot</span></span>
<span data-ttu-id="4b7bb-253">Anger att denna cmdlet väntar på att den virtuella datorn ska nå tillståndet ReadyRole.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="4b7bb-254">Om den virtuella datorn uppfyller något av följande tillstånd Miss lyckas cmdleten: FailedStartingVM, ProvisioningFailed eller ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="4b7bb-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="4b7bb-255">-Windows</span></span>
<span data-ttu-id="4b7bb-256">Anger att den här cmdleten skapar en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="4b7bb-257">-WinRMCertificate</span></span>
<span data-ttu-id="4b7bb-258">Anger ett certifikat som denna cmdlet associerar till en WinRM-slut punkt.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="4b7bb-259">-X509Certificates</span></span>
<span data-ttu-id="4b7bb-260">Anger en matris med X509-certifikat som distribueras till en värdbaserad tjänst.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7bb-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7bb-261">CommonParameters</span></span>
<span data-ttu-id="4b7bb-262">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b7bb-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7bb-263">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b7bb-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7bb-264">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b7bb-264">INPUTS</span></span>

## <span data-ttu-id="4b7bb-265">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b7bb-265">OUTPUTS</span></span>

## <span data-ttu-id="4b7bb-266">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b7bb-266">NOTES</span></span>

## <span data-ttu-id="4b7bb-267">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b7bb-267">RELATED LINKS</span></span>

[<span data-ttu-id="4b7bb-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="4b7bb-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="4b7bb-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4b7bb-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="4b7bb-270">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4b7bb-270">New-AzureDns</span></span>](./New-AzureDns.md)


