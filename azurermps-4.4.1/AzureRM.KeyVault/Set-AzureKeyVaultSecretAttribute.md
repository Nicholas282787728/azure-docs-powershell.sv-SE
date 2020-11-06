---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://go.microsoft.com/fwlink/?LinkId=690305
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: 9d9bd8a14b3a24d6001a7f1c2663b05a1e427f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584679"
---
# <span data-ttu-id="c3f42-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="c3f42-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="c3f42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3f42-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f42-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="c3f42-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3f42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3f42-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3f42-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f42-106">Cmdleten **set-AzureKeyVaultSecretAttribute** uppdaterar redigerbara attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="c3f42-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="c3f42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3f42-107">EXAMPLES</span></span>

### <span data-ttu-id="c3f42-108">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="c3f42-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="c3f42-109">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="c3f42-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="c3f42-110">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="c3f42-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="c3f42-111">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="c3f42-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="c3f42-112">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="c3f42-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="c3f42-113">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="c3f42-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="c3f42-114">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="c3f42-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="c3f42-115">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="c3f42-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="c3f42-116">I det tredje kommandot används cmdleten Get-AzureKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="c3f42-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="c3f42-117">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="c3f42-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="c3f42-118">Kommandot rör den hemlighet som matchar filtret för Set-AzureKeyVaultSecretAttribute cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="c3f42-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="c3f42-119">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="c3f42-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="c3f42-120">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="c3f42-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="c3f42-121">Med det fjärde kommandot används cmdleten Get-AzureKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Set-AzureKeyVaultSecretAttribute-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3f42-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="c3f42-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3f42-122">PARAMETERS</span></span>

### <span data-ttu-id="c3f42-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3f42-123">-Confirm</span></span>
<span data-ttu-id="c3f42-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3f42-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f42-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c3f42-125">-ContentType</span></span>
<span data-ttu-id="c3f42-126">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="c3f42-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="c3f42-127">Om du inte anger den här parametern ändras inte den aktuella hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="c3f42-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="c3f42-128">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="c3f42-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-129">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="c3f42-129">-Enable</span></span>
<span data-ttu-id="c3f42-130">Anger om en hemlighet ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="c3f42-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="c3f42-131">Ange $False om du vill inaktivera en hemlig hemlighet eller $True för att aktivera en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="c3f42-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="c3f42-132">Om du inte anger den här parametern ändras inte den aktuella hemlighetens aktiverade eller inaktiverade status.</span><span class="sxs-lookup"><span data-stu-id="c3f42-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="c3f42-133">-Upphör</span><span class="sxs-lookup"><span data-stu-id="c3f42-133">-Expires</span></span>
<span data-ttu-id="c3f42-134">Anger det datum och den tid då en hemlig hemlighet upphör.</span><span class="sxs-lookup"><span data-stu-id="c3f42-134">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3f42-135">-Name</span></span>
<span data-ttu-id="c3f42-136">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="c3f42-136">Specifies the name of a secret.</span></span> <span data-ttu-id="c3f42-137">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="c3f42-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="c3f42-138">-NotBefore</span></span>
<span data-ttu-id="c3f42-139">Anger den koordinerade universella tiden (UTC) innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="c3f42-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="c3f42-140">Om du inte anger den här parametern ändras inte den aktuella hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="c3f42-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3f42-141">-PassThru</span></span>
<span data-ttu-id="c3f42-142">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c3f42-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c3f42-143">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c3f42-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3f42-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c3f42-144">-Tag</span></span>
<span data-ttu-id="c3f42-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c3f42-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c3f42-146">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c3f42-146">For example:</span></span>

<span data-ttu-id="c3f42-147">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c3f42-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c3f42-148">-VaultName</span></span>
<span data-ttu-id="c3f42-149">Anger namnet på det Key-valv som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c3f42-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="c3f42-150">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="c3f42-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="c3f42-151">-Version</span><span class="sxs-lookup"><span data-stu-id="c3f42-151">-Version</span></span>
<span data-ttu-id="c3f42-152">Anger vilken version av en hemlighet du har.</span><span class="sxs-lookup"><span data-stu-id="c3f42-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="c3f42-153">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="c3f42-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f42-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f42-154">-WhatIf</span></span>
<span data-ttu-id="c3f42-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3f42-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f42-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3f42-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f42-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f42-157">-DefaultProfile</span></span>
<span data-ttu-id="c3f42-158">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f42-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f42-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f42-159">CommonParameters</span></span>
<span data-ttu-id="c3f42-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f42-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f42-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f42-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f42-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3f42-162">INPUTS</span></span>

## <span data-ttu-id="c3f42-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3f42-163">OUTPUTS</span></span>

### <span data-ttu-id="c3f42-164">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="c3f42-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="c3f42-165">Returnerar Microsoft. Azure. commands. nyckel valv. Models. Secret-objekt om PassThru har angetts.</span><span class="sxs-lookup"><span data-stu-id="c3f42-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="c3f42-166">Annars returnerar nej.</span><span class="sxs-lookup"><span data-stu-id="c3f42-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="c3f42-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3f42-167">NOTES</span></span>

## <span data-ttu-id="c3f42-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3f42-168">RELATED LINKS</span></span>

[<span data-ttu-id="c3f42-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c3f42-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="c3f42-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3f42-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="c3f42-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3f42-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
