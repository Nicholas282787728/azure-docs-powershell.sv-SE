---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088861"
---
# <span data-ttu-id="4ccd6-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4ccd6-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="4ccd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ccd6-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccd6-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="4ccd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ccd6-104">SYNTAX</span></span>

### <span data-ttu-id="4ccd6-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="4ccd6-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ccd6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ccd6-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ccd6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ccd6-107">DESCRIPTION</span></span>
<span data-ttu-id="4ccd6-108">**Update-AzKeyVaultSecret** cmdlet uppdaterar redigerbara attribut i en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="4ccd6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ccd6-109">EXAMPLES</span></span>

### <span data-ttu-id="4ccd6-110">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="4ccd6-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="4ccd6-111">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="4ccd6-112">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="4ccd6-113">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="4ccd6-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="4ccd6-114">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="4ccd6-115">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="4ccd6-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="4ccd6-116">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="4ccd6-117">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="4ccd6-118">I det tredje kommandot används cmdleten Get-AzKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="4ccd6-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="4ccd6-119">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="4ccd6-120">Kommandot rör den hemlighet som matchar filtret för Update-AzKeyVaultSecret cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="4ccd6-121">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="4ccd6-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="4ccd6-122">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="4ccd6-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="4ccd6-123">Med det fjärde kommandot används cmdleten Get-AzKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Update-AzKeyVaultSecret-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="4ccd6-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ccd6-124">PARAMETERS</span></span>

### <span data-ttu-id="4ccd6-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4ccd6-125">-ContentType</span></span>
<span data-ttu-id="4ccd6-126">Hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-126">Secret's content type.</span></span>
<span data-ttu-id="4ccd6-127">Om det inte anges ändras inte det befintliga värdet för hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="4ccd6-128">Ta bort det befintliga innehålls typs värdet genom att ange en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccd6-129">-DefaultProfile</span></span>
<span data-ttu-id="4ccd6-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ccd6-131">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="4ccd6-131">-Enable</span></span>
<span data-ttu-id="4ccd6-132">Om det finns någon kan du aktivera en hemlighet om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="4ccd6-133">Inaktivera en hemlighet om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="4ccd6-134">Om det inte anges ändras inte det befintliga värdet för hemlighetens aktiverade/inaktiverade läge.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="4ccd6-135">-Upphör</span><span class="sxs-lookup"><span data-stu-id="4ccd6-135">-Expires</span></span>
<span data-ttu-id="4ccd6-136">Förfallo tid för en hemlighet i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="4ccd6-137">Om inget anges ändras inte det befintliga värdet för hemlighetens förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ccd6-138">-InputObject</span></span>
<span data-ttu-id="4ccd6-139">Hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="4ccd6-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ccd6-140">-Name</span></span>
<span data-ttu-id="4ccd6-141">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-141">Secret name.</span></span>
<span data-ttu-id="4ccd6-142">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="4ccd6-143">-NotBefore</span></span>
<span data-ttu-id="4ccd6-144">UTC-tiden innan hemligheten kan inte användas.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="4ccd6-145">Om det inte anges ändras inte det befintliga värdet för hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ccd6-146">-PassThru</span></span>
<span data-ttu-id="4ccd6-147">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="4ccd6-148">Om den här växeln anges returneras hemliga objekt.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="4ccd6-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4ccd6-149">-Tag</span></span>
<span data-ttu-id="4ccd6-150">En hash som representerar hemliga taggar.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="4ccd6-151">Om det inte anges ändras inte de befintliga taggarna för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="4ccd6-152">Ta bort en tagg genom att ange en tom hash.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ccd6-153">-VaultName</span></span>
<span data-ttu-id="4ccd6-154">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-154">Vault name.</span></span>
<span data-ttu-id="4ccd6-155">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-156">-Version</span><span class="sxs-lookup"><span data-stu-id="4ccd6-156">-Version</span></span>
<span data-ttu-id="4ccd6-157">Hemlig version.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-157">Secret version.</span></span>
<span data-ttu-id="4ccd6-158">Cmdlet konstruerar FQDN för en hemlighet från valv namnet, den valda miljön, det hemliga namnet och hemlighet-versionen.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ccd6-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ccd6-159">-Confirm</span></span>
<span data-ttu-id="4ccd6-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ccd6-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ccd6-161">-WhatIf</span></span>
<span data-ttu-id="4ccd6-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ccd6-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ccd6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccd6-164">CommonParameters</span></span>
<span data-ttu-id="4ccd6-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ccd6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccd6-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ccd6-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccd6-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ccd6-167">INPUTS</span></span>

### <span data-ttu-id="4ccd6-168">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4ccd6-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="4ccd6-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ccd6-169">OUTPUTS</span></span>

### <span data-ttu-id="4ccd6-170">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4ccd6-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="4ccd6-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ccd6-171">NOTES</span></span>

## <span data-ttu-id="4ccd6-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ccd6-172">RELATED LINKS</span></span>