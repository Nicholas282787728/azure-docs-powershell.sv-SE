---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099275"
---
# <span data-ttu-id="7077f-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7077f-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="7077f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7077f-102">SYNOPSIS</span></span>
<span data-ttu-id="7077f-103">Lägger till filen kock till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7077f-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="7077f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7077f-104">SYNTAX</span></span>

### <span data-ttu-id="7077f-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="7077f-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7077f-106">Linux</span><span class="sxs-lookup"><span data-stu-id="7077f-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7077f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7077f-107">DESCRIPTION</span></span>
<span data-ttu-id="7077f-108">Cmdleten **set-AzureVMChefExtension** lägger till kock-tillägget till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7077f-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="7077f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7077f-109">EXAMPLES</span></span>

### <span data-ttu-id="7077f-110">Exempel 1: lägga till en kock-anknytning till en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="7077f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="7077f-111">Det här kommandot lägger till en kock-anknytning till en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="7077f-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="7077f-112">När den virtuella datorn kommer är den bootstrapped med kock och kör Apache på den.</span><span class="sxs-lookup"><span data-stu-id="7077f-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="7077f-113">Exempel 2: lägga till en kock-anknytning till en virtuell Windows-dator med start</span><span class="sxs-lookup"><span data-stu-id="7077f-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="7077f-114">Det här kommandot lägger till filen kock till en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="7077f-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="7077f-115">När den virtuella datorn startas är den bootstrapped med kock och kör Apache på den.</span><span class="sxs-lookup"><span data-stu-id="7077f-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="7077f-116">Efter start refererar den virtuella datorn till den *BootstrapOptions* som anges i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="7077f-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="7077f-117">Exempel 3: lägga till en kock-anknytning till en virtuell Windows-dator och installera Apache och GIT</span><span class="sxs-lookup"><span data-stu-id="7077f-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="7077f-118">Det här kommandot lägger till filen kock till en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="7077f-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="7077f-119">När den virtuella datorn startas är det bootstrapped med kock och har Apache och GIT installerat.</span><span class="sxs-lookup"><span data-stu-id="7077f-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="7077f-120">Om du inte anger client. RB måste du ange URL-adressen till chefs servern och verifierings klient namnet.</span><span class="sxs-lookup"><span data-stu-id="7077f-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="7077f-121">Exempel 4: lägga till en kock-anknytning till en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="7077f-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="7077f-122">Det här kommandot lägger till filen kock till en virtuell dator i Linux.</span><span class="sxs-lookup"><span data-stu-id="7077f-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="7077f-123">När den virtuella datorn startas är den bootstrapped med kock.</span><span class="sxs-lookup"><span data-stu-id="7077f-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="7077f-124">Om du inte anger client. RB måste du ange URL och organisation för chefs servern.</span><span class="sxs-lookup"><span data-stu-id="7077f-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="7077f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7077f-125">PARAMETERS</span></span>

### <span data-ttu-id="7077f-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="7077f-126">-BootstrapOptions</span></span>
<span data-ttu-id="7077f-127">Anger start alternativ i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="7077f-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="7077f-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="7077f-128">-BootstrapVersion</span></span>
<span data-ttu-id="7077f-129">Anger vilken version av chefs klienten som installeras tillsammans med tillägget.</span><span class="sxs-lookup"><span data-stu-id="7077f-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="7077f-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="7077f-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="7077f-131">Anger hur ofta (i minuter) som kock-tjänsten körs.</span><span class="sxs-lookup"><span data-stu-id="7077f-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="7077f-132">Om du inte vill att kock-tjänsten ska installeras på Azure VM ställer du in värdet som 0 i det här fältet.</span><span class="sxs-lookup"><span data-stu-id="7077f-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7077f-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="7077f-133">-ChefServerUrl</span></span>
<span data-ttu-id="7077f-134">Anger URL-adressen för chefs servern.</span><span class="sxs-lookup"><span data-stu-id="7077f-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="7077f-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="7077f-135">-ClientRb</span></span>
<span data-ttu-id="7077f-136">Anger den fullständiga sökvägen för chef client. RB.</span><span class="sxs-lookup"><span data-stu-id="7077f-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="7077f-137">-Daemon</span><span class="sxs-lookup"><span data-stu-id="7077f-137">-Daemon</span></span>
<span data-ttu-id="7077f-138">Konfigurerar chef för klient tjänst för obevakad körning.</span><span class="sxs-lookup"><span data-stu-id="7077f-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="7077f-139">Noden plattform bör vara Windows.</span><span class="sxs-lookup"><span data-stu-id="7077f-139">The node platform should be Windows.</span></span>
<span data-ttu-id="7077f-140">Tillåtna alternativ: none, service och Task.</span><span class="sxs-lookup"><span data-stu-id="7077f-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="7077f-141">ingen-hindrar för tillfället att klient tjänsten är konfigurerad som en tjänst.</span><span class="sxs-lookup"><span data-stu-id="7077f-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="7077f-142">tjänst – konfigurerar kock-klienten så att den körs automatiskt i bakgrunden som en tjänst.</span><span class="sxs-lookup"><span data-stu-id="7077f-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="7077f-143">uppgift – konfigurerar kock-klienten så att den körs automatiskt i bakgrunden som en secheduled-uppgift.</span><span class="sxs-lookup"><span data-stu-id="7077f-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="7077f-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7077f-144">-InformationAction</span></span>
<span data-ttu-id="7077f-145">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="7077f-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7077f-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7077f-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7077f-147">Vidare</span><span class="sxs-lookup"><span data-stu-id="7077f-147">Continue</span></span>
- <span data-ttu-id="7077f-148">Över</span><span class="sxs-lookup"><span data-stu-id="7077f-148">Ignore</span></span>
- <span data-ttu-id="7077f-149">Inquire</span><span class="sxs-lookup"><span data-stu-id="7077f-149">Inquire</span></span>
- <span data-ttu-id="7077f-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7077f-150">SilentlyContinue</span></span>
- <span data-ttu-id="7077f-151">Stanna</span><span class="sxs-lookup"><span data-stu-id="7077f-151">Stop</span></span>
- <span data-ttu-id="7077f-152">Avbryt</span><span class="sxs-lookup"><span data-stu-id="7077f-152">Suspend</span></span>

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

### <span data-ttu-id="7077f-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7077f-153">-InformationVariable</span></span>
<span data-ttu-id="7077f-154">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="7077f-154">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7077f-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="7077f-155">-JsonAttribute</span></span>
<span data-ttu-id="7077f-156">En JSON-sträng som ska läggas till i första körningen av kock-klienten.</span><span class="sxs-lookup"><span data-stu-id="7077f-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="7077f-157">t.-JsonAttribute ' {"foo": "bar"}</span><span class="sxs-lookup"><span data-stu-id="7077f-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="7077f-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="7077f-158">-Linux</span></span>
<span data-ttu-id="7077f-159">Anger att denna cmdlet skapar en Linux-baserad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7077f-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="7077f-160">-Organisations namn</span><span class="sxs-lookup"><span data-stu-id="7077f-160">-OrganizationName</span></span>
<span data-ttu-id="7077f-161">Anger organisations namnet för chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="7077f-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="7077f-162">-Profil</span><span class="sxs-lookup"><span data-stu-id="7077f-162">-Profile</span></span>
<span data-ttu-id="7077f-163">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7077f-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7077f-164">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7077f-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7077f-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="7077f-165">-RunList</span></span>
<span data-ttu-id="7077f-166">Anger noden för en kock-nod.</span><span class="sxs-lookup"><span data-stu-id="7077f-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="7077f-167">-Secret</span><span class="sxs-lookup"><span data-stu-id="7077f-167">-Secret</span></span>
<span data-ttu-id="7077f-168">Krypterings nycklar som används för att kryptera och dekryptera objekt värden.</span><span class="sxs-lookup"><span data-stu-id="7077f-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="7077f-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="7077f-169">-SecretFile</span></span>
<span data-ttu-id="7077f-170">Sökvägen till filen som innehåller krypterings knappen som används för att kryptera och dekryptera objektets värden.</span><span class="sxs-lookup"><span data-stu-id="7077f-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="7077f-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="7077f-171">-ValidationClientName</span></span>
<span data-ttu-id="7077f-172">Anger namnet på verifierings klienten.</span><span class="sxs-lookup"><span data-stu-id="7077f-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="7077f-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="7077f-173">-ValidationPem</span></span>
<span data-ttu-id="7077f-174">Anger sökväg för chefs-validator. pem.</span><span class="sxs-lookup"><span data-stu-id="7077f-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="7077f-175">-Version</span><span class="sxs-lookup"><span data-stu-id="7077f-175">-Version</span></span>
<span data-ttu-id="7077f-176">Anger versions numret för chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="7077f-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="7077f-177">-VM</span><span class="sxs-lookup"><span data-stu-id="7077f-177">-VM</span></span>
<span data-ttu-id="7077f-178">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="7077f-178">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="7077f-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="7077f-179">-Windows</span></span>
<span data-ttu-id="7077f-180">Anger att den här cmdleten skapar en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="7077f-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="7077f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7077f-181">CommonParameters</span></span>
<span data-ttu-id="7077f-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7077f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7077f-183">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7077f-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7077f-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7077f-184">INPUTS</span></span>

## <span data-ttu-id="7077f-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7077f-185">OUTPUTS</span></span>

## <span data-ttu-id="7077f-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7077f-186">NOTES</span></span>

## <span data-ttu-id="7077f-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7077f-187">RELATED LINKS</span></span>

[<span data-ttu-id="7077f-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7077f-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="7077f-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7077f-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


