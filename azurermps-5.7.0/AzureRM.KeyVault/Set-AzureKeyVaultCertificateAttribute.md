---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573423"
---
# <span data-ttu-id="c457d-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="c457d-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="c457d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c457d-102">SYNOPSIS</span></span>
<span data-ttu-id="c457d-103">Ändrar redigerbara attribut i ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="c457d-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c457d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c457d-104">SYNTAX</span></span>

### <span data-ttu-id="c457d-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c457d-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c457d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c457d-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c457d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c457d-107">DESCRIPTION</span></span>
<span data-ttu-id="c457d-108">Cmdleten **set-AzureKeyVaultCertificateAttribute** ändrar ett certifikats redigerbara attribut.</span><span class="sxs-lookup"><span data-stu-id="c457d-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="c457d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c457d-109">EXAMPLES</span></span>

### <span data-ttu-id="c457d-110">Exempel 1: ändra de taggar som associeras med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c457d-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="c457d-111">Det första kommandot tilldelar en matris med tangentkombinationer till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="c457d-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="c457d-112">Det andra kommandot anger värdet för taggen TestCert01 för att vara $Tags.</span><span class="sxs-lookup"><span data-stu-id="c457d-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="c457d-113">Det sista kommandot visar TestCert01-certifikatet genom att använda Get-AzureKeyVaultCertificate cmdlet för att verifiera åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c457d-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="c457d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c457d-114">PARAMETERS</span></span>

### <span data-ttu-id="c457d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c457d-115">-DefaultProfile</span></span>
<span data-ttu-id="c457d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c457d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c457d-117">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="c457d-117">-Enable</span></span>
<span data-ttu-id="c457d-118">Anger om ett certifikat ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="c457d-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="c457d-119">Ange $True som ska aktive ras eller $Falseas.</span><span class="sxs-lookup"><span data-stu-id="c457d-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c457d-120">-InputObject</span></span>
<span data-ttu-id="c457d-121">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="c457d-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c457d-122">-Name</span></span>
<span data-ttu-id="c457d-123">Anger namnet på det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c457d-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="c457d-124">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="c457d-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c457d-125">-PassThru</span></span>
<span data-ttu-id="c457d-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c457d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c457d-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c457d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c457d-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c457d-128">-Tag</span></span>
<span data-ttu-id="c457d-129">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c457d-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c457d-130">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c457d-130">For example:</span></span>

<span data-ttu-id="c457d-131">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c457d-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c457d-132">-VaultName</span></span>
<span data-ttu-id="c457d-133">Anger namnet på den Key valv som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="c457d-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="c457d-134">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="c457d-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-135">-Version</span><span class="sxs-lookup"><span data-stu-id="c457d-135">-Version</span></span>
<span data-ttu-id="c457d-136">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="c457d-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="c457d-137">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="c457d-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c457d-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c457d-138">-Confirm</span></span>
<span data-ttu-id="c457d-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c457d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c457d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c457d-140">-WhatIf</span></span>
<span data-ttu-id="c457d-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c457d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c457d-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c457d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c457d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c457d-143">CommonParameters</span></span>
<span data-ttu-id="c457d-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c457d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c457d-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c457d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c457d-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c457d-146">INPUTS</span></span>

### <span data-ttu-id="c457d-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="c457d-147">None</span></span>
<span data-ttu-id="c457d-148">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c457d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c457d-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c457d-149">OUTPUTS</span></span>

### <span data-ttu-id="c457d-150">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c457d-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="c457d-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c457d-151">NOTES</span></span>

## <span data-ttu-id="c457d-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c457d-152">RELATED LINKS</span></span>

[<span data-ttu-id="c457d-153">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c457d-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
