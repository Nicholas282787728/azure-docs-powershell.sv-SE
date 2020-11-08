---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 01d1b07ec861b5eeb02d4590001e304936bde395
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092350"
---
# <span data-ttu-id="ceddf-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ceddf-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="ceddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ceddf-102">SYNOPSIS</span></span>
<span data-ttu-id="ceddf-103">Anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ceddf-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="ceddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ceddf-104">SYNTAX</span></span>

### <span data-ttu-id="ceddf-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="ceddf-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceddf-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ceddf-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceddf-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ceddf-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceddf-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ceddf-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceddf-109">Linux</span><span class="sxs-lookup"><span data-stu-id="ceddf-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ceddf-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ceddf-110">DESCRIPTION</span></span>
<span data-ttu-id="ceddf-111">Cmdleten **set-AzVMOperatingSystem** anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ceddf-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="ceddf-112">Du kan ange inloggnings uppgifter, dator namn och typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="ceddf-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="ceddf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ceddf-113">EXAMPLES</span></span>

### <span data-ttu-id="ceddf-114">Exempel 1: Ange egenskaper för operativ systemet för en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ceddf-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="ceddf-115">Det första kommandot konverterar ett lösen ord till en säker sträng och lagrar det sedan i $SecurePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="ceddf-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="ceddf-116">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ceddf-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="ceddf-117">Det andra kommandot skapar en autentiseringsuppgift för användaren FullerP och det lösen ord som lagras i $SecurePassword och lagrar sedan autentiseringsuppgiften i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ceddf-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="ceddf-118">Om du vill ha mer information skriver du `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="ceddf-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="ceddf-119">Det tredje kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="ceddf-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ceddf-120">Det fjärde kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="ceddf-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ceddf-121">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="ceddf-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ceddf-122">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ceddf-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ceddf-123">Nästa fyra kommandon tilldelar värden till variabler som ska användas i följande kommando.</span><span class="sxs-lookup"><span data-stu-id="ceddf-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="ceddf-124">Eftersom du kan ange de här strängarna direkt i kommandot **set-AzVMOperatingSystem** används den här metoden endast för läsbarhet.</span><span class="sxs-lookup"><span data-stu-id="ceddf-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="ceddf-125">Men du kan använda en metod som det här i skript.</span><span class="sxs-lookup"><span data-stu-id="ceddf-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="ceddf-126">Det sista kommandot anger egenskaper för operativ systemet för den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ceddf-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ceddf-127">Kommandot använder autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="ceddf-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="ceddf-128">Kommandot använder variabler som tilldelats tidigare kommandon för vissa parametrar.</span><span class="sxs-lookup"><span data-stu-id="ceddf-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="ceddf-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ceddf-129">PARAMETERS</span></span>

### <span data-ttu-id="ceddf-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ceddf-130">-ComputerName</span></span>
<span data-ttu-id="ceddf-131">Anger namnet på datorn.</span><span class="sxs-lookup"><span data-stu-id="ceddf-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="ceddf-132">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ceddf-132">-Credential</span></span>
<span data-ttu-id="ceddf-133">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ceddf-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ceddf-134">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ceddf-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ceddf-135">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ceddf-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="ceddf-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ceddf-136">-CustomData</span></span>
<span data-ttu-id="ceddf-137">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="ceddf-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ceddf-138">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ceddf-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ceddf-139">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="ceddf-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ceddf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceddf-140">-DefaultProfile</span></span>
<span data-ttu-id="ceddf-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ceddf-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceddf-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ceddf-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ceddf-143">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="ceddf-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="ceddf-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ceddf-144">-DisableVMAgent</span></span>
<span data-ttu-id="ceddf-145">Inaktivera etablera virtuell dator agent.</span><span class="sxs-lookup"><span data-stu-id="ceddf-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="ceddf-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ceddf-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="ceddf-147">Anger att denna cmdlet aktiverar AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="ceddf-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="ceddf-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="ceddf-148">-Linux</span></span>
<span data-ttu-id="ceddf-149">Anger att operativ systemet är Linux.</span><span class="sxs-lookup"><span data-stu-id="ceddf-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="ceddf-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ceddf-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="ceddf-151">Anger att inställningarna kräver att den virtuella dator agenten är installerad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ceddf-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="ceddf-152">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ceddf-152">-TimeZone</span></span>
<span data-ttu-id="ceddf-153">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ceddf-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="ceddf-154">-VM</span><span class="sxs-lookup"><span data-stu-id="ceddf-154">-VM</span></span>
<span data-ttu-id="ceddf-155">Anger det lokala virtuella dator objekt där du kan ange egenskaper för operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="ceddf-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="ceddf-156">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="ceddf-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ceddf-157">Skapa ett virtuellt dator objekt med hjälp av New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceddf-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="ceddf-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="ceddf-158">-Windows</span></span>
<span data-ttu-id="ceddf-159">Anger att operativ systemet är Windows.</span><span class="sxs-lookup"><span data-stu-id="ceddf-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="ceddf-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ceddf-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="ceddf-161">Anger URI för ett WinRM-certifikat.</span><span class="sxs-lookup"><span data-stu-id="ceddf-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="ceddf-162">Det här måste lagras i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="ceddf-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="ceddf-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ceddf-163">-WinRMHttp</span></span>
<span data-ttu-id="ceddf-164">Anger att det här operativ systemet använder HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="ceddf-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="ceddf-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ceddf-165">-WinRMHttps</span></span>
<span data-ttu-id="ceddf-166">Anger att det här operativ systemet använder HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="ceddf-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="ceddf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceddf-167">CommonParameters</span></span>
<span data-ttu-id="ceddf-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceddf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceddf-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceddf-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceddf-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ceddf-170">INPUTS</span></span>

### <span data-ttu-id="ceddf-171">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ceddf-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ceddf-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ceddf-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ceddf-173">System. String</span><span class="sxs-lookup"><span data-stu-id="ceddf-173">System.String</span></span>

### <span data-ttu-id="ceddf-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ceddf-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ceddf-175">System. URI</span><span class="sxs-lookup"><span data-stu-id="ceddf-175">System.Uri</span></span>

## <span data-ttu-id="ceddf-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ceddf-176">OUTPUTS</span></span>

### <span data-ttu-id="ceddf-177">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ceddf-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ceddf-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ceddf-178">NOTES</span></span>

## <span data-ttu-id="ceddf-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ceddf-179">RELATED LINKS</span></span>

[<span data-ttu-id="ceddf-180">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ceddf-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ceddf-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ceddf-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

