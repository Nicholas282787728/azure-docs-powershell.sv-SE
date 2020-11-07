---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 7c3ad97a2896104d9c60c1e24b7ea844b3a090a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916194"
---
# <span data-ttu-id="34f46-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="34f46-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="34f46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34f46-102">SYNOPSIS</span></span>
<span data-ttu-id="34f46-103">Ändrar redigerbara attribut i ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="34f46-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="34f46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34f46-104">SYNTAX</span></span>

### <span data-ttu-id="34f46-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="34f46-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34f46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="34f46-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34f46-107">DESCRIPTION</span></span>
<span data-ttu-id="34f46-108">Cmdleten **Update-AzKeyVaultCertificate** ändrar ett certifikats redigerbara attribut.</span><span class="sxs-lookup"><span data-stu-id="34f46-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="34f46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34f46-109">EXAMPLES</span></span>

### <span data-ttu-id="34f46-110">Exempel 1: ändra de taggar som associeras med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="34f46-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="34f46-111">Det första kommandot tilldelar en matris med tangentkombinationer till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="34f46-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="34f46-112">Det andra kommandot anger värdet för taggen TestCert01 för att vara $Tags.</span><span class="sxs-lookup"><span data-stu-id="34f46-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="34f46-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34f46-113">PARAMETERS</span></span>

### <span data-ttu-id="34f46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f46-114">-DefaultProfile</span></span>
<span data-ttu-id="34f46-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34f46-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f46-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="34f46-116">-Enable</span></span>
<span data-ttu-id="34f46-117">Om det finns något aktiverar du ett certifikat om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="34f46-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="34f46-118">Inaktivera ett certifikat om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="34f46-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="34f46-119">Om det inte anges ändras inte det befintliga värdet i certifikatets aktiverade/inaktiverade läge.</span><span class="sxs-lookup"><span data-stu-id="34f46-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="34f46-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f46-120">-InputObject</span></span>
<span data-ttu-id="34f46-121">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="34f46-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f46-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="34f46-122">-Name</span></span>
<span data-ttu-id="34f46-123">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="34f46-123">Certificate name.</span></span>
<span data-ttu-id="34f46-124">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="34f46-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f46-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34f46-125">-PassThru</span></span>
<span data-ttu-id="34f46-126">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="34f46-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="34f46-127">Om denna växel anges returneras ett certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="34f46-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="34f46-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="34f46-128">-Tag</span></span>
<span data-ttu-id="34f46-129">En hash som representerar certifikat koder.</span><span class="sxs-lookup"><span data-stu-id="34f46-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="34f46-130">Om det inte anges ändras inte sertificate befintliga taggar.</span><span class="sxs-lookup"><span data-stu-id="34f46-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="34f46-131">Ta bort en tagg genom att ange en tom hash.</span><span class="sxs-lookup"><span data-stu-id="34f46-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f46-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="34f46-132">-VaultName</span></span>
<span data-ttu-id="34f46-133">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="34f46-133">Vault name.</span></span>
<span data-ttu-id="34f46-134">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="34f46-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f46-135">-Version</span><span class="sxs-lookup"><span data-stu-id="34f46-135">-Version</span></span>
<span data-ttu-id="34f46-136">Certifikat version.</span><span class="sxs-lookup"><span data-stu-id="34f46-136">Certificate version.</span></span>
<span data-ttu-id="34f46-137">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, den valda miljön, certifikat namnet och certifikat versionen.</span><span class="sxs-lookup"><span data-stu-id="34f46-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f46-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34f46-138">-Confirm</span></span>
<span data-ttu-id="34f46-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34f46-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f46-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f46-140">-WhatIf</span></span>
<span data-ttu-id="34f46-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34f46-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f46-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34f46-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f46-143">CommonParameters</span></span>
<span data-ttu-id="34f46-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f46-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f46-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f46-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34f46-146">INPUTS</span></span>

### <span data-ttu-id="34f46-147">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="34f46-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="34f46-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34f46-148">OUTPUTS</span></span>

### <span data-ttu-id="34f46-149">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="34f46-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="34f46-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34f46-150">NOTES</span></span>

## <span data-ttu-id="34f46-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34f46-151">RELATED LINKS</span></span>
