---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 56a3fb2d31e4f80b15c027945437ffdc78aa131a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924422"
---
# <span data-ttu-id="12c3c-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12c3c-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="12c3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="12c3c-103">Skapar eller uppdaterar en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="12c3c-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="12c3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12c3c-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="12c3c-106">Cmdleten **set-AzKeyVaultSecret** skapar eller uppdaterar en hemlighet i ett nyckel valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="12c3c-106">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="12c3c-107">Om det inte finns någon hemlighet skapar den här cmdleten den.</span><span class="sxs-lookup"><span data-stu-id="12c3c-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="12c3c-108">Om det redan finns en hemlighet skapar den här cmdleten en ny version av den hemligheten.</span><span class="sxs-lookup"><span data-stu-id="12c3c-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="12c3c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12c3c-109">EXAMPLES</span></span>

### <span data-ttu-id="12c3c-110">Exempel 1: ändra värdet för en hemlighet som använder standardattribut</span><span class="sxs-lookup"><span data-stu-id="12c3c-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="12c3c-111">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Secret variabel.</span><span class="sxs-lookup"><span data-stu-id="12c3c-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="12c3c-112">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="12c3c-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="12c3c-113">Det andra kommandot ändrar värdet för hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="12c3c-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="12c3c-114">Det hemliga värdet blir det värde som lagras i $Secret.</span><span class="sxs-lookup"><span data-stu-id="12c3c-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="12c3c-115">Exempel 2: ändra värdet för en hemlighet med anpassade attribut</span><span class="sxs-lookup"><span data-stu-id="12c3c-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="12c3c-116">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Secret variabel.</span><span class="sxs-lookup"><span data-stu-id="12c3c-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="12c3c-117">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="12c3c-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="12c3c-118">Nästa kommando definierar anpassade attribut för utgångs datum, taggar och kontext typ och lagrar attribut i variabler.</span><span class="sxs-lookup"><span data-stu-id="12c3c-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="12c3c-119">Det slutliga kommandot ändrar värdena för hemligheten som heter ITSecret i nyckel valvet contoso med de värden som anges tidigare som variabler.</span><span class="sxs-lookup"><span data-stu-id="12c3c-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="12c3c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12c3c-120">PARAMETERS</span></span>

### <span data-ttu-id="12c3c-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="12c3c-121">-ContentType</span></span>
<span data-ttu-id="12c3c-122">Anger innehålls typen för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="12c3c-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="12c3c-123">Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="12c3c-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="12c3c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c3c-124">-DefaultProfile</span></span>
<span data-ttu-id="12c3c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12c3c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12c3c-126">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="12c3c-126">-Disable</span></span>
<span data-ttu-id="12c3c-127">Anger att denna cmdlet inaktiverar en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="12c3c-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="12c3c-128">-Upphör</span><span class="sxs-lookup"><span data-stu-id="12c3c-128">-Expires</span></span>
<span data-ttu-id="12c3c-129">Anger förfallo tid, som ett **datetime** -objekt, för den hemlighet som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="12c3c-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="12c3c-130">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="12c3c-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="12c3c-131">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="12c3c-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="12c3c-132">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="12c3c-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="12c3c-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="12c3c-133">-Name</span></span>
<span data-ttu-id="12c3c-134">Anger namnet på en hemlighet som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="12c3c-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="12c3c-135">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="12c3c-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="12c3c-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="12c3c-136">-NotBefore</span></span>
<span data-ttu-id="12c3c-137">Anger tiden, som ett **datetime** -objekt, innan hemligheten inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="12c3c-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="12c3c-138">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="12c3c-138">This parameter uses UTC.</span></span> <span data-ttu-id="12c3c-139">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="12c3c-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="12c3c-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="12c3c-140">-SecretValue</span></span>
<span data-ttu-id="12c3c-141">Anger värdet för hemligheten som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="12c3c-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="12c3c-142">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="12c3c-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="12c3c-143">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="12c3c-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c3c-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="12c3c-144">-Tag</span></span>
<span data-ttu-id="12c3c-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="12c3c-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12c3c-146">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="12c3c-146">For example:</span></span>

<span data-ttu-id="12c3c-147">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="12c3c-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="12c3c-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="12c3c-148">-VaultName</span></span>
<span data-ttu-id="12c3c-149">Anger namnet på det nyckel valv som den här hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="12c3c-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="12c3c-150">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="12c3c-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="12c3c-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12c3c-151">-Confirm</span></span>
<span data-ttu-id="12c3c-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12c3c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c3c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c3c-153">-WhatIf</span></span>
<span data-ttu-id="12c3c-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12c3c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c3c-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12c3c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c3c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c3c-156">CommonParameters</span></span>
<span data-ttu-id="12c3c-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c3c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c3c-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c3c-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c3c-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12c3c-159">INPUTS</span></span>

### <span data-ttu-id="12c3c-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="12c3c-160">None</span></span>
<span data-ttu-id="12c3c-161">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="12c3c-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12c3c-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12c3c-162">OUTPUTS</span></span>

### <span data-ttu-id="12c3c-163">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="12c3c-163">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="12c3c-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12c3c-164">NOTES</span></span>

## <span data-ttu-id="12c3c-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12c3c-165">RELATED LINKS</span></span>

[<span data-ttu-id="12c3c-166">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12c3c-166">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="12c3c-167">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12c3c-167">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
