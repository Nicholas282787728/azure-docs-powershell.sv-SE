---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 2f4f11c66e01160fe757f16fb74cddc952cbd228
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925293"
---
# <span data-ttu-id="b2565-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="b2565-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="b2565-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2565-102">SYNOPSIS</span></span>
<span data-ttu-id="b2565-103">Lägger till en hemlighet till en VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2565-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="b2565-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2565-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2565-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2565-105">DESCRIPTION</span></span>
<span data-ttu-id="b2565-106">Cmdleten **Add-AzVmssSecret** lägger till en hemlighet till den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b2565-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b2565-107">Hemligheten måste lagras i ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b2565-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="b2565-108">Mer information om viktiga valv finns i [Vad är Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="b2565-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="b2565-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b2565-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="b2565-110">Mer information om cmdletar finns i [cmdlets för Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) i Microsoft Developer Network Library eller cmdleten [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="b2565-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="b2565-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2565-111">EXAMPLES</span></span>

### <span data-ttu-id="b2565-112">Exempel 1: lägga till en hemlighet på VMSS</span><span class="sxs-lookup"><span data-stu-id="b2565-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="b2565-113">I det här exemplet läggs en hemlighet till i VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2565-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="b2565-114">Det första kommandot använder cmdleten Get-AzKeyVault för att hämta en valv hemlighet från valvet ContosoVault och lagrar resultatet i variabeln som heter $Vault.</span><span class="sxs-lookup"><span data-stu-id="b2565-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="b2565-115">Med det andra kommandot används cmdleten **New-AzVmssVaultCertificateConfig** för att skapa en konfiguration för ett valv certifikat med hjälp av den angivna certifikat-URL: en från certifikat arkivet med namnen certifikat och lagrar resultaten i variabeln som heter $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="b2565-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="b2565-116">I det tredje kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2565-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b2565-117">Det fjärde kommandot lägger till en hemlighet till VMSS med hjälp av valv hemligheten med nyckel resurs-ID: t och valvet-certifikatet som lagras i $Vault och $CertConfig variabler.</span><span class="sxs-lookup"><span data-stu-id="b2565-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="b2565-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2565-118">PARAMETERS</span></span>

### <span data-ttu-id="b2565-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2565-119">-DefaultProfile</span></span>
<span data-ttu-id="b2565-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2565-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2565-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b2565-121">-SourceVaultId</span></span>
<span data-ttu-id="b2565-122">Anger resurs-ID för det huvud valv som innehåller de certifikat som du kan lägga till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b2565-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="b2565-123">Det här värdet fungerar också som nycklar för att lägga till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="b2565-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="b2565-124">Det innebär att du kan använda samma värde för parametern *SourceVaultId* när du lägger till flera certifikat från samma Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b2565-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="b2565-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b2565-125">-VaultCertificate</span></span>
<span data-ttu-id="b2565-126">Anger det valv **certifikat** objekt som innehåller certifikatets URL och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="b2565-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="b2565-127">Du kan använda cmdleten [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="b2565-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="b2565-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2565-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b2565-129">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="b2565-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="b2565-130">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="b2565-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2565-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2565-131">-Confirm</span></span>
<span data-ttu-id="b2565-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2565-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2565-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2565-133">-WhatIf</span></span>
<span data-ttu-id="b2565-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2565-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2565-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2565-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2565-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2565-136">CommonParameters</span></span>
<span data-ttu-id="b2565-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2565-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2565-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2565-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2565-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2565-139">INPUTS</span></span>

### <span data-ttu-id="b2565-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2565-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b2565-141">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b2565-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b2565-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2565-142">OUTPUTS</span></span>

### <span data-ttu-id="b2565-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2565-143">None</span></span>
<span data-ttu-id="b2565-144">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b2565-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b2565-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2565-145">NOTES</span></span>

## <span data-ttu-id="b2565-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2565-146">RELATED LINKS</span></span>

[<span data-ttu-id="b2565-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="b2565-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="b2565-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b2565-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)