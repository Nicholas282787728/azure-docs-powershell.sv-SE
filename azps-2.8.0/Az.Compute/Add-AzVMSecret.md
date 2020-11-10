---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 561610141f0f802b8e2a2bc917330e67c0e5f482
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395245"
---
# <span data-ttu-id="b3cda-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="b3cda-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="b3cda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3cda-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cda-103">Lägger till en hemlighet till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cda-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="b3cda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3cda-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3cda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3cda-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cda-106">Cmdleten **Add-AzVMSecret** lägger till en hemlighet till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cda-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="b3cda-107">Med det här värdet kan du lägga till ett certifikat till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b3cda-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="b3cda-108">Hemligheten måste lagras i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="b3cda-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="b3cda-109">Mer information om viktiga valv finns i [Vad är Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b3cda-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="b3cda-110">Mer information om cmdletar finns i cmdletarna för [Azure Key Vault](/powershell/module/az.keyvault) eller cmdleten [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="b3cda-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="b3cda-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3cda-111">EXAMPLES</span></span>

### <span data-ttu-id="b3cda-112">Exempel 1: lägga till en hemlighet på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b3cda-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="b3cda-113">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="b3cda-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b3cda-114">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="b3cda-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b3cda-115">Det andra kommandot skapar ett Credential-objekt med hjälp av Get-Credential cmdlet och lagrar sedan resultatet i variabeln $Credential.</span><span class="sxs-lookup"><span data-stu-id="b3cda-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="b3cda-116">Kommandot frågar efter användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b3cda-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="b3cda-117">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b3cda-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="b3cda-118">I det tredje kommandot används cmdleten **set-AzVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b3cda-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b3cda-119">Det fjärde kommandot tilldelar ett valv-ID till $SourceVaultId variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="b3cda-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="b3cda-120">Kommandot utgår från att variabeln $SubscriptionId har ett lämpligt värde.</span><span class="sxs-lookup"><span data-stu-id="b3cda-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="b3cda-121">Det femte kommandot tilldelar ett värde till variabeln $CertificateStore 01 för senare användning.</span><span class="sxs-lookup"><span data-stu-id="b3cda-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="b3cda-122">Det sjätte kommandot tilldelar en URL till en certifikat lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="b3cda-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="b3cda-123">Det sjunde kommandot lägger till en hemlighet till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b3cda-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b3cda-124">Parametern SourceVaultId anger Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b3cda-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="b3cda-125">Kommandot anger namnet på certifikat arkivet och URL-adressen till certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b3cda-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="b3cda-126">Du kan köra **AzVMSecret** flera gånger för att lägga till hemligheter för andra certifikat.</span><span class="sxs-lookup"><span data-stu-id="b3cda-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="b3cda-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3cda-127">PARAMETERS</span></span>

### <span data-ttu-id="b3cda-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b3cda-128">-CertificateStore</span></span>
<span data-ttu-id="b3cda-129">Anger namnet på ett certifikat Arkiv på den virtuella dator som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="b3cda-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="b3cda-130">Denna cmdlet lägger till certifikatet i arkivet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b3cda-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="b3cda-131">Du kan endast ange den här parametern för virtuella datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="b3cda-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b3cda-132">-CertificateUrl</span></span>
<span data-ttu-id="b3cda-133">Anger URL-adressen som pekar på en nyckel valv hemlighet som innehåller ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="b3cda-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="b3cda-134">Certifikatet är base64-kodningen för följande JavaScript-objekt, som är kodade i UTF-8: {"data": " \<Base64-encoded-file\> ", "datatyp": " \<file-format\> ", "lösen ord": " \<pfx-file-password\> "}, för närvarande accepterar data typen bara. PFX-filer.</span><span class="sxs-lookup"><span data-stu-id="b3cda-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cda-135">-DefaultProfile</span></span>
<span data-ttu-id="b3cda-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cda-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3cda-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b3cda-137">-SourceVaultId</span></span>
<span data-ttu-id="b3cda-138">Anger resurs-ID för det huvud valv som innehåller de certifikat som du kan lägga till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b3cda-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="b3cda-139">Det här värdet fungerar också som nycklar för att lägga till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="b3cda-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="b3cda-140">Det innebär att du kan använda samma värde för *SourceVaultId* när du lägger till flera certifikat från samma Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b3cda-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-141">-VM</span><span class="sxs-lookup"><span data-stu-id="b3cda-141">-VM</span></span>
<span data-ttu-id="b3cda-142">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b3cda-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b3cda-143">Använd cmdleten [Get-AzVM](./Get-AzVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b3cda-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b3cda-144">Du kan använda cmdleten [New-AzVMConfig](./New-AzVMConfig.md) för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b3cda-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="b3cda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cda-145">CommonParameters</span></span>
<span data-ttu-id="b3cda-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cda-147">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3cda-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cda-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3cda-148">INPUTS</span></span>

### <span data-ttu-id="b3cda-149">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b3cda-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b3cda-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b3cda-150">System.String</span></span>

## <span data-ttu-id="b3cda-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3cda-151">OUTPUTS</span></span>

### <span data-ttu-id="b3cda-152">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b3cda-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b3cda-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3cda-153">NOTES</span></span>

## <span data-ttu-id="b3cda-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3cda-154">RELATED LINKS</span></span>

[<span data-ttu-id="b3cda-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3cda-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b3cda-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b3cda-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="b3cda-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b3cda-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
