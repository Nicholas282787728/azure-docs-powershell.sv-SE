---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: d5c84aab35b2c8dbbc6a3d1479a194ae9df827de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917518"
---
# <span data-ttu-id="e9bc9-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="e9bc9-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="e9bc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bc9-103">Lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="e9bc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9bc9-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9bc9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="e9bc9-106">Cmdleten **Add-AzVMAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="e9bc9-107">Ange ytterligare Base 64-kodad. XML-formaterad information som läggs till i unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="e9bc9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9bc9-108">EXAMPLES</span></span>

### <span data-ttu-id="e9bc9-109">Exempel 1: lägga till innehåll i unattend.xml</span><span class="sxs-lookup"><span data-stu-id="e9bc9-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="e9bc9-110">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e9bc9-111">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e9bc9-112">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e9bc9-113">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e9bc9-114">Det tredje kommandot skapar ett Credential-objekt med hjälp av Get-Credential cmdlet och lagrar sedan resultatet i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="e9bc9-115">Kommandot frågar efter användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="e9bc9-116">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e9bc9-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="e9bc9-117">Det fjärde kommandot använder cmdleten **set-AzVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e9bc9-118">Det femte kommandot tilldelar innehåll till $AucContent variabel.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="e9bc9-119">Innehållet inkluderar ett lösen ord.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-119">The content includes a password.</span></span>
<span data-ttu-id="e9bc9-120">Med kommandot slut läggs innehållet som lagras i $AucContent till unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="e9bc9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9bc9-121">PARAMETERS</span></span>

### <span data-ttu-id="e9bc9-122">-Innehåll</span><span class="sxs-lookup"><span data-stu-id="e9bc9-122">-Content</span></span>
<span data-ttu-id="e9bc9-123">Anger Base 64-kodat XML-formaterat innehåll.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="e9bc9-124">Denna cmdlet lägger till innehållet i unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="e9bc9-125">XML-innehåll måste vara mindre än 4 KB och måste innehålla rot elementet för den inställning eller funktion som denna cmdlet infogar.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bc9-126">-DefaultProfile</span></span>
<span data-ttu-id="e9bc9-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9bc9-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="e9bc9-128">-SettingName</span></span>
<span data-ttu-id="e9bc9-129">Anger namnet på den inställning som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="e9bc9-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e9bc9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9bc9-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="e9bc9-131">FirstLogonCommands</span></span>
- <span data-ttu-id="e9bc9-132">Automatisk inloggning</span><span class="sxs-lookup"><span data-stu-id="e9bc9-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc9-133">-VM</span><span class="sxs-lookup"><span data-stu-id="e9bc9-133">-VM</span></span>
<span data-ttu-id="e9bc9-134">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="e9bc9-135">Använd cmdleten [Get-AzVM](./Get-AzVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="e9bc9-136">Skapa ett virtuellt dator objekt med hjälp av [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="e9bc9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bc9-137">CommonParameters</span></span>
<span data-ttu-id="e9bc9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bc9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bc9-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9bc9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bc9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9bc9-140">INPUTS</span></span>

### <span data-ttu-id="e9bc9-141">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9bc9-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e9bc9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e9bc9-142">System.String</span></span>

### <span data-ttu-id="e9bc9-143">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e9bc9-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e9bc9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9bc9-144">OUTPUTS</span></span>

### <span data-ttu-id="e9bc9-145">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9bc9-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e9bc9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9bc9-146">NOTES</span></span>

## <span data-ttu-id="e9bc9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9bc9-147">RELATED LINKS</span></span>

[<span data-ttu-id="e9bc9-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e9bc9-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e9bc9-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9bc9-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="e9bc9-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e9bc9-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)