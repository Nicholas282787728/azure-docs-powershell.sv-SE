---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757935"
---
# <span data-ttu-id="98b50-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="98b50-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="98b50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98b50-102">SYNOPSIS</span></span>
<span data-ttu-id="98b50-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="98b50-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98b50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98b50-104">SYNTAX</span></span>

### <span data-ttu-id="98b50-105">Vis</span><span class="sxs-lookup"><span data-stu-id="98b50-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b50-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98b50-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98b50-107">DESCRIPTION</span></span>
<span data-ttu-id="98b50-108">Cmdleten **set-AzureKeyVaultSecretAttribute** uppdaterar redigerbara attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="98b50-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="98b50-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98b50-109">EXAMPLES</span></span>

### <span data-ttu-id="98b50-110">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="98b50-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="98b50-111">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="98b50-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="98b50-112">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="98b50-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="98b50-113">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="98b50-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="98b50-114">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="98b50-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="98b50-115">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="98b50-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="98b50-116">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="98b50-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="98b50-117">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="98b50-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="98b50-118">I det tredje kommandot används cmdleten Get-AzureKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="98b50-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="98b50-119">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="98b50-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="98b50-120">Kommandot rör den hemlighet som matchar filtret för Set-AzureKeyVaultSecretAttribute cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="98b50-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="98b50-121">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="98b50-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="98b50-122">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="98b50-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="98b50-123">Med det fjärde kommandot används cmdleten Get-AzureKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Set-AzureKeyVaultSecretAttribute-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b50-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="98b50-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98b50-124">PARAMETERS</span></span>

### <span data-ttu-id="98b50-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="98b50-125">-ContentType</span></span>
<span data-ttu-id="98b50-126">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="98b50-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="98b50-127">Om du inte anger den här parametern ändras inte den aktuella hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="98b50-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="98b50-128">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="98b50-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b50-129">-DefaultProfile</span></span>
<span data-ttu-id="98b50-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="98b50-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98b50-131">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="98b50-131">-Enable</span></span>
<span data-ttu-id="98b50-132">Anger om en hemlighet ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="98b50-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="98b50-133">Ange $False om du vill inaktivera en hemlig hemlighet eller $True för att aktivera en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="98b50-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="98b50-134">Om du inte anger den här parametern ändras inte den aktuella hemlighetens aktiverade eller inaktiverade status.</span><span class="sxs-lookup"><span data-stu-id="98b50-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="98b50-135">-Upphör</span><span class="sxs-lookup"><span data-stu-id="98b50-135">-Expires</span></span>
<span data-ttu-id="98b50-136">Anger det datum och den tid då en hemlig hemlighet upphör.</span><span class="sxs-lookup"><span data-stu-id="98b50-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b50-137">-InputObject</span></span>
<span data-ttu-id="98b50-138">Hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="98b50-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="98b50-139">-Name</span></span>
<span data-ttu-id="98b50-140">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="98b50-140">Specifies the name of a secret.</span></span> <span data-ttu-id="98b50-141">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="98b50-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="98b50-142">-NotBefore</span></span>
<span data-ttu-id="98b50-143">Anger den koordinerade universella tiden (UTC) innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="98b50-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="98b50-144">Om du inte anger den här parametern ändras inte den aktuella hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="98b50-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98b50-145">-PassThru</span></span>
<span data-ttu-id="98b50-146">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="98b50-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="98b50-147">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="98b50-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98b50-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="98b50-148">-Tag</span></span>
<span data-ttu-id="98b50-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="98b50-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="98b50-150">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="98b50-150">For example:</span></span>

<span data-ttu-id="98b50-151">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="98b50-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98b50-152">-VaultName</span></span>
<span data-ttu-id="98b50-153">Anger namnet på det Key-valv som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="98b50-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="98b50-154">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="98b50-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-155">-Version</span><span class="sxs-lookup"><span data-stu-id="98b50-155">-Version</span></span>
<span data-ttu-id="98b50-156">Anger vilken version av en hemlighet du har.</span><span class="sxs-lookup"><span data-stu-id="98b50-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="98b50-157">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="98b50-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b50-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98b50-158">-Confirm</span></span>
<span data-ttu-id="98b50-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98b50-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b50-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b50-160">-WhatIf</span></span>
<span data-ttu-id="98b50-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98b50-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b50-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98b50-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b50-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b50-163">CommonParameters</span></span>
<span data-ttu-id="98b50-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b50-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b50-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b50-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b50-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98b50-166">INPUTS</span></span>

### <span data-ttu-id="98b50-167">Ingen</span><span class="sxs-lookup"><span data-stu-id="98b50-167">None</span></span>
<span data-ttu-id="98b50-168">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="98b50-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98b50-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98b50-169">OUTPUTS</span></span>

### <span data-ttu-id="98b50-170">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="98b50-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="98b50-171">Returnerar Microsoft. Azure. commands. nyckel valv. Models. Secret-objekt om PassThru har angetts.</span><span class="sxs-lookup"><span data-stu-id="98b50-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="98b50-172">Annars returnerar nej.</span><span class="sxs-lookup"><span data-stu-id="98b50-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="98b50-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98b50-173">NOTES</span></span>

## <span data-ttu-id="98b50-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98b50-174">RELATED LINKS</span></span>

[<span data-ttu-id="98b50-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98b50-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="98b50-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="98b50-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="98b50-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="98b50-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
