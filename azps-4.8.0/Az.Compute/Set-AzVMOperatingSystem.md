---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101623"
---
# <span data-ttu-id="6c30e-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6c30e-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="6c30e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c30e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c30e-103">Anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6c30e-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="6c30e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c30e-104">SYNTAX</span></span>

### <span data-ttu-id="6c30e-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="6c30e-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c30e-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="6c30e-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c30e-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="6c30e-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c30e-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="6c30e-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c30e-109">Linux</span><span class="sxs-lookup"><span data-stu-id="6c30e-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c30e-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c30e-110">DESCRIPTION</span></span>
<span data-ttu-id="6c30e-111">Cmdleten **set-AzVMOperatingSystem** anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6c30e-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="6c30e-112">Du kan ange inloggnings uppgifter, dator namn och typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="6c30e-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="6c30e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c30e-113">EXAMPLES</span></span>

### <span data-ttu-id="6c30e-114">Exempel 1: Ange egenskaper för operativ systemet för en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="6c30e-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="6c30e-115">Det första kommandot konverterar ett lösen ord till en säker sträng och lagrar det sedan i $SecurePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="6c30e-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="6c30e-116">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6c30e-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6c30e-117">Det andra kommandot skapar en autentiseringsuppgift för användaren FullerP och det lösen ord som lagras i $SecurePassword och lagrar sedan autentiseringsuppgiften i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6c30e-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="6c30e-118">Om du vill ha mer information skriver du `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="6c30e-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="6c30e-119">Det tredje kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="6c30e-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="6c30e-120">Det fjärde kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="6c30e-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6c30e-121">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="6c30e-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6c30e-122">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="6c30e-123">Nästa fyra kommandon tilldelar värden till variabler som ska användas i följande kommando.</span><span class="sxs-lookup"><span data-stu-id="6c30e-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="6c30e-124">Eftersom du kan ange de här strängarna direkt i kommandot **set-AzVMOperatingSystem** används den här metoden endast för läsbarhet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="6c30e-125">Men du kan använda en metod som det här i skript.</span><span class="sxs-lookup"><span data-stu-id="6c30e-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="6c30e-126">Det sista kommandot anger egenskaper för operativ systemet för den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6c30e-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6c30e-127">Kommandot använder autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="6c30e-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="6c30e-128">Kommandot använder variabler som tilldelats tidigare kommandon för vissa parametrar.</span><span class="sxs-lookup"><span data-stu-id="6c30e-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="6c30e-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c30e-129">PARAMETERS</span></span>

### <span data-ttu-id="6c30e-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="6c30e-130">-ComputerName</span></span>
<span data-ttu-id="6c30e-131">Anger namnet på datorn.</span><span class="sxs-lookup"><span data-stu-id="6c30e-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-132">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="6c30e-132">-Credential</span></span>
<span data-ttu-id="6c30e-133">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6c30e-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="6c30e-134">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="6c30e-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="6c30e-135">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="6c30e-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="6c30e-136">-CustomData</span></span>
<span data-ttu-id="6c30e-137">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="6c30e-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="6c30e-138">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6c30e-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="6c30e-139">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="6c30e-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="6c30e-140">**Obs! Godkänn inte någon hemlighet eller lösen ord i egenskapen customData**</span><span class="sxs-lookup"><span data-stu-id="6c30e-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="6c30e-141">Det går inte att uppdatera den här egenskapen när den virtuella datorn har skapats.</span><span class="sxs-lookup"><span data-stu-id="6c30e-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="6c30e-142">customData skickas till den virtuella datorn som ska sparas som en fil, mer information finns i [Anpassa data på virtuella Azure-datorer](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="6c30e-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="6c30e-143">Information om hur du använder Cloud-Init för Linux VM finns i [använda Cloud-Init för att anpassa en virtuella dator för Linux-skapande](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span><span class="sxs-lookup"><span data-stu-id="6c30e-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c30e-144">-DefaultProfile</span></span>
<span data-ttu-id="6c30e-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c30e-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="6c30e-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="6c30e-147">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="6c30e-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="6c30e-148">-DisableVMAgent</span></span>
<span data-ttu-id="6c30e-149">Inaktivera etablera virtuell dator agent.</span><span class="sxs-lookup"><span data-stu-id="6c30e-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6c30e-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="6c30e-151">Anger att denna cmdlet aktiverar AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="6c30e-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="6c30e-152">-Linux</span></span>
<span data-ttu-id="6c30e-153">Anger att operativ systemet är Linux.</span><span class="sxs-lookup"><span data-stu-id="6c30e-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="6c30e-154">-PatchMode</span></span>
<span data-ttu-id="6c30e-155">Anger läget för en gäst korrigering till IaaS virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="6c30e-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="6c30e-156">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="6c30e-156">Possible values are:</span></span><br>
<span data-ttu-id="6c30e-157">**Manuell** – du styr program korrigeringar till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6c30e-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="6c30e-158">Det gör du genom att använda korrigeringsfiler manuellt i den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6c30e-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="6c30e-159">I det här läget är automatiska uppdateringar inaktiverade; Egenskapen WindowsConfiguration. enableAutomaticUpdates måste vara falskt</span><span class="sxs-lookup"><span data-stu-id="6c30e-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="6c30e-160">**AutomaticByOS** – den virtuella datorn uppdateras automatiskt av operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="6c30e-161">Egenskapen WindowsConfiguration. enableAutomaticUpdates måste vara true.</span><span class="sxs-lookup"><span data-stu-id="6c30e-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="6c30e-162">**AutomaticByPlatform** – den virtuella datorn uppdateras automatiskt av operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="6c30e-163">Egenskaperna provisionVMAgent och WindowsConfiguration. enableAutomaticUpdates måste vara true</span><span class="sxs-lookup"><span data-stu-id="6c30e-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="6c30e-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="6c30e-165">Anger att inställningarna kräver att den virtuella dator agenten är installerad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6c30e-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="6c30e-166">-TimeZone</span></span>
<span data-ttu-id="6c30e-167">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6c30e-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="6c30e-168">t. \" Pacific, normal tid \" .</span><span class="sxs-lookup"><span data-stu-id="6c30e-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="6c30e-169">Möjliga värden kan vara [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) värde från tids zoner som returneras av [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="6c30e-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-170">-VM</span><span class="sxs-lookup"><span data-stu-id="6c30e-170">-VM</span></span>
<span data-ttu-id="6c30e-171">Anger det lokala virtuella dator objekt där du kan ange egenskaper för operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="6c30e-172">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="6c30e-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="6c30e-173">Skapa ett virtuellt dator objekt med hjälp av New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c30e-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="6c30e-174">-Windows</span></span>
<span data-ttu-id="6c30e-175">Anger att operativ systemet är Windows.</span><span class="sxs-lookup"><span data-stu-id="6c30e-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="6c30e-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="6c30e-177">Anger URI för ett WinRM-certifikat.</span><span class="sxs-lookup"><span data-stu-id="6c30e-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="6c30e-178">Det här måste lagras i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="6c30e-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="6c30e-179">-WinRMHttp</span></span>
<span data-ttu-id="6c30e-180">Anger att det här operativ systemet använder HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="6c30e-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="6c30e-181">-WinRMHttps</span></span>
<span data-ttu-id="6c30e-182">Anger att det här operativ systemet använder HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="6c30e-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c30e-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c30e-183">CommonParameters</span></span>
<span data-ttu-id="6c30e-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c30e-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c30e-185">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c30e-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c30e-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c30e-186">INPUTS</span></span>

### <span data-ttu-id="6c30e-187">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c30e-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6c30e-188">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6c30e-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6c30e-189">System. String</span><span class="sxs-lookup"><span data-stu-id="6c30e-189">System.String</span></span>

### <span data-ttu-id="6c30e-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="6c30e-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="6c30e-191">System. URI</span><span class="sxs-lookup"><span data-stu-id="6c30e-191">System.Uri</span></span>

## <span data-ttu-id="6c30e-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c30e-192">OUTPUTS</span></span>

### <span data-ttu-id="6c30e-193">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c30e-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6c30e-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c30e-194">NOTES</span></span>

## <span data-ttu-id="6c30e-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c30e-195">RELATED LINKS</span></span>

[<span data-ttu-id="6c30e-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6c30e-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6c30e-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6c30e-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


