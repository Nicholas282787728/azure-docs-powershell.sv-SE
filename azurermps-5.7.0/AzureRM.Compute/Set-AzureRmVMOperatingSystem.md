---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578283"
---
# <span data-ttu-id="245cb-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="245cb-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="245cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="245cb-102">SYNOPSIS</span></span>
<span data-ttu-id="245cb-103">Anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="245cb-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="245cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="245cb-104">SYNTAX</span></span>

### <span data-ttu-id="245cb-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="245cb-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="245cb-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="245cb-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="245cb-107">Linux</span><span class="sxs-lookup"><span data-stu-id="245cb-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="245cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="245cb-108">DESCRIPTION</span></span>
<span data-ttu-id="245cb-109">Cmdleten **set-AzureRmVMOperatingSystem** anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="245cb-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="245cb-110">Du kan ange inloggnings uppgifter, dator namn och typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="245cb-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="245cb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="245cb-111">EXAMPLES</span></span>

### <span data-ttu-id="245cb-112">Exempel 1: Ange egenskaper för operativ systemet för en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="245cb-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="245cb-113">Det första kommandot konverterar ett lösen ord till en säker sträng och lagrar det sedan i $SecurePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="245cb-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="245cb-114">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="245cb-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="245cb-115">Det andra kommandot skapar en autentiseringsuppgift för användaren FullerP och det lösen ord som lagras i $SecurePassword och lagrar sedan autentiseringsuppgiften i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="245cb-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="245cb-116">Om du vill ha mer information skriver du `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="245cb-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="245cb-117">Det tredje kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="245cb-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="245cb-118">Det fjärde kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="245cb-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="245cb-119">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="245cb-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="245cb-120">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="245cb-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="245cb-121">Nästa fyra kommandon tilldelar värden till variabler som ska användas i följande kommando.</span><span class="sxs-lookup"><span data-stu-id="245cb-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="245cb-122">Eftersom du kan ange de här strängarna direkt i kommandot **set-AzureRmVMOperatingSystem** används den här metoden endast för läsbarhet.</span><span class="sxs-lookup"><span data-stu-id="245cb-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="245cb-123">Men du kan använda en metod som det här i skript.</span><span class="sxs-lookup"><span data-stu-id="245cb-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="245cb-124">Det sista kommandot anger egenskaper för operativ systemet för den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="245cb-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="245cb-125">Kommandot använder autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="245cb-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="245cb-126">Kommandot använder variabler som tilldelats tidigare kommandon för vissa parametrar.</span><span class="sxs-lookup"><span data-stu-id="245cb-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="245cb-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="245cb-127">PARAMETERS</span></span>

### <span data-ttu-id="245cb-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="245cb-128">-ComputerName</span></span>
<span data-ttu-id="245cb-129">Anger namnet på datorn.</span><span class="sxs-lookup"><span data-stu-id="245cb-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-130">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="245cb-130">-Credential</span></span>
<span data-ttu-id="245cb-131">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="245cb-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="245cb-132">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="245cb-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="245cb-133">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="245cb-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="245cb-134">-CustomData</span></span>
<span data-ttu-id="245cb-135">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="245cb-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="245cb-136">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="245cb-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="245cb-137">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="245cb-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="245cb-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="245cb-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="245cb-139">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="245cb-139">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-140">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="245cb-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="245cb-141">Anger att denna cmdlet aktiverar AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="245cb-141">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="245cb-142">-Linux</span></span>
<span data-ttu-id="245cb-143">Anger att operativ systemet är Linux.</span><span class="sxs-lookup"><span data-stu-id="245cb-143">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="245cb-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="245cb-145">Anger att inställningarna kräver att den virtuella dator agenten är installerad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="245cb-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="245cb-146">-TimeZone</span></span>
<span data-ttu-id="245cb-147">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="245cb-147">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-148">-VM</span><span class="sxs-lookup"><span data-stu-id="245cb-148">-VM</span></span>
<span data-ttu-id="245cb-149">Anger det lokala virtuella dator objekt där du kan ange egenskaper för operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="245cb-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="245cb-150">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="245cb-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="245cb-151">Skapa ett virtuellt dator objekt med hjälp av New-AzureRmVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245cb-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="245cb-152">-Windows</span></span>
<span data-ttu-id="245cb-153">Anger att operativ systemet är Windows.</span><span class="sxs-lookup"><span data-stu-id="245cb-153">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-154">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="245cb-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="245cb-155">Anger URI för ett WinRM-certifikat.</span><span class="sxs-lookup"><span data-stu-id="245cb-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="245cb-156">Det här måste lagras i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="245cb-156">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="245cb-157">-WinRMHttp</span></span>
<span data-ttu-id="245cb-158">Anger att det här operativ systemet använder HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="245cb-158">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="245cb-159">-WinRMHttps</span></span>
<span data-ttu-id="245cb-160">Anger att det här operativ systemet använder HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="245cb-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245cb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245cb-161">CommonParameters</span></span>
<span data-ttu-id="245cb-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245cb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245cb-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245cb-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245cb-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="245cb-164">INPUTS</span></span>

### <span data-ttu-id="245cb-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="245cb-165">None</span></span>
<span data-ttu-id="245cb-166">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="245cb-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="245cb-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="245cb-167">OUTPUTS</span></span>

## <span data-ttu-id="245cb-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="245cb-168">NOTES</span></span>

## <span data-ttu-id="245cb-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="245cb-169">RELATED LINKS</span></span>

[<span data-ttu-id="245cb-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="245cb-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="245cb-171">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="245cb-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


