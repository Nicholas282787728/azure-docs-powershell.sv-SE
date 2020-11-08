---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100628"
---
# <span data-ttu-id="41aa2-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-101">New-WAPackVM</span></span>

## <span data-ttu-id="41aa2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="41aa2-103">Skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="41aa2-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="41aa2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41aa2-104">SYNTAX</span></span>

### <span data-ttu-id="41aa2-105">CreateVMFromTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="41aa2-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="41aa2-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="41aa2-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="41aa2-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="41aa2-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41aa2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41aa2-108">DESCRIPTION</span></span>
<span data-ttu-id="41aa2-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="41aa2-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="41aa2-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="41aa2-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="41aa2-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="41aa2-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="41aa2-112">Cmdleten **New-WAPackVM** skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="41aa2-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="41aa2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41aa2-113">EXAMPLES</span></span>

### <span data-ttu-id="41aa2-114">Exempel 1: skapa en virtuell dator för Windows operativ system med hjälp av en mall</span><span class="sxs-lookup"><span data-stu-id="41aa2-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="41aa2-115">Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="41aa2-116">Du uppmanas att ange ett konto och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="41aa2-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="41aa2-117">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="41aa2-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="41aa2-118">Det andra kommandot hämtar mallen för virtuell dator med namnet ContosoTemplate04 med hjälp av cmdleten **Get-WAPackVMTemplate** och lagrar den sedan i $Template variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="41aa2-119">Med kommandot slut skapas en virtuell dator med namnet ContosoV023, baserat på mallen som lagras i $Template variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="41aa2-120">Kommandot anger *Windows* -parametern och därför måste den virtuella datorn köra en version av operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="41aa2-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="41aa2-121">Exempel 2: skapa en virtuell dator för Linux-operativsystemet genom att använda en mall</span><span class="sxs-lookup"><span data-stu-id="41aa2-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="41aa2-122">Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="41aa2-123">Det andra kommandot hämtar mallen för virtuell dator med namnet ContosoTemplate19 med hjälp av cmdleten **Get-WAPackVMTemplate** och lagrar den sedan i $Template variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="41aa2-124">Med kommandot slut skapas en virtuell dator med namnet ContosoV028, baserat på mallen som lagras i $Template variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="41aa2-125">Kommandot anger *Linux* -parametern och därför måste den virtuella datorn köra en version av Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="41aa2-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="41aa2-126">Exempel 3: skapa en virtuell dator från en hård disk och storleks profil</span><span class="sxs-lookup"><span data-stu-id="41aa2-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="41aa2-127">Det första kommandot får en operativ system disk som heter ContosoDiskOS med hjälp av cmdleten **Get-WAPackVMOSDisk** och lagrar den sedan i $OSDisk variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="41aa2-128">Det andra kommandot får storleks profilen "MediumSizeVM" med cmdleten **Get-WAPackVMSizeProfile** och lagrar den sedan i $SizeProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="41aa2-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="41aa2-129">Med kommandot slut skapas en virtuell dator med namnet ContosoV073 från operativ system disken som lagras i $OSDisk och den profil som lagras i $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="41aa2-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="41aa2-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41aa2-130">PARAMETERS</span></span>

### <span data-ttu-id="41aa2-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="41aa2-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="41aa2-132">Anger SSH-tangenten (Secure Shell) för administratörs kontot.</span><span class="sxs-lookup"><span data-stu-id="41aa2-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="41aa2-133">-Linux</span></span>
<span data-ttu-id="41aa2-134">Anger att cmdleten skapar en virtuell dator som kör Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="41aa2-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="41aa2-135">-Name</span></span>
<span data-ttu-id="41aa2-136">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="41aa2-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="41aa2-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="41aa2-137">-OSDisk</span></span>
<span data-ttu-id="41aa2-138">Anger en operativ system disk som ett **VirtualHardDisk** -objekt.</span><span class="sxs-lookup"><span data-stu-id="41aa2-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="41aa2-139">Använd cmdleten **Get-WAPackVMOSDisk** för att få en operativ system disk.</span><span class="sxs-lookup"><span data-stu-id="41aa2-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="41aa2-140">-ProductKey</span></span>
<span data-ttu-id="41aa2-141">Anger en produkt nyckeln.</span><span class="sxs-lookup"><span data-stu-id="41aa2-141">Specifies a product key.</span></span>
<span data-ttu-id="41aa2-142">Produkt nyckeln är ett 25-siffrigt nummer som identifierar produkt licensen.</span><span class="sxs-lookup"><span data-stu-id="41aa2-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="41aa2-143">Använd en produkt nyckeln för ett operativ system som du planerar att installera på en virtuell dator eller värd.</span><span class="sxs-lookup"><span data-stu-id="41aa2-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="41aa2-144">-Profile</span></span>
<span data-ttu-id="41aa2-145">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="41aa2-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41aa2-146">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="41aa2-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41aa2-147">-Mall</span><span class="sxs-lookup"><span data-stu-id="41aa2-147">-Template</span></span>
<span data-ttu-id="41aa2-148">Anger en mall.</span><span class="sxs-lookup"><span data-stu-id="41aa2-148">Specifies a template.</span></span>
<span data-ttu-id="41aa2-149">Cmdleten skapar en virtuell dator utifrån den mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="41aa2-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="41aa2-150">Använd cmdleten Get-WAPackVMTemplate för att hämta ett Template-objekt.</span><span class="sxs-lookup"><span data-stu-id="41aa2-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="41aa2-151">-VMCredential</span></span>
<span data-ttu-id="41aa2-152">Anger autentiseringsuppgifter för det lokala administratörs kontot.</span><span class="sxs-lookup"><span data-stu-id="41aa2-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="41aa2-153">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="41aa2-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="41aa2-154">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="41aa2-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="41aa2-155">-VMSizeProfile</span></span>
<span data-ttu-id="41aa2-156">Anger en storleks profil för en virtuell dator som ett **HardwareProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="41aa2-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="41aa2-157">Använd cmdleten **Get-WAPackVMSizeProfile** för att få en storleks profil.</span><span class="sxs-lookup"><span data-stu-id="41aa2-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="41aa2-158">-VNet</span></span>
<span data-ttu-id="41aa2-159">Anger ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="41aa2-159">Specifies a virtual network.</span></span>
<span data-ttu-id="41aa2-160">Cmdleten ansluter den virtuella datorn till det virtuella nätverk som du anger.</span><span class="sxs-lookup"><span data-stu-id="41aa2-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="41aa2-161">Använd cmdleten **Get-WAPackVNet** för att få ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="41aa2-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="41aa2-162">-Windows</span></span>
<span data-ttu-id="41aa2-163">Anger att cmdleten skapar en virtuell dator för att köra operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="41aa2-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41aa2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41aa2-164">CommonParameters</span></span>
<span data-ttu-id="41aa2-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41aa2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41aa2-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41aa2-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41aa2-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41aa2-167">INPUTS</span></span>

## <span data-ttu-id="41aa2-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41aa2-168">OUTPUTS</span></span>

## <span data-ttu-id="41aa2-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41aa2-169">NOTES</span></span>

## <span data-ttu-id="41aa2-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41aa2-170">RELATED LINKS</span></span>

[<span data-ttu-id="41aa2-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="41aa2-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="41aa2-173">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="41aa2-174">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="41aa2-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="41aa2-176">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="41aa2-177">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="41aa2-178">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="41aa2-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="41aa2-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="41aa2-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="41aa2-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="41aa2-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="41aa2-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="41aa2-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


