---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922670"
---
# <span data-ttu-id="ae295-101">Set-AzKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="ae295-101">Set-AzKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="ae295-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae295-102">SYNOPSIS</span></span>
<span data-ttu-id="ae295-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="ae295-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ae295-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae295-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae295-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae295-105">DESCRIPTION</span></span>
<span data-ttu-id="ae295-106">Cmdleten **set-AzKeyVaultSecretAttribute** uppdaterar redigerbara attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="ae295-106">The **Set-AzKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ae295-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae295-107">EXAMPLES</span></span>

### <span data-ttu-id="ae295-108">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="ae295-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="ae295-109">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="ae295-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="ae295-110">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="ae295-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="ae295-111">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="ae295-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="ae295-112">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="ae295-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae295-113">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="ae295-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="ae295-114">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="ae295-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="ae295-115">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="ae295-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="ae295-116">I det tredje kommandot används cmdleten Get-AzKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="ae295-116">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="ae295-117">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="ae295-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="ae295-118">Kommandot rör den hemlighet som matchar filtret för Set-AzKeyVaultSecretAttribute cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="ae295-118">The command pipes the secrets that match the filter to the Set-AzKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="ae295-119">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="ae295-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="ae295-120">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="ae295-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="ae295-121">Med det fjärde kommandot används cmdleten Get-AzKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Set-AzKeyVaultSecretAttribute-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae295-121">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="ae295-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae295-122">PARAMETERS</span></span>

### <span data-ttu-id="ae295-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ae295-123">-ContentType</span></span>
<span data-ttu-id="ae295-124">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="ae295-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="ae295-125">Om du inte anger den här parametern ändras inte den aktuella hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="ae295-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="ae295-126">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="ae295-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="ae295-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae295-127">-DefaultProfile</span></span>
<span data-ttu-id="ae295-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ae295-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae295-129">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="ae295-129">-Enable</span></span>
<span data-ttu-id="ae295-130">Anger om en hemlighet ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="ae295-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="ae295-131">Ange $False om du vill inaktivera en hemlig hemlighet eller $True för att aktivera en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="ae295-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="ae295-132">Om du inte anger den här parametern ändras inte den aktuella hemlighetens aktiverade eller inaktiverade status.</span><span class="sxs-lookup"><span data-stu-id="ae295-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="ae295-133">-Upphör</span><span class="sxs-lookup"><span data-stu-id="ae295-133">-Expires</span></span>
<span data-ttu-id="ae295-134">Anger det datum och den tid då en hemlig hemlighet upphör.</span><span class="sxs-lookup"><span data-stu-id="ae295-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="ae295-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae295-135">-Name</span></span>
<span data-ttu-id="ae295-136">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="ae295-136">Specifies the name of a secret.</span></span> <span data-ttu-id="ae295-137">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="ae295-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae295-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ae295-138">-NotBefore</span></span>
<span data-ttu-id="ae295-139">Anger den koordinerade universella tiden (UTC) innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="ae295-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="ae295-140">Om du inte anger den här parametern ändras inte den aktuella hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="ae295-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="ae295-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae295-141">-PassThru</span></span>
<span data-ttu-id="ae295-142">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ae295-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae295-143">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ae295-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae295-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ae295-144">-Tag</span></span>
<span data-ttu-id="ae295-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ae295-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae295-146">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ae295-146">For example:</span></span>

<span data-ttu-id="ae295-147">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ae295-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae295-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae295-148">-VaultName</span></span>
<span data-ttu-id="ae295-149">Anger namnet på det Key-valv som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ae295-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="ae295-150">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="ae295-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="ae295-151">-Version</span><span class="sxs-lookup"><span data-stu-id="ae295-151">-Version</span></span>
<span data-ttu-id="ae295-152">Anger vilken version av en hemlighet du har.</span><span class="sxs-lookup"><span data-stu-id="ae295-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="ae295-153">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ae295-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="ae295-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae295-154">-Confirm</span></span>
<span data-ttu-id="ae295-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae295-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae295-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae295-156">-WhatIf</span></span>
<span data-ttu-id="ae295-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae295-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae295-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae295-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae295-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae295-159">CommonParameters</span></span>
<span data-ttu-id="ae295-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae295-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae295-161">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae295-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae295-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae295-162">INPUTS</span></span>

### <span data-ttu-id="ae295-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae295-163">None</span></span>
<span data-ttu-id="ae295-164">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ae295-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae295-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae295-165">OUTPUTS</span></span>

### <span data-ttu-id="ae295-166">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="ae295-166">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="ae295-167">Returnerar Microsoft. Azure. commands. nyckel valv. Models. Secret-objekt om PassThru har angetts.</span><span class="sxs-lookup"><span data-stu-id="ae295-167">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="ae295-168">Annars returnerar nej.</span><span class="sxs-lookup"><span data-stu-id="ae295-168">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="ae295-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae295-169">NOTES</span></span>

## <span data-ttu-id="ae295-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae295-170">RELATED LINKS</span></span>

[<span data-ttu-id="ae295-171">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae295-171">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="ae295-172">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae295-172">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="ae295-173">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae295-173">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
