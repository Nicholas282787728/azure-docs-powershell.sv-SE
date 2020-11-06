---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://go.microsoft.com/fwlink/?LinkId=822861
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: b8dac56d55446915af1c9a2f00f71d903f3daf03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586511"
---
# <span data-ttu-id="e3a11-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="e3a11-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="e3a11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3a11-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a11-103">Ändrar redigerbara attribut i ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="e3a11-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3a11-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3a11-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a11-106">Cmdleten **set-AzureKeyVaultCertificateAttribute** ändrar ett certifikats redigerbara attribut.</span><span class="sxs-lookup"><span data-stu-id="e3a11-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="e3a11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3a11-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a11-108">Exempel 1: ändra de taggar som associeras med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="e3a11-108">Example 1: Modify the tags associated with a certificate</span></span>
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

<span data-ttu-id="e3a11-109">Det första kommandot tilldelar en matris med tangentkombinationer till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="e3a11-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="e3a11-110">Det andra kommandot anger värdet för taggen TestCert01 för att vara $Tags.</span><span class="sxs-lookup"><span data-stu-id="e3a11-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="e3a11-111">Det sista kommandot visar TestCert01-certifikatet genom att använda Get-AzureKeyVaultCertificate cmdlet för att verifiera åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="e3a11-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3a11-112">PARAMETERS</span></span>

### <span data-ttu-id="e3a11-113">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="e3a11-113">-Enable</span></span>
<span data-ttu-id="e3a11-114">Anger om ett certifikat ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="e3a11-114">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="e3a11-115">Ange $True som ska aktive ras eller $Falseas.</span><span class="sxs-lookup"><span data-stu-id="e3a11-115">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3a11-116">-Name</span></span>
<span data-ttu-id="e3a11-117">Anger namnet på det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e3a11-117">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="e3a11-118">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-118">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3a11-119">-PassThru</span></span>
<span data-ttu-id="e3a11-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e3a11-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3a11-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e3a11-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e3a11-122">-Tag</span></span>
<span data-ttu-id="e3a11-123">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e3a11-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e3a11-124">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e3a11-124">For example:</span></span>

<span data-ttu-id="e3a11-125">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e3a11-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e3a11-126">-VaultName</span></span>
<span data-ttu-id="e3a11-127">Anger namnet på den Key valv som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="e3a11-127">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="e3a11-128">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="e3a11-128">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-129">-Version</span><span class="sxs-lookup"><span data-stu-id="e3a11-129">-Version</span></span>
<span data-ttu-id="e3a11-130">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="e3a11-130">Specifies the version of a certificate.</span></span>
<span data-ttu-id="e3a11-131">Denna cmdlet konstruerar FQDN för ett certifikat baserat på namnet på Key Vault, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-131">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3a11-132">-Confirm</span></span>
<span data-ttu-id="e3a11-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3a11-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a11-134">-WhatIf</span></span>
<span data-ttu-id="e3a11-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3a11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a11-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3a11-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a11-137">-DefaultProfile</span></span>
<span data-ttu-id="e3a11-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a11-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a11-139">CommonParameters</span></span>
<span data-ttu-id="e3a11-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a11-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a11-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a11-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3a11-142">INPUTS</span></span>

## <span data-ttu-id="e3a11-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3a11-143">OUTPUTS</span></span>

### <span data-ttu-id="e3a11-144">Microsoft. Azure. commands. valv. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e3a11-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="e3a11-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3a11-145">NOTES</span></span>

## <span data-ttu-id="e3a11-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3a11-146">RELATED LINKS</span></span>

[<span data-ttu-id="e3a11-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e3a11-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
