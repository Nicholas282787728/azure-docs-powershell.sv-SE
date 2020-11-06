---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f2507d441dc04fd01217dde685deb667211f4034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586088"
---
# <span data-ttu-id="cd28c-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd28c-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="cd28c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd28c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd28c-103">Hämtar hemligheterna i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="cd28c-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd28c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd28c-104">SYNTAX</span></span>

### <span data-ttu-id="cd28c-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="cd28c-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd28c-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="cd28c-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd28c-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="cd28c-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd28c-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="cd28c-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd28c-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="cd28c-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd28c-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="cd28c-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd28c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd28c-111">DESCRIPTION</span></span>
<span data-ttu-id="cd28c-112">Cmdleten **Get-AzureKeyVaultSecret** får hemligheter i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="cd28c-112">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="cd28c-113">Denna cmdlet tar emot specifik hemlighet eller alla hemligheter i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="cd28c-113">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="cd28c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd28c-114">EXAMPLES</span></span>

### <span data-ttu-id="cd28c-115">Exempel 1: Hämta alla aktuella versioner av alla hemligheter i ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="cd28c-115">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="cd28c-116">Det här kommandot får de aktuella versionerna av alla hemligheter i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-116">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd28c-117">Exempel 2: skaffa alla versioner av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="cd28c-117">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="cd28c-118">Det här kommandot får alla versioner av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-118">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd28c-119">Exempel 3: Skaffa den senaste versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="cd28c-119">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="cd28c-120">Det här kommandot får den aktuella versionen av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-120">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd28c-121">Exempel 4: skaffa en specifik version av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="cd28c-121">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="cd28c-122">Det här kommandot får en specifik version av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-122">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd28c-123">Exempel 5: Hämta värdet oformaterad text för den aktuella versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="cd28c-123">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="cd28c-124">Dessa kommandon får den aktuella versionen av en hemlighet som heter ITSecret och visar sedan det oformaterade textvärdet för den hemligheten.</span><span class="sxs-lookup"><span data-stu-id="cd28c-124">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="cd28c-125">Exempel 6: Hämta alla hemligheter som tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="cd28c-125">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="cd28c-126">Det här kommandot får alla hemligheter som tagits bort tidigare, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-126">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd28c-127">Exempel 7: hämtar den hemliga ITSecret som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="cd28c-127">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="cd28c-128">Det här kommandot får den hemliga ITSecret som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="cd28c-128">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="cd28c-129">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för den här borttagna hemligheten.</span><span class="sxs-lookup"><span data-stu-id="cd28c-129">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="cd28c-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd28c-130">PARAMETERS</span></span>

### <span data-ttu-id="cd28c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd28c-131">-DefaultProfile</span></span>
<span data-ttu-id="cd28c-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cd28c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd28c-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="cd28c-133">-IncludeVersions</span></span>
<span data-ttu-id="cd28c-134">Visar att denna cmdlet får alla versioner av en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="cd28c-134">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="cd28c-135">Den aktuella versionen av en hemlighet är den första i listan.</span><span class="sxs-lookup"><span data-stu-id="cd28c-135">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="cd28c-136">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="cd28c-136">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="cd28c-137">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av hemligheten med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="cd28c-137">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd28c-138">-InputObject</span></span>
<span data-ttu-id="cd28c-139">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="cd28c-139">KeyVault Object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-140">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="cd28c-140">-InRemovedState</span></span>
<span data-ttu-id="cd28c-141">Anger om tidigare borttagna hemligheter ska visas i utdata</span><span class="sxs-lookup"><span data-stu-id="cd28c-141">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd28c-142">-Name</span></span>
<span data-ttu-id="cd28c-143">Anger namnet på den hemlighet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="cd28c-143">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cd28c-144">-VaultName</span></span>
<span data-ttu-id="cd28c-145">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="cd28c-145">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="cd28c-146">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="cd28c-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-147">-Version</span><span class="sxs-lookup"><span data-stu-id="cd28c-147">-Version</span></span>
<span data-ttu-id="cd28c-148">Anger den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="cd28c-148">Specifies the secret version.</span></span>
<span data-ttu-id="cd28c-149">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="cd28c-149">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, ByInputObjectSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd28c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd28c-150">CommonParameters</span></span>
<span data-ttu-id="cd28c-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd28c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd28c-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd28c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd28c-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd28c-153">INPUTS</span></span>

### <span data-ttu-id="cd28c-154">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="cd28c-154">String</span></span>

## <span data-ttu-id="cd28c-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd28c-155">OUTPUTS</span></span>

### <span data-ttu-id="cd28c-156">List<Microsoft. Azure. kommandon. PSKeyVaultSecret. Models. PSKeyVaultSecretIdentityItem>, Microsoft. Azure. kommandon., list<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd28c-156">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="cd28c-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd28c-157">NOTES</span></span>

## <span data-ttu-id="cd28c-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd28c-158">RELATED LINKS</span></span>

[<span data-ttu-id="cd28c-159">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd28c-159">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="cd28c-160">Ångra-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="cd28c-160">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="cd28c-161">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd28c-161">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

