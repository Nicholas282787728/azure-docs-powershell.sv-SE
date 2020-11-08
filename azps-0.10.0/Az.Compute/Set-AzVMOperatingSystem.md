---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924785"
---
# <span data-ttu-id="94a6a-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="94a6a-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="94a6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="94a6a-103">Anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="94a6a-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="94a6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94a6a-104">SYNTAX</span></span>

### <span data-ttu-id="94a6a-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="94a6a-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a6a-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="94a6a-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a6a-107">Linux</span><span class="sxs-lookup"><span data-stu-id="94a6a-107">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94a6a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94a6a-108">DESCRIPTION</span></span>
<span data-ttu-id="94a6a-109">Cmdleten **set-AzVMOperatingSystem** anger egenskaper för operativ systemet för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="94a6a-109">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="94a6a-110">Du kan ange inloggnings uppgifter, dator namn och typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="94a6a-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="94a6a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94a6a-111">EXAMPLES</span></span>

### <span data-ttu-id="94a6a-112">Exempel 1: Ange egenskaper för operativ systemet för en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="94a6a-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="94a6a-113">Det första kommandot konverterar ett lösen ord till en säker sträng och lagrar det sedan i $SecurePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="94a6a-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="94a6a-114">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="94a6a-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="94a6a-115">Det andra kommandot skapar en autentiseringsuppgift för användaren FullerP och det lösen ord som lagras i $SecurePassword och lagrar sedan autentiseringsuppgiften i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="94a6a-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="94a6a-116">Om du vill ha mer information skriver du `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="94a6a-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="94a6a-117">Det tredje kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="94a6a-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="94a6a-118">Det fjärde kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="94a6a-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="94a6a-119">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="94a6a-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="94a6a-120">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="94a6a-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="94a6a-121">Nästa fyra kommandon tilldelar värden till variabler som ska användas i följande kommando.</span><span class="sxs-lookup"><span data-stu-id="94a6a-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="94a6a-122">Eftersom du kan ange de här strängarna direkt i kommandot **set-AzVMOperatingSystem** används den här metoden endast för läsbarhet.</span><span class="sxs-lookup"><span data-stu-id="94a6a-122">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="94a6a-123">Men du kan använda en metod som det här i skript.</span><span class="sxs-lookup"><span data-stu-id="94a6a-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="94a6a-124">Det sista kommandot anger egenskaper för operativ systemet för den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="94a6a-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="94a6a-125">Kommandot använder autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="94a6a-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="94a6a-126">Kommandot använder variabler som tilldelats tidigare kommandon för vissa parametrar.</span><span class="sxs-lookup"><span data-stu-id="94a6a-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="94a6a-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94a6a-127">PARAMETERS</span></span>

### <span data-ttu-id="94a6a-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="94a6a-128">-ComputerName</span></span>
<span data-ttu-id="94a6a-129">Anger namnet på datorn.</span><span class="sxs-lookup"><span data-stu-id="94a6a-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="94a6a-130">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="94a6a-130">-Credential</span></span>
<span data-ttu-id="94a6a-131">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="94a6a-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="94a6a-132">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="94a6a-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="94a6a-133">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="94a6a-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="94a6a-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="94a6a-134">-CustomData</span></span>
<span data-ttu-id="94a6a-135">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="94a6a-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="94a6a-136">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="94a6a-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="94a6a-137">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="94a6a-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="94a6a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a6a-138">-DefaultProfile</span></span>
<span data-ttu-id="94a6a-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94a6a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a6a-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="94a6a-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="94a6a-141">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="94a6a-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="94a6a-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="94a6a-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="94a6a-143">Anger att denna cmdlet aktiverar AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="94a6a-143">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="94a6a-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="94a6a-144">-Linux</span></span>
<span data-ttu-id="94a6a-145">Anger att operativ systemet är Linux.</span><span class="sxs-lookup"><span data-stu-id="94a6a-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="94a6a-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="94a6a-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="94a6a-147">Anger att inställningarna kräver att den virtuella dator agenten är installerad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="94a6a-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="94a6a-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="94a6a-148">-TimeZone</span></span>
<span data-ttu-id="94a6a-149">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="94a6a-149">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="94a6a-150">-VM</span><span class="sxs-lookup"><span data-stu-id="94a6a-150">-VM</span></span>
<span data-ttu-id="94a6a-151">Anger det lokala virtuella dator objekt där du kan ange egenskaper för operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="94a6a-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="94a6a-152">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="94a6a-152">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="94a6a-153">Skapa ett virtuellt dator objekt med hjälp av New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94a6a-153">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="94a6a-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="94a6a-154">-Windows</span></span>
<span data-ttu-id="94a6a-155">Anger att operativ systemet är Windows.</span><span class="sxs-lookup"><span data-stu-id="94a6a-155">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="94a6a-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="94a6a-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="94a6a-157">Anger URI för ett WinRM-certifikat.</span><span class="sxs-lookup"><span data-stu-id="94a6a-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="94a6a-158">Det här måste lagras i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="94a6a-158">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="94a6a-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="94a6a-159">-WinRMHttp</span></span>
<span data-ttu-id="94a6a-160">Anger att det här operativ systemet använder HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="94a6a-160">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="94a6a-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="94a6a-161">-WinRMHttps</span></span>
<span data-ttu-id="94a6a-162">Anger att det här operativ systemet använder HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="94a6a-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="94a6a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a6a-163">CommonParameters</span></span>
<span data-ttu-id="94a6a-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a6a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a6a-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a6a-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a6a-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94a6a-166">INPUTS</span></span>

### <span data-ttu-id="94a6a-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94a6a-167">PSVirtualMachine</span></span>
<span data-ttu-id="94a6a-168">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="94a6a-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="94a6a-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94a6a-169">OUTPUTS</span></span>

### <span data-ttu-id="94a6a-170">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94a6a-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="94a6a-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94a6a-171">NOTES</span></span>

## <span data-ttu-id="94a6a-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94a6a-172">RELATED LINKS</span></span>

[<span data-ttu-id="94a6a-173">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="94a6a-173">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="94a6a-174">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="94a6a-174">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

