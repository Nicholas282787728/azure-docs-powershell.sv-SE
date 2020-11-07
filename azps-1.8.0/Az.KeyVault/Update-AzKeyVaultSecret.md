---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 9a0e40716623b4d0b11f661ce859a0ee8787e685
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916166"
---
# <span data-ttu-id="b2f16-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b2f16-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b2f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2f16-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f16-103">Uppdaterar attribut för en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="b2f16-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b2f16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2f16-104">SYNTAX</span></span>

### <span data-ttu-id="b2f16-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="b2f16-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f16-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f16-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2f16-107">DESCRIPTION</span></span>
<span data-ttu-id="b2f16-108">**Update-AzKeyVaultSecret** cmdlet uppdaterar redigerbara attribut i en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="b2f16-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b2f16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2f16-109">EXAMPLES</span></span>

### <span data-ttu-id="b2f16-110">Exempel 1: ändra attributen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="b2f16-110">Example 1: Modify the attributes of a secret</span></span>
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

<span data-ttu-id="b2f16-111">De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.</span><span class="sxs-lookup"><span data-stu-id="b2f16-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="b2f16-112">Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.</span><span class="sxs-lookup"><span data-stu-id="b2f16-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="b2f16-113">Exempel 2: ta bort taggarna och innehålls typen för en hemlighet</span><span class="sxs-lookup"><span data-stu-id="b2f16-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="b2f16-114">Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="b2f16-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="b2f16-115">Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den</span><span class="sxs-lookup"><span data-stu-id="b2f16-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="b2f16-116">Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="b2f16-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="b2f16-117">Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.</span><span class="sxs-lookup"><span data-stu-id="b2f16-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="b2f16-118">I det tredje kommandot används cmdleten Get-AzKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** .</span><span class="sxs-lookup"><span data-stu-id="b2f16-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="b2f16-119">Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som.</span><span class="sxs-lookup"><span data-stu-id="b2f16-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="b2f16-120">Kommandot rör den hemlighet som matchar filtret för Update-AzKeyVaultSecret cmdlet som inaktiverar dem.</span><span class="sxs-lookup"><span data-stu-id="b2f16-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="b2f16-121">Exempel 4: Ange ContentType för alla versioner av en hemlighet</span><span class="sxs-lookup"><span data-stu-id="b2f16-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="b2f16-122">De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="b2f16-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="b2f16-123">Med det fjärde kommandot används cmdleten Get-AzKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Update-AzKeyVaultSecret-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2f16-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="b2f16-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2f16-124">PARAMETERS</span></span>

### <span data-ttu-id="b2f16-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b2f16-125">-ContentType</span></span>
<span data-ttu-id="b2f16-126">Hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="b2f16-126">Secret's content type.</span></span>
<span data-ttu-id="b2f16-127">Om det inte anges ändras inte det befintliga värdet för hemlighetens innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="b2f16-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="b2f16-128">Ta bort det befintliga innehålls typs värdet genom att ange en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="b2f16-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="b2f16-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f16-129">-DefaultProfile</span></span>
<span data-ttu-id="b2f16-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f16-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f16-131">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="b2f16-131">-Enable</span></span>
<span data-ttu-id="b2f16-132">Om det finns någon kan du aktivera en hemlighet om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="b2f16-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="b2f16-133">Inaktivera en hemlighet om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="b2f16-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="b2f16-134">Om det inte anges ändras inte det befintliga värdet för hemlighetens aktiverade/inaktiverade läge.</span><span class="sxs-lookup"><span data-stu-id="b2f16-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b2f16-135">-Upphör</span><span class="sxs-lookup"><span data-stu-id="b2f16-135">-Expires</span></span>
<span data-ttu-id="b2f16-136">Förfallo tid för en hemlighet i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="b2f16-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="b2f16-137">Om inget anges ändras inte det befintliga värdet för hemlighetens förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="b2f16-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="b2f16-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f16-138">-InputObject</span></span>
<span data-ttu-id="b2f16-139">Hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="b2f16-139">Secret object</span></span>

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

### <span data-ttu-id="b2f16-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2f16-140">-Name</span></span>
<span data-ttu-id="b2f16-141">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="b2f16-141">Secret name.</span></span>
<span data-ttu-id="b2f16-142">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="b2f16-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b2f16-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b2f16-143">-NotBefore</span></span>
<span data-ttu-id="b2f16-144">UTC-tiden innan hemligheten kan inte användas.</span><span class="sxs-lookup"><span data-stu-id="b2f16-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="b2f16-145">Om det inte anges ändras inte det befintliga värdet för hemlighetens NotBefore-attribut.</span><span class="sxs-lookup"><span data-stu-id="b2f16-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="b2f16-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2f16-146">-PassThru</span></span>
<span data-ttu-id="b2f16-147">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="b2f16-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="b2f16-148">Om den här växeln anges returneras hemliga objekt.</span><span class="sxs-lookup"><span data-stu-id="b2f16-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="b2f16-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b2f16-149">-Tag</span></span>
<span data-ttu-id="b2f16-150">En hash som representerar hemliga taggar.</span><span class="sxs-lookup"><span data-stu-id="b2f16-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="b2f16-151">Om det inte anges ändras inte de befintliga taggarna för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b2f16-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="b2f16-152">Ta bort en tagg genom att ange en tom hash.</span><span class="sxs-lookup"><span data-stu-id="b2f16-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="b2f16-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b2f16-153">-VaultName</span></span>
<span data-ttu-id="b2f16-154">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="b2f16-154">Vault name.</span></span>
<span data-ttu-id="b2f16-155">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="b2f16-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b2f16-156">-Version</span><span class="sxs-lookup"><span data-stu-id="b2f16-156">-Version</span></span>
<span data-ttu-id="b2f16-157">Hemlig version.</span><span class="sxs-lookup"><span data-stu-id="b2f16-157">Secret version.</span></span>
<span data-ttu-id="b2f16-158">Cmdlet konstruerar FQDN för en hemlighet från valv namnet, den valda miljön, det hemliga namnet och hemlighet-versionen.</span><span class="sxs-lookup"><span data-stu-id="b2f16-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="b2f16-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2f16-159">-Confirm</span></span>
<span data-ttu-id="b2f16-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2f16-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f16-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f16-161">-WhatIf</span></span>
<span data-ttu-id="b2f16-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2f16-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f16-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2f16-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f16-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f16-164">CommonParameters</span></span>
<span data-ttu-id="b2f16-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f16-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f16-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f16-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f16-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2f16-167">INPUTS</span></span>

### <span data-ttu-id="b2f16-168">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b2f16-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b2f16-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2f16-169">OUTPUTS</span></span>

### <span data-ttu-id="b2f16-170">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b2f16-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b2f16-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2f16-171">NOTES</span></span>

## <span data-ttu-id="b2f16-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2f16-172">RELATED LINKS</span></span>
