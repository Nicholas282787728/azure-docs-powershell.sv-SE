---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099612"
---
# <span data-ttu-id="5740d-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="5740d-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="5740d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5740d-102">SYNOPSIS</span></span>
<span data-ttu-id="5740d-103">Lägger till etableringen-konfiguration för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="5740d-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="5740d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5740d-104">SYNTAX</span></span>

### <span data-ttu-id="5740d-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="5740d-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5740d-106">Linux</span><span class="sxs-lookup"><span data-stu-id="5740d-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5740d-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="5740d-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5740d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5740d-108">DESCRIPTION</span></span>
<span data-ttu-id="5740d-109">Cmdleten **Add-AzureProvisioningConfig** lägger till konfigurations information för etableringen i en konfiguration för en Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="5740d-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="5740d-110">Du kan använda konfigurationsobjektet för att skapa en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5740d-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="5740d-111">Denna cmdlet har stöd för olika konfigurations konfigurationer, inklusive fristående Windows-servrar, Windows-servrar som är anslutna till en Active Directory-domän och Linux-baserade servrar.</span><span class="sxs-lookup"><span data-stu-id="5740d-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="5740d-112">Om du vill skapa en server för Active Directory-anslutare anger du det fullständigt kvalificerade domän namnet för Active Directory-domänen och domänautentiseringsuppgifter för en användare som har behörighet att ansluta den virtuella datorn till domänen.</span><span class="sxs-lookup"><span data-stu-id="5740d-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="5740d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5740d-113">EXAMPLES</span></span>

### <span data-ttu-id="5740d-114">Exempel 1: skapa en fristående virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5740d-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5740d-115">Det här kommandot skapar ett konfigurations objekt för virtuell dator med hjälp av cmdleten **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="5740d-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="5740d-116">Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5740d-117">Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="5740d-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="5740d-118">Konfigurationen inkluderar administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="5740d-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="5740d-119">Kommandot överför konfigurationen till cmdleten **New-AzureVM** , som skapar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="5740d-120">Exempel 2: skapa en domänansluten virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5740d-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5740d-121">Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-122">Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som ska kopplas till domänen contoso.</span><span class="sxs-lookup"><span data-stu-id="5740d-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="5740d-123">Kommandot innehåller användar namn och lösen ord som krävs för att ansluta den virtuella datorn till domänen.</span><span class="sxs-lookup"><span data-stu-id="5740d-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="5740d-124">Konfigurationen kräver att användaren ändrar lösen ordet vid första inloggningen.</span><span class="sxs-lookup"><span data-stu-id="5740d-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="5740d-125">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5740d-126">Exempel 3: skapa en Linux-baserad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5740d-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5740d-127">Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-128">Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som kör Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="5740d-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="5740d-129">Konfigurationen inkluderar rot användar namnet och lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="5740d-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="5740d-130">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5740d-131">Exempel 4: skapa en virtuell dator som innehåller certifikat för WinRM</span><span class="sxs-lookup"><span data-stu-id="5740d-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5740d-132">Det första kommandot får certifikat från ett certifikat Arkiv och lagrar dem sedan i $certs mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="5740d-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="5740d-133">Det andra kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-134">Den aktuella cmdleten lägger till etableringen med konfiguration som inkluderar certifikat för WinRM.</span><span class="sxs-lookup"><span data-stu-id="5740d-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="5740d-135">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5740d-136">Exempel 5: skapa en virtuell dator med WinRM aktiverat över HTTP</span><span class="sxs-lookup"><span data-stu-id="5740d-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5740d-137">Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-138">Den aktuella cmdleten lägger till etableringen konfiguration med WinRM aktiverat över HTTP.</span><span class="sxs-lookup"><span data-stu-id="5740d-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="5740d-139">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5740d-140">Exempel 6: skapa en virtuell dator med WinRM inaktiverat över HTTPS</span><span class="sxs-lookup"><span data-stu-id="5740d-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5740d-141">Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-142">Den aktuella cmdleten lägger till etableringen-konfiguration som inaktiverar WinRM via HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5740d-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="5740d-143">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5740d-144">Exempel 7: skapa en virtuell dator utan att exportera nycklar</span><span class="sxs-lookup"><span data-stu-id="5740d-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5740d-145">Det första kommandot får certifikat från ett certifikat Arkiv och lagrar dem sedan i $certs mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="5740d-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="5740d-146">Det andra kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5740d-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5740d-147">Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som innehåller certifikat och exporterar inte privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="5740d-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="5740d-148">Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.</span><span class="sxs-lookup"><span data-stu-id="5740d-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="5740d-149">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5740d-149">PARAMETERS</span></span>

### <span data-ttu-id="5740d-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="5740d-150">-AdminUsername</span></span>
<span data-ttu-id="5740d-151">Anger användar namnet på det administratörs konto som den här konfigurationen skapar på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-152">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="5740d-152">-Certificates</span></span>
<span data-ttu-id="5740d-153">Anger en uppsättning certifikat som denna konfiguration installerar på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="5740d-154">-CustomDataFile</span></span>
<span data-ttu-id="5740d-155">Anger en datafil för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="5740d-156">Denna cmdlet kodar innehållet i filen som base64.</span><span class="sxs-lookup"><span data-stu-id="5740d-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="5740d-157">Filen måste vara mindre än 64 kilobyte lång.</span><span class="sxs-lookup"><span data-stu-id="5740d-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="5740d-158">Om gäst operativ systemet är Windows-operativsystemet sparas dessa data som en binär fil med namnet%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="5740d-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="5740d-159">Om gäst operativ systemet är Linux skickar denna konfiguration data med hjälp av ovf-env.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="5740d-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="5740d-160">Konfiguration kopierar filen till/var/lib/waagent-katalogen.</span><span class="sxs-lookup"><span data-stu-id="5740d-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="5740d-161">Agenten lagrar också base64-kodade data i/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="5740d-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="5740d-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="5740d-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="5740d-163">Anger att den här konfigurationen inaktiverar automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="5740d-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="5740d-164">-DisableGuestAgent</span></span>
<span data-ttu-id="5740d-165">Anger att den här konfigurationen inaktiverar infrastrukturen som en tjänst gäst agent (IaaS).</span><span class="sxs-lookup"><span data-stu-id="5740d-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="5740d-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="5740d-166">-DisableSSH</span></span>
<span data-ttu-id="5740d-167">Anger att den här konfigurationen inaktiverar SSH.</span><span class="sxs-lookup"><span data-stu-id="5740d-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="5740d-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="5740d-169">Anger att den här konfigurationen inaktiverar Windows Remote Management (WinRM) på HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5740d-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="5740d-170">WinRM är aktiverat som standard via HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5740d-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-171">-Domain</span><span class="sxs-lookup"><span data-stu-id="5740d-171">-Domain</span></span>
<span data-ttu-id="5740d-172">Anger namnet på domänen för det konto som har behörighet att lägga till datorn i en domän.</span><span class="sxs-lookup"><span data-stu-id="5740d-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="5740d-173">-DomainPassword</span></span>
<span data-ttu-id="5740d-174">Anger lösen ordet för det användar konto som har behörighet att lägga till datorn i en domän.</span><span class="sxs-lookup"><span data-stu-id="5740d-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="5740d-175">-DomainUserName</span></span>
<span data-ttu-id="5740d-176">Anger namnet på det användar konto som har behörighet att lägga till datorn i en domän.</span><span class="sxs-lookup"><span data-stu-id="5740d-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="5740d-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="5740d-178">Anger att den här konfigurationen aktiverar WinRM över HTTP.</span><span class="sxs-lookup"><span data-stu-id="5740d-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5740d-179">-InformationAction</span></span>
<span data-ttu-id="5740d-180">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="5740d-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5740d-181">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5740d-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5740d-182">Vidare</span><span class="sxs-lookup"><span data-stu-id="5740d-182">Continue</span></span>
- <span data-ttu-id="5740d-183">Över</span><span class="sxs-lookup"><span data-stu-id="5740d-183">Ignore</span></span>
- <span data-ttu-id="5740d-184">Inquire</span><span class="sxs-lookup"><span data-stu-id="5740d-184">Inquire</span></span>
- <span data-ttu-id="5740d-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5740d-185">SilentlyContinue</span></span>
- <span data-ttu-id="5740d-186">Stanna</span><span class="sxs-lookup"><span data-stu-id="5740d-186">Stop</span></span>
- <span data-ttu-id="5740d-187">Avbryt</span><span class="sxs-lookup"><span data-stu-id="5740d-187">Suspend</span></span>

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

### <span data-ttu-id="5740d-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5740d-188">-InformationVariable</span></span>
<span data-ttu-id="5740d-189">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="5740d-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5740d-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="5740d-190">-JoinDomain</span></span>
<span data-ttu-id="5740d-191">Anger det fullständigt kvalificerade domän namnet (FQDN) för domänen som ska anslutas.</span><span class="sxs-lookup"><span data-stu-id="5740d-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="5740d-192">-Linux</span></span>
<span data-ttu-id="5740d-193">Anger att den här konfigurationen skapar en Linux-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5740d-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="5740d-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="5740d-194">-LinuxUser</span></span>
<span data-ttu-id="5740d-195">Anger användar namnet på det administratörs konto för Linux som den här konfigurationen skapar på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="5740d-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="5740d-196">-MachineObjectOU</span></span>
<span data-ttu-id="5740d-197">Anger det fullständigt kvalificerade namnet på den organisatoriska enhet (OU) som konfigurationen skapar dator kontot i.</span><span class="sxs-lookup"><span data-stu-id="5740d-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="5740d-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="5740d-199">Anger att den här konfigurationen inte laddar upp den privata knappen.</span><span class="sxs-lookup"><span data-stu-id="5740d-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="5740d-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="5740d-201">Anger att den här konfigurationen skapar en virtuell dator utan slut punkt för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="5740d-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="5740d-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="5740d-203">Anger att den här konfigurationen skapar en virtuell dator utan en SSH-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5740d-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="5740d-204">-NoSSHPassword</span></span>
<span data-ttu-id="5740d-205">Anger att den här konfigurationen skapar en virtuell dator utan ett SSH-lösenord.</span><span class="sxs-lookup"><span data-stu-id="5740d-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="5740d-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="5740d-207">Anger att den här konfigurationen inte lägger till en WinRM-slutpunkt för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5740d-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-208">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="5740d-208">-Password</span></span>
<span data-ttu-id="5740d-209">Anger lösen ordet för administratörs kontot.</span><span class="sxs-lookup"><span data-stu-id="5740d-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="5740d-210">-Profil</span><span class="sxs-lookup"><span data-stu-id="5740d-210">-Profile</span></span>
<span data-ttu-id="5740d-211">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5740d-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5740d-212">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5740d-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5740d-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="5740d-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="5740d-214">Anger att den virtuella datorn kräver att användaren ändrar lösen ordet vid den första inloggningen.</span><span class="sxs-lookup"><span data-stu-id="5740d-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="5740d-215">-SSHKeyPairs</span></span>
<span data-ttu-id="5740d-216">Anger SSH-nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="5740d-216">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="5740d-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="5740d-217">-SSHPublicKeys</span></span>
<span data-ttu-id="5740d-218">Anger offentliga nycklar för SSH.</span><span class="sxs-lookup"><span data-stu-id="5740d-218">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="5740d-219">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5740d-219">-TimeZone</span></span>
<span data-ttu-id="5740d-220">Anger tids zonen för den virtuella datorn, till exempel Pacific standard time eller Canada Central, normal tid.</span><span class="sxs-lookup"><span data-stu-id="5740d-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-221">-VM</span><span class="sxs-lookup"><span data-stu-id="5740d-221">-VM</span></span>
<span data-ttu-id="5740d-222">Anger ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="5740d-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="5740d-223">-Windows</span></span>
<span data-ttu-id="5740d-224">Anger att den här konfigurationen skapar en fristående virtuell dator som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="5740d-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="5740d-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="5740d-225">-WindowsDomain</span></span>
<span data-ttu-id="5740d-226">Anger att den här konfigurationen skapar Windows Server som är ansluten till en Active Directory-domän.</span><span class="sxs-lookup"><span data-stu-id="5740d-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="5740d-227">-WinRMCertificate</span></span>
<span data-ttu-id="5740d-228">Anger ett certifikat som den här konfigurationen associeras med en WinRM-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5740d-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="5740d-229">-X509Certificates</span></span>
<span data-ttu-id="5740d-230">Anger en matris med X509-certifikat som distribueras till en värdbaserad tjänst.</span><span class="sxs-lookup"><span data-stu-id="5740d-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5740d-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5740d-231">CommonParameters</span></span>
<span data-ttu-id="5740d-232">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5740d-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5740d-233">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5740d-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5740d-234">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5740d-234">INPUTS</span></span>

## <span data-ttu-id="5740d-235">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5740d-235">OUTPUTS</span></span>

## <span data-ttu-id="5740d-236">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5740d-236">NOTES</span></span>

## <span data-ttu-id="5740d-237">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5740d-237">RELATED LINKS</span></span>

[<span data-ttu-id="5740d-238">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5740d-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5740d-239">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="5740d-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


