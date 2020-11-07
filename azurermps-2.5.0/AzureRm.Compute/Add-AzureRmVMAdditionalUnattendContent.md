---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: e1441178898f675d0ccc5e654d3020212e532d90
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930757"
---
# <span data-ttu-id="60a1c-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="60a1c-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="60a1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="60a1c-103">Lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="60a1c-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60a1c-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a1c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="60a1c-106">Cmdleten **Add-AzureRmVMAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="60a1c-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="60a1c-107">Ange ytterligare Base 64-kodad. XML-formaterad information som läggs till i unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="60a1c-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="60a1c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60a1c-108">EXAMPLES</span></span>

### <span data-ttu-id="60a1c-109">Exempel 1: lägga till innehåll i unattend.xml</span><span class="sxs-lookup"><span data-stu-id="60a1c-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="60a1c-110">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="60a1c-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="60a1c-111">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="60a1c-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="60a1c-112">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="60a1c-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="60a1c-113">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="60a1c-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="60a1c-114">Det tredje kommandot skapar ett Credential-objekt med hjälp av Get-Credential cmdlet och lagrar sedan resultatet i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="60a1c-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="60a1c-115">Kommandot frågar efter användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="60a1c-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="60a1c-116">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="60a1c-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="60a1c-117">Det fjärde kommandot använder cmdleten **set-AzureRmVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="60a1c-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="60a1c-118">Det femte kommandot tilldelar innehåll till $AucContent variabel.</span><span class="sxs-lookup"><span data-stu-id="60a1c-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="60a1c-119">Innehållet inkluderar ett lösen ord.</span><span class="sxs-lookup"><span data-stu-id="60a1c-119">The content includes a password.</span></span>

<span data-ttu-id="60a1c-120">Med kommandot slut läggs innehållet som lagras i $AucContent till unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="60a1c-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="60a1c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60a1c-121">PARAMETERS</span></span>

### <span data-ttu-id="60a1c-122">-Innehåll</span><span class="sxs-lookup"><span data-stu-id="60a1c-122">-Content</span></span>
<span data-ttu-id="60a1c-123">Anger Base 64-kodat XML-formaterat innehåll.</span><span class="sxs-lookup"><span data-stu-id="60a1c-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="60a1c-124">Denna cmdlet lägger till innehållet i unattend.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="60a1c-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="60a1c-125">XML-innehåll måste vara mindre än 4 KB och måste innehålla rot elementet för den inställning eller funktion som denna cmdlet infogar.</span><span class="sxs-lookup"><span data-stu-id="60a1c-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a1c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a1c-126">-DefaultProfile</span></span>
<span data-ttu-id="60a1c-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60a1c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a1c-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="60a1c-128">-SettingName</span></span>
<span data-ttu-id="60a1c-129">Anger namnet på den inställning som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="60a1c-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="60a1c-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="60a1c-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60a1c-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="60a1c-131">FirstLogonCommands</span></span>
- <span data-ttu-id="60a1c-132">Automatisk inloggning</span><span class="sxs-lookup"><span data-stu-id="60a1c-132">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a1c-133">-VM</span><span class="sxs-lookup"><span data-stu-id="60a1c-133">-VM</span></span>
<span data-ttu-id="60a1c-134">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="60a1c-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="60a1c-135">Använd cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="60a1c-135">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="60a1c-136">Skapa ett virtuellt dator objekt med hjälp av [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a1c-136">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="60a1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a1c-137">CommonParameters</span></span>
<span data-ttu-id="60a1c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a1c-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a1c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a1c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60a1c-140">INPUTS</span></span>

### <span data-ttu-id="60a1c-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60a1c-141">PSVirtualMachine</span></span>
<span data-ttu-id="60a1c-142">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="60a1c-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="60a1c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60a1c-143">OUTPUTS</span></span>

### <span data-ttu-id="60a1c-144">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60a1c-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="60a1c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60a1c-145">NOTES</span></span>

## <span data-ttu-id="60a1c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60a1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="60a1c-147">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60a1c-147">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="60a1c-148">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="60a1c-148">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="60a1c-149">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="60a1c-149">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
