---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25082cbf5b69867953580cb0f4b0ea74c15005da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577093"
---
# <span data-ttu-id="a993b-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a993b-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="a993b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a993b-102">SYNOPSIS</span></span>
<span data-ttu-id="a993b-103">Lägger till en kock-anknytning till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a993b-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a993b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a993b-104">SYNTAX</span></span>

### <span data-ttu-id="a993b-105">Linux</span><span class="sxs-lookup"><span data-stu-id="a993b-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a993b-106">Windows</span><span class="sxs-lookup"><span data-stu-id="a993b-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a993b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a993b-107">DESCRIPTION</span></span>
<span data-ttu-id="a993b-108">Cmdleten **set-AzureVMChefExtension** lägger till kock-tillägget till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a993b-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="a993b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a993b-109">EXAMPLES</span></span>

### <span data-ttu-id="a993b-110">Exempel 1: lägga till en kock-anknytning till en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="a993b-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="a993b-111">Det här kommandot lägger till en kock-anknytning till en virtuell Windows-dator med namnet WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="a993b-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="a993b-112">När den virtuella datorn startas startar chef den virtuella datorn för att köra apache.</span><span class="sxs-lookup"><span data-stu-id="a993b-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a993b-113">Exempel 2: lägga till en kock-anknytning till en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="a993b-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="a993b-114">Det här kommandot lägger till en kock-anknytning till en virtuell dator med namnet LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="a993b-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="a993b-115">När den virtuella datorn startas startar chef den virtuella datorn för att köra apache.</span><span class="sxs-lookup"><span data-stu-id="a993b-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a993b-116">Exempel 3: lägga till en kock-anknytning till en virtuell Windows-dator med start alternativ</span><span class="sxs-lookup"><span data-stu-id="a993b-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="a993b-117">Det här kommandot lägger till filen kock till en virtuell Windows-dator med namnet WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="a993b-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="a993b-118">När den virtuella datorn startas startar chef den virtuella datorn för att köra apache.</span><span class="sxs-lookup"><span data-stu-id="a993b-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="a993b-119">Efter start refererar den virtuella datorn till den BootstrapOptions som anges i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a993b-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="a993b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a993b-120">PARAMETERS</span></span>

### <span data-ttu-id="a993b-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a993b-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="a993b-122">-BootstrapOptions</span></span>
<span data-ttu-id="a993b-123">Anger konfigurations inställningar i alternativet client_rb.</span><span class="sxs-lookup"><span data-stu-id="a993b-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="a993b-124">-BootstrapVersion</span></span>
<span data-ttu-id="a993b-125">Anger start konfigurations versionen.</span><span class="sxs-lookup"><span data-stu-id="a993b-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="a993b-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="a993b-127">Anger hur ofta (i minuter) som kock-tjänsten körs.</span><span class="sxs-lookup"><span data-stu-id="a993b-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="a993b-128">Om du inte vill att kock-tjänsten ska installeras på Azure VM ställer du in värdet som 0 i det här fältet.</span><span class="sxs-lookup"><span data-stu-id="a993b-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="a993b-129">-ChefServerUrl</span></span>
<span data-ttu-id="a993b-130">Anger Server länken för kock, som en URL.</span><span class="sxs-lookup"><span data-stu-id="a993b-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="a993b-131">-ClientRb</span></span>
<span data-ttu-id="a993b-132">Anger den fullständiga sökvägen för chef client. RB.</span><span class="sxs-lookup"><span data-stu-id="a993b-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="a993b-133">-Daemon</span></span>
<span data-ttu-id="a993b-134">Konfigurerar chef för klient tjänst för obevakad körning.</span><span class="sxs-lookup"><span data-stu-id="a993b-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="a993b-135">Noden plattform bör vara Windows.</span><span class="sxs-lookup"><span data-stu-id="a993b-135">The node platform should be Windows.</span></span>
<span data-ttu-id="a993b-136">Tillåtna alternativ: none, service och Task.</span><span class="sxs-lookup"><span data-stu-id="a993b-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="a993b-137">ingen-hindrar för tillfället att klient tjänsten är konfigurerad som en tjänst.</span><span class="sxs-lookup"><span data-stu-id="a993b-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="a993b-138">tjänst – konfigurerar kock-klienten så att den körs automatiskt i bakgrunden som en tjänst.</span><span class="sxs-lookup"><span data-stu-id="a993b-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="a993b-139">uppgift – konfigurerar kock-klienten så att den körs automatiskt i bakgrunden som en secheduled-uppgift.</span><span class="sxs-lookup"><span data-stu-id="a993b-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a993b-140">-DefaultProfile</span></span>
<span data-ttu-id="a993b-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a993b-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="a993b-142">-JsonAttribute</span></span>
<span data-ttu-id="a993b-143">En JSON-sträng som ska läggas till i första körningen av kock-klienten.</span><span class="sxs-lookup"><span data-stu-id="a993b-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="a993b-144">t.-JsonAttribute ' {"foo": "bar"}</span><span class="sxs-lookup"><span data-stu-id="a993b-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="a993b-145">-Linux</span></span>
<span data-ttu-id="a993b-146">Anger att den här cmdleten skapar en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="a993b-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-147">-Plats</span><span class="sxs-lookup"><span data-stu-id="a993b-147">-Location</span></span>
<span data-ttu-id="a993b-148">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a993b-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="a993b-149">-Name</span></span>
<span data-ttu-id="a993b-150">Anger namnet på chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="a993b-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-151">-Organisations namn</span><span class="sxs-lookup"><span data-stu-id="a993b-151">-OrganizationName</span></span>
<span data-ttu-id="a993b-152">Anger organisations namnet för chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="a993b-152">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a993b-153">-ResourceGroupName</span></span>
<span data-ttu-id="a993b-154">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a993b-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="a993b-155">-RunList</span></span>
<span data-ttu-id="a993b-156">Anger noden för en kock-nod.</span><span class="sxs-lookup"><span data-stu-id="a993b-156">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-157">-Secret</span><span class="sxs-lookup"><span data-stu-id="a993b-157">-Secret</span></span>
<span data-ttu-id="a993b-158">Krypterings nycklar som används för att kryptera och dekryptera objekt värden.</span><span class="sxs-lookup"><span data-stu-id="a993b-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="a993b-159">-SecretFile</span></span>
<span data-ttu-id="a993b-160">Sökvägen till filen som innehåller krypterings knappen som används för att kryptera och dekryptera objektets värden.</span><span class="sxs-lookup"><span data-stu-id="a993b-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a993b-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="a993b-162">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a993b-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="a993b-163">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="a993b-164">-ValidationPem</span></span>
<span data-ttu-id="a993b-165">Anger sökväg för chefs-validator. pem</span><span class="sxs-lookup"><span data-stu-id="a993b-165">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="a993b-166">-VMName</span></span>
<span data-ttu-id="a993b-167">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a993b-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a993b-168">Denna cmdlet lägger till kock-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a993b-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="a993b-169">-Windows</span></span>
<span data-ttu-id="a993b-170">Anger att den här cmdleten skapar en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="a993b-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a993b-171">-Confirm</span></span>
<span data-ttu-id="a993b-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a993b-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a993b-173">-WhatIf</span></span>
<span data-ttu-id="a993b-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a993b-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a993b-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a993b-175">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a993b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a993b-176">CommonParameters</span></span>
<span data-ttu-id="a993b-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a993b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a993b-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a993b-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a993b-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a993b-179">INPUTS</span></span>

### <span data-ttu-id="a993b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="a993b-180">System.String</span></span>

### <span data-ttu-id="a993b-181">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a993b-181">System.Boolean</span></span>

## <span data-ttu-id="a993b-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a993b-182">OUTPUTS</span></span>

### <span data-ttu-id="a993b-183">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a993b-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a993b-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a993b-184">NOTES</span></span>

## <span data-ttu-id="a993b-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a993b-185">RELATED LINKS</span></span>

[<span data-ttu-id="a993b-186">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a993b-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="a993b-187">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a993b-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
