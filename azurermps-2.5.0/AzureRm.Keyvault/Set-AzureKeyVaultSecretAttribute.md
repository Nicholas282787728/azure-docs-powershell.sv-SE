---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928758"
---
# <span data-ttu-id="96758-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="96758-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="96758-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96758-102">SYNOPSIS</span></span>
<span data-ttu-id="96758-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="96758-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96758-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96758-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96758-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96758-105">DESCRIPTION</span></span>
<span data-ttu-id="96758-106">Cmdleten **set-AzureKeyVaultSecretAttribute** uppdaterar redigerbara attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="96758-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="96758-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96758-107">EXAMPLES</span></span>

### <span data-ttu-id="96758-108">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="96758-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="96758-109">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="96758-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="96758-110">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="96758-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="96758-111">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="96758-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="96758-112">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="96758-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="96758-113">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="96758-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="96758-114">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="96758-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="96758-115">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="96758-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="96758-116">I det tredje kommandot används cmdleten Get-AzureKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="96758-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="96758-117">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="96758-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="96758-118">Kommandot rör den hemlighet som matchar filtret för Set-AzureKeyVaultSecretAttribute cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="96758-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="96758-119">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="96758-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="96758-120">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="96758-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="96758-121">Med det fjärde kommandot används cmdleten Get-AzureKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Set-AzureKeyVaultSecretAttribute-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96758-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="96758-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96758-122">PARAMETERS</span></span>

### <span data-ttu-id="96758-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="96758-123">-ContentType</span></span>
<span data-ttu-id="96758-124">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="96758-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="96758-125">Om du inte anger den här parametern ändras inte den aktuella hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="96758-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="96758-126">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="96758-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="96758-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96758-127">-DefaultProfile</span></span>
<span data-ttu-id="96758-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="96758-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96758-129">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="96758-129">-Enable</span></span>
<span data-ttu-id="96758-130">Anger om en hemlighet ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="96758-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="96758-131">Ange $False om du vill inaktivera en hemlig hemlighet eller $True för att aktivera en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="96758-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="96758-132">Om du inte anger den här parametern ändras inte den aktuella hemlighetens aktiverade eller inaktiverade status.</span><span class="sxs-lookup"><span data-stu-id="96758-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="96758-133">-Upphör</span><span class="sxs-lookup"><span data-stu-id="96758-133">-Expires</span></span>
<span data-ttu-id="96758-134">Anger det datum och den tid då en hemlig hemlighet upphör.</span><span class="sxs-lookup"><span data-stu-id="96758-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="96758-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="96758-135">-Name</span></span>
<span data-ttu-id="96758-136">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="96758-136">Specifies the name of a secret.</span></span> <span data-ttu-id="96758-137">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="96758-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="96758-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="96758-138">-NotBefore</span></span>
<span data-ttu-id="96758-139">Anger den koordinerade universella tiden (UTC) innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="96758-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="96758-140">Om du inte anger den här parametern ändras inte den aktuella hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="96758-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="96758-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96758-141">-PassThru</span></span>
<span data-ttu-id="96758-142">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="96758-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96758-143">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="96758-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96758-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="96758-144">-Tag</span></span>
<span data-ttu-id="96758-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="96758-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="96758-146">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="96758-146">For example:</span></span>

<span data-ttu-id="96758-147">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="96758-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="96758-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="96758-148">-VaultName</span></span>
<span data-ttu-id="96758-149">Anger namnet på det Key-valv som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="96758-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="96758-150">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="96758-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="96758-151">-Version</span><span class="sxs-lookup"><span data-stu-id="96758-151">-Version</span></span>
<span data-ttu-id="96758-152">Anger vilken version av en hemlighet du har.</span><span class="sxs-lookup"><span data-stu-id="96758-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="96758-153">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="96758-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="96758-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96758-154">-Confirm</span></span>
<span data-ttu-id="96758-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96758-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96758-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96758-156">-WhatIf</span></span>
<span data-ttu-id="96758-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96758-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96758-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96758-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96758-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96758-159">CommonParameters</span></span>
<span data-ttu-id="96758-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96758-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96758-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96758-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96758-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96758-162">INPUTS</span></span>

## <span data-ttu-id="96758-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96758-163">OUTPUTS</span></span>

### <span data-ttu-id="96758-164">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="96758-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="96758-165">Returnerar Microsoft. Azure. commands. nyckel valv. Models. Secret-objekt om PassThru har angetts.</span><span class="sxs-lookup"><span data-stu-id="96758-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="96758-166">Annars returnerar nej.</span><span class="sxs-lookup"><span data-stu-id="96758-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="96758-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96758-167">NOTES</span></span>

## <span data-ttu-id="96758-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96758-168">RELATED LINKS</span></span>

[<span data-ttu-id="96758-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96758-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="96758-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96758-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="96758-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96758-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
