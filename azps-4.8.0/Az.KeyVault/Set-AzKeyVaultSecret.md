---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259611"
---
# <span data-ttu-id="6538e-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6538e-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6538e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6538e-102">SYNOPSIS</span></span>
<span data-ttu-id="6538e-103">Skapar eller uppdaterar en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="6538e-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="6538e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6538e-104">SYNTAX</span></span>

### <span data-ttu-id="6538e-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="6538e-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6538e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6538e-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6538e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6538e-107">DESCRIPTION</span></span>
<span data-ttu-id="6538e-108">Cmdleten **set-AzKeyVaultSecret** skapar eller uppdaterar en hemlighet i ett nyckel valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6538e-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="6538e-109">Om det inte finns någon hemlighet skapar den här cmdleten den.</span><span class="sxs-lookup"><span data-stu-id="6538e-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="6538e-110">Om det redan finns en hemlighet skapar den här cmdleten en ny version av den hemligheten.</span><span class="sxs-lookup"><span data-stu-id="6538e-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="6538e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6538e-111">EXAMPLES</span></span>

### <span data-ttu-id="6538e-112">Exempel 1: ändra värdet för en hemlighet som använder standardattribut</span><span class="sxs-lookup"><span data-stu-id="6538e-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="6538e-113">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Secret variabel.</span><span class="sxs-lookup"><span data-stu-id="6538e-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6538e-114">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6538e-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6538e-115">Det andra kommandot ändrar värdet för hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="6538e-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="6538e-116">Det hemliga värdet blir det värde som lagras i $Secret.</span><span class="sxs-lookup"><span data-stu-id="6538e-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="6538e-117">Exempel 2: ändra värdet för en hemlighet med anpassade attribut</span><span class="sxs-lookup"><span data-stu-id="6538e-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="6538e-118">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Secret variabel.</span><span class="sxs-lookup"><span data-stu-id="6538e-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6538e-119">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6538e-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6538e-120">Nästa kommando definierar anpassade attribut för utgångs datum, taggar och kontext typ och lagrar attribut i variabler.</span><span class="sxs-lookup"><span data-stu-id="6538e-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="6538e-121">Det slutliga kommandot ändrar värdena för hemligheten som heter ITSecret i nyckel valvet contoso med de värden som anges tidigare som variabler.</span><span class="sxs-lookup"><span data-stu-id="6538e-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="6538e-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6538e-122">PARAMETERS</span></span>

### <span data-ttu-id="6538e-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6538e-123">-ContentType</span></span>
<span data-ttu-id="6538e-124">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="6538e-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="6538e-125">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="6538e-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="6538e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6538e-126">-DefaultProfile</span></span>
<span data-ttu-id="6538e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6538e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6538e-128">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="6538e-128">-Disable</span></span>
<span data-ttu-id="6538e-129">Anger att denna cmdlet inaktiverar en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="6538e-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="6538e-130">-Upphör</span><span class="sxs-lookup"><span data-stu-id="6538e-130">-Expires</span></span>
<span data-ttu-id="6538e-131">Anger förfallo tid, som ett **datetime** -objekt, för den hemlighet som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="6538e-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="6538e-132">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="6538e-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="6538e-133">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6538e-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="6538e-134">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6538e-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="6538e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6538e-135">-InputObject</span></span>
<span data-ttu-id="6538e-136">Hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="6538e-136">Secret object</span></span>

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

### <span data-ttu-id="6538e-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="6538e-137">-Name</span></span>
<span data-ttu-id="6538e-138">Anger namnet på en hemlighet som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="6538e-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="6538e-139">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="6538e-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="6538e-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6538e-140">-NotBefore</span></span>
<span data-ttu-id="6538e-141">Anger tiden, som ett **datetime** -objekt, innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="6538e-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="6538e-142">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="6538e-142">This parameter uses UTC.</span></span> <span data-ttu-id="6538e-143">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6538e-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="6538e-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="6538e-144">-SecretValue</span></span>
<span data-ttu-id="6538e-145">Anger värdet för hemligheten som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6538e-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="6538e-146">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="6538e-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="6538e-147">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6538e-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6538e-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6538e-148">-Tag</span></span>
<span data-ttu-id="6538e-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6538e-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6538e-150">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6538e-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6538e-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6538e-151">-VaultName</span></span>
<span data-ttu-id="6538e-152">Anger namnet på det nyckel valv som den här hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="6538e-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="6538e-153">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="6538e-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="6538e-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6538e-154">-Confirm</span></span>
<span data-ttu-id="6538e-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6538e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6538e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6538e-156">-WhatIf</span></span>
<span data-ttu-id="6538e-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6538e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6538e-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6538e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6538e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6538e-159">CommonParameters</span></span>
<span data-ttu-id="6538e-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6538e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6538e-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6538e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6538e-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6538e-162">INPUTS</span></span>

### <span data-ttu-id="6538e-163">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6538e-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6538e-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6538e-164">OUTPUTS</span></span>

### <span data-ttu-id="6538e-165">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6538e-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6538e-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6538e-166">NOTES</span></span>

## <span data-ttu-id="6538e-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6538e-167">RELATED LINKS</span></span>

[<span data-ttu-id="6538e-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6538e-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6538e-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6538e-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
