---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924437"
---
# <span data-ttu-id="3110c-101">Set-AzKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="3110c-101">Set-AzKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="3110c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3110c-102">SYNOPSIS</span></span>
<span data-ttu-id="3110c-103">Ändrar redigerbara attribut i ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="3110c-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="3110c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3110c-104">SYNTAX</span></span>

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3110c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3110c-105">DESCRIPTION</span></span>
<span data-ttu-id="3110c-106">Cmdleten **set-AzKeyVaultCertificateAttribute** ändrar ett certifikats redigerbara attribut.</span><span class="sxs-lookup"><span data-stu-id="3110c-106">The **Set-AzKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="3110c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3110c-107">EXAMPLES</span></span>

### <span data-ttu-id="3110c-108">Exempel 1: ändra de taggar som associeras med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="3110c-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="3110c-109">Det första kommandot tilldelar en matris med tangentkombinationer till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="3110c-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="3110c-110">Det andra kommandot anger värdet för taggen TestCert01 för att vara $Tags.</span><span class="sxs-lookup"><span data-stu-id="3110c-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="3110c-111">Det sista kommandot visar TestCert01-certifikatet genom att använda Get-AzKeyVaultCertificate cmdlet för att verifiera åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3110c-111">The final command displays the TestCert01 certificate by using the Get-AzKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="3110c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3110c-112">PARAMETERS</span></span>

### <span data-ttu-id="3110c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3110c-113">-DefaultProfile</span></span>
<span data-ttu-id="3110c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3110c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3110c-115">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="3110c-115">-Enable</span></span>
<span data-ttu-id="3110c-116">Anger om ett certifikat ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="3110c-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="3110c-117">Ange $True som ska aktive ras eller $Falseas.</span><span class="sxs-lookup"><span data-stu-id="3110c-117">Specify $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="3110c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3110c-118">-Name</span></span>
<span data-ttu-id="3110c-119">Anger namnet på det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="3110c-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="3110c-120">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="3110c-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3110c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3110c-121">-PassThru</span></span>
<span data-ttu-id="3110c-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3110c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3110c-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3110c-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3110c-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3110c-124">-Tag</span></span>
<span data-ttu-id="3110c-125">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3110c-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3110c-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3110c-126">For example:</span></span>

<span data-ttu-id="3110c-127">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3110c-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3110c-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3110c-128">-VaultName</span></span>
<span data-ttu-id="3110c-129">Anger namnet på den Key valv som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="3110c-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="3110c-130">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="3110c-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3110c-131">-Version</span><span class="sxs-lookup"><span data-stu-id="3110c-131">-Version</span></span>
<span data-ttu-id="3110c-132">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="3110c-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="3110c-133">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="3110c-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="3110c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3110c-134">-Confirm</span></span>
<span data-ttu-id="3110c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3110c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3110c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3110c-136">-WhatIf</span></span>
<span data-ttu-id="3110c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3110c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3110c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3110c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3110c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3110c-139">CommonParameters</span></span>
<span data-ttu-id="3110c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3110c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3110c-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3110c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3110c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3110c-142">INPUTS</span></span>

### <span data-ttu-id="3110c-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="3110c-143">None</span></span>
<span data-ttu-id="3110c-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3110c-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3110c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3110c-145">OUTPUTS</span></span>

### <span data-ttu-id="3110c-146">Microsoft. Azure. commands. valv. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3110c-146">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="3110c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3110c-147">NOTES</span></span>

## <span data-ttu-id="3110c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3110c-148">RELATED LINKS</span></span>

[<span data-ttu-id="3110c-149">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3110c-149">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)
