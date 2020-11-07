---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930586"
---
# <span data-ttu-id="780fc-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="780fc-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="780fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="780fc-102">SYNOPSIS</span></span>
<span data-ttu-id="780fc-103">Hämtar hemligheterna i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="780fc-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="780fc-104">SYNTAX</span></span>

### <span data-ttu-id="780fc-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="780fc-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="780fc-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="780fc-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="780fc-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="780fc-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="780fc-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="780fc-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="780fc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="780fc-109">DESCRIPTION</span></span>
<span data-ttu-id="780fc-110">Cmdleten **Get-AzureKeyVaultSecret** får hemligheter i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="780fc-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="780fc-111">Denna cmdlet tar emot specifik hemlighet eller alla hemligheter i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="780fc-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="780fc-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="780fc-112">EXAMPLES</span></span>

### <span data-ttu-id="780fc-113">Exempel 1: Hämta alla aktuella versioner av alla hemligheter i ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="780fc-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="780fc-114">Det här kommandot får de aktuella versionerna av alla hemligheter i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="780fc-115">Exempel 2: skaffa alla versioner av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="780fc-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="780fc-116">Det här kommandot får alla versioner av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="780fc-117">Exempel 3: Skaffa den senaste versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="780fc-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="780fc-118">Det här kommandot får den aktuella versionen av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="780fc-119">Exempel 4: skaffa en specifik version av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="780fc-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="780fc-120">Det här kommandot får en specifik version av hemligheten som heter ITSecret i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="780fc-121">Exempel 5: Hämta värdet oformaterad text för den aktuella versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="780fc-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="780fc-122">Dessa kommandon får den aktuella versionen av en hemlighet som heter ITSecret och visar sedan det oformaterade textvärdet för den hemligheten.</span><span class="sxs-lookup"><span data-stu-id="780fc-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="780fc-123">Exempel 6: Hämta alla hemligheter som tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="780fc-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="780fc-124">Det här kommandot får alla hemligheter som tagits bort tidigare, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="780fc-125">Exempel 7: hämtar den hemliga ITSecret som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="780fc-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="780fc-126">Det här kommandot får den hemliga ITSecret som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="780fc-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="780fc-127">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för den här borttagna hemligheten.</span><span class="sxs-lookup"><span data-stu-id="780fc-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="780fc-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="780fc-128">PARAMETERS</span></span>

### <span data-ttu-id="780fc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780fc-129">-DefaultProfile</span></span>
<span data-ttu-id="780fc-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="780fc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="780fc-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="780fc-131">-IncludeVersions</span></span>
<span data-ttu-id="780fc-132">Visar att denna cmdlet får alla versioner av en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="780fc-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="780fc-133">Den aktuella versionen av en hemlighet är den första i listan.</span><span class="sxs-lookup"><span data-stu-id="780fc-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="780fc-134">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="780fc-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="780fc-135">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av hemligheten med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="780fc-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fc-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="780fc-136">-InRemovedState</span></span>
<span data-ttu-id="780fc-137">Anger om tidigare borttagna hemligheter ska visas i utdata</span><span class="sxs-lookup"><span data-stu-id="780fc-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fc-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="780fc-138">-Name</span></span>
<span data-ttu-id="780fc-139">Anger namnet på den hemlighet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="780fc-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780fc-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="780fc-140">-VaultName</span></span>
<span data-ttu-id="780fc-141">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="780fc-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="780fc-142">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="780fc-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="780fc-143">-Version</span><span class="sxs-lookup"><span data-stu-id="780fc-143">-Version</span></span>
<span data-ttu-id="780fc-144">Anger den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="780fc-144">Specifies the secret version.</span></span>
<span data-ttu-id="780fc-145">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="780fc-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780fc-146">CommonParameters</span></span>
<span data-ttu-id="780fc-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780fc-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780fc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780fc-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="780fc-149">INPUTS</span></span>

### <span data-ttu-id="780fc-150">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="780fc-150">String</span></span>

## <span data-ttu-id="780fc-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="780fc-151">OUTPUTS</span></span>

### <span data-ttu-id="780fc-152">List<Microsoft. Azure. commands. nyckel valv. Models. SecretIdentityItem>, Microsoft. Azure. kommandon. nyckel valv. Models. Secret, list<Microsoft. Azure. commands.. Models. DeletedSecretIdentityItem>, Microsoft. Azure. kommandon. nyckel valv. Models.</span><span class="sxs-lookup"><span data-stu-id="780fc-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="780fc-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="780fc-153">NOTES</span></span>

## <span data-ttu-id="780fc-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="780fc-154">RELATED LINKS</span></span>

[<span data-ttu-id="780fc-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="780fc-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="780fc-156">Ångra-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="780fc-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="780fc-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="780fc-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

