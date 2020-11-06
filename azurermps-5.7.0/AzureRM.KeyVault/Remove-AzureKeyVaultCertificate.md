---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583144"
---
# <span data-ttu-id="ba84e-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ba84e-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="ba84e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba84e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba84e-103">Tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ba84e-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba84e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba84e-104">SYNTAX</span></span>

### <span data-ttu-id="ba84e-105">ByVaultNameAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="ba84e-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba84e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ba84e-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba84e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba84e-107">DESCRIPTION</span></span>
<span data-ttu-id="ba84e-108">Cmdleten **Remove-AzureKeyVaultCertificate** tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ba84e-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="ba84e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba84e-109">EXAMPLES</span></span>

### <span data-ttu-id="ba84e-110">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="ba84e-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="ba84e-111">Det här kommandot tar bort certifikatet som heter SelfSigned01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="ba84e-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="ba84e-112">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ba84e-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ba84e-113">Därför behöver du inte bekräfta en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ba84e-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ba84e-114">Exempel 3: ta bort det borttagna certifikatet från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="ba84e-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="ba84e-115">Det här kommandot tar permanent bort certifikatet med namnet ' mitt certifikat ' från huvud valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="ba84e-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="ba84e-116">För att köra denna cmdlet krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren i det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="ba84e-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="ba84e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba84e-117">PARAMETERS</span></span>

### <span data-ttu-id="ba84e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba84e-118">-DefaultProfile</span></span>
<span data-ttu-id="ba84e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ba84e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba84e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ba84e-120">-Force</span></span>
<span data-ttu-id="ba84e-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ba84e-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba84e-122">-InputObject</span></span>
<span data-ttu-id="ba84e-123">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="ba84e-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ba84e-124">-InRemovedState</span></span>
<span data-ttu-id="ba84e-125">Om det finns någon tar bort det tidigare borttagna certifikatet permanent</span><span class="sxs-lookup"><span data-stu-id="ba84e-125">If present, removes the previously deleted certificate permanently</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba84e-126">-Name</span></span>
<span data-ttu-id="ba84e-127">Anger namnet på det certifikat som denna cmdlet tar bort från ett valv.</span><span class="sxs-lookup"><span data-stu-id="ba84e-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="ba84e-128">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="ba84e-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba84e-129">-PassThru</span></span>
<span data-ttu-id="ba84e-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ba84e-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba84e-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ba84e-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ba84e-132">-VaultName</span></span>
<span data-ttu-id="ba84e-133">Anger namnet på det huvud valv som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="ba84e-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="ba84e-134">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="ba84e-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba84e-135">-Confirm</span></span>
<span data-ttu-id="ba84e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba84e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba84e-137">-WhatIf</span></span>
<span data-ttu-id="ba84e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba84e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba84e-139">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba84e-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba84e-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba84e-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba84e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba84e-141">CommonParameters</span></span>
<span data-ttu-id="ba84e-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba84e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba84e-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba84e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba84e-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba84e-144">INPUTS</span></span>

### <span data-ttu-id="ba84e-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="ba84e-145">None</span></span>
<span data-ttu-id="ba84e-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ba84e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba84e-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba84e-147">OUTPUTS</span></span>

### <span data-ttu-id="ba84e-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ba84e-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="ba84e-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba84e-149">NOTES</span></span>

## <span data-ttu-id="ba84e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba84e-150">RELATED LINKS</span></span>

[<span data-ttu-id="ba84e-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ba84e-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ba84e-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ba84e-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ba84e-153">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ba84e-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ba84e-154">Ångra-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="ba84e-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
