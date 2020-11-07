---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755266"
---
# <span data-ttu-id="04839-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="04839-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="04839-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04839-102">SYNOPSIS</span></span>
<span data-ttu-id="04839-103">Lägger till en hemlighet till en VMSS.</span><span class="sxs-lookup"><span data-stu-id="04839-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04839-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04839-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04839-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04839-105">DESCRIPTION</span></span>
<span data-ttu-id="04839-106">Cmdleten **Add-AzureRmVmssSecret** lägger till en hemlighet till den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="04839-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="04839-107">Hemligheten måste lagras i ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="04839-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="04839-108">Mer information om viktiga valv finns i [Vad är Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="04839-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="04839-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="04839-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="04839-110">Mer information om cmdletar finns i [cmdlets för Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) i Microsoft Developer Network Library eller cmdleten [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="04839-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="04839-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04839-111">EXAMPLES</span></span>

### <span data-ttu-id="04839-112">Exempel 1: lägga till en hemlighet på VMSS</span><span class="sxs-lookup"><span data-stu-id="04839-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="04839-113">I det här exemplet läggs en hemlighet till i VMSS.</span><span class="sxs-lookup"><span data-stu-id="04839-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="04839-114">Det första kommandot använder cmdleten Get-AzureRmKeyVault för att hämta en valv hemlighet från valvet ContosoVault och lagrar resultatet i variabeln som heter $Vault.</span><span class="sxs-lookup"><span data-stu-id="04839-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="04839-115">Med det andra kommandot används cmdleten **New-AzureRmVmssVaultCertificateConfig** för att skapa en konfiguration för ett valv certifikat med hjälp av den angivna certifikat-URL: en från certifikat arkivet med namnen certifikat och lagrar resultaten i variabeln som heter $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="04839-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="04839-116">I det tredje kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="04839-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="04839-117">Det fjärde kommandot lägger till en hemlighet till VMSS med hjälp av valv hemligheten med nyckel resurs-ID: t och valvet-certifikatet som lagras i $Vault och $CertConfig variabler.</span><span class="sxs-lookup"><span data-stu-id="04839-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="04839-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04839-118">PARAMETERS</span></span>

### <span data-ttu-id="04839-119">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="04839-119">-SourceVaultId</span></span>
<span data-ttu-id="04839-120">Anger resurs-ID för det huvud valv som innehåller de certifikat som du kan lägga till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="04839-120">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="04839-121">Det här värdet fungerar också som nycklar för att lägga till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="04839-121">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="04839-122">Det innebär att du kan använda samma värde för parametern *SourceVaultId* när du lägger till flera certifikat från samma Key-valv.</span><span class="sxs-lookup"><span data-stu-id="04839-122">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="04839-123">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="04839-123">-VaultCertificate</span></span>
<span data-ttu-id="04839-124">Anger det valv **certifikat** objekt som innehåller certifikatets URL och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="04839-124">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="04839-125">Du kan använda cmdleten [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="04839-125">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04839-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="04839-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="04839-127">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="04839-127">Specifies the VMSS object.</span></span>
<span data-ttu-id="04839-128">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="04839-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04839-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04839-129">-Confirm</span></span>
<span data-ttu-id="04839-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04839-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04839-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04839-131">-WhatIf</span></span>
<span data-ttu-id="04839-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04839-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04839-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04839-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04839-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04839-134">CommonParameters</span></span>
<span data-ttu-id="04839-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04839-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04839-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04839-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04839-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04839-137">INPUTS</span></span>

### <span data-ttu-id="04839-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="04839-138">None</span></span>
<span data-ttu-id="04839-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="04839-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04839-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04839-140">OUTPUTS</span></span>

###  
<span data-ttu-id="04839-141">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="04839-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="04839-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04839-142">NOTES</span></span>

## <span data-ttu-id="04839-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04839-143">RELATED LINKS</span></span>

[<span data-ttu-id="04839-144">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="04839-144">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="04839-145">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="04839-145">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
