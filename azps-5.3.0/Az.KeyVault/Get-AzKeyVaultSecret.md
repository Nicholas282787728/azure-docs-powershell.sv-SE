---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523533"
---
# <span data-ttu-id="aae72-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aae72-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="aae72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aae72-102">SYNOPSIS</span></span>
<span data-ttu-id="aae72-103">Hämtar hemligheterna i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="aae72-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="aae72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aae72-104">SYNTAX</span></span>

### <span data-ttu-id="aae72-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="aae72-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="aae72-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="aae72-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="aae72-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="aae72-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="aae72-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="aae72-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="aae72-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae72-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="aae72-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae72-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aae72-114">DESCRIPTION</span></span>
<span data-ttu-id="aae72-115">Cmdleten **Get-AzKeyVaultSecret** får hemligheter i ett nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="aae72-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="aae72-116">Denna cmdlet tar emot specifik hemlighet eller alla hemligheter i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="aae72-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="aae72-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aae72-117">EXAMPLES</span></span>

### <span data-ttu-id="aae72-118">Exempel 1: Hämta alla aktuella versioner av alla hemligheter i ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="aae72-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="aae72-119">Det här kommandot får de aktuella versionerna av alla hemligheter i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="aae72-120">Exempel 2: skaffa alla versioner av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="aae72-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="aae72-121">Det här kommandot får alla versioner av hemligheten som heter secret1 i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="aae72-122">Exempel 3: Skaffa den senaste versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="aae72-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="aae72-123">Det här kommandot får den aktuella versionen av hemligheten som heter secret1 i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="aae72-124">Exempel 4: skaffa en specifik version av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="aae72-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="aae72-125">Det här kommandot får en specifik version av hemligheten som heter secret1 i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="aae72-126">Exempel 5: Hämta värdet oformaterad text för den aktuella versionen av en viss hemlighet</span><span class="sxs-lookup"><span data-stu-id="aae72-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="aae72-127">Cmdleten returnerar hemligheten som en sträng när `-AsPlainText` används.</span><span class="sxs-lookup"><span data-stu-id="aae72-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="aae72-128">Exempel 6: Hämta alla hemligheter som tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="aae72-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="aae72-129">Det här kommandot får alla hemligheter som tagits bort tidigare, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="aae72-130">Exempel 7: hämtar den hemliga ITSecret som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="aae72-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="aae72-131">Det här kommandot får det hemliga värdet ' secret1 ' som tidigare har tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="aae72-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="aae72-132">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för den här borttagna hemligheten.</span><span class="sxs-lookup"><span data-stu-id="aae72-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="aae72-133">Exempel 8: Hämta alla aktuella versioner av alla hemligheter i ett viktigt-valv med filter</span><span class="sxs-lookup"><span data-stu-id="aae72-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="aae72-134">Det här kommandot hämtar de aktuella versionerna av alla hemligheter i det nyckel valv som börjar med "hemligt".</span><span class="sxs-lookup"><span data-stu-id="aae72-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="aae72-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aae72-135">PARAMETERS</span></span>

### <span data-ttu-id="aae72-136">-Klar text</span><span class="sxs-lookup"><span data-stu-id="aae72-136">-AsPlainText</span></span>
<span data-ttu-id="aae72-137">När den är aktive rad konverteras hemligheten i en säker sträng till den dekrypterade oformaterade text strängen som utdata.</span><span class="sxs-lookup"><span data-stu-id="aae72-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae72-138">-DefaultProfile</span></span>
<span data-ttu-id="aae72-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aae72-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aae72-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="aae72-140">-IncludeVersions</span></span>
<span data-ttu-id="aae72-141">Visar att denna cmdlet får alla versioner av en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="aae72-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="aae72-142">Den aktuella versionen av en hemlighet är den första i listan.</span><span class="sxs-lookup"><span data-stu-id="aae72-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="aae72-143">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="aae72-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="aae72-144">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av hemligheten med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="aae72-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aae72-145">-InputObject</span></span>
<span data-ttu-id="aae72-146">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="aae72-146">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="aae72-147">-InRemovedState</span></span>
<span data-ttu-id="aae72-148">Anger om tidigare borttagna hemligheter ska visas i utdata</span><span class="sxs-lookup"><span data-stu-id="aae72-148">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="aae72-149">-Name</span></span>
<span data-ttu-id="aae72-150">Anger namnet på den hemlighet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="aae72-150">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="aae72-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aae72-151">-ResourceId</span></span>
<span data-ttu-id="aae72-152">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="aae72-152">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aae72-153">-VaultName</span></span>
<span data-ttu-id="aae72-154">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="aae72-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="aae72-155">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="aae72-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-156">-Version</span><span class="sxs-lookup"><span data-stu-id="aae72-156">-Version</span></span>
<span data-ttu-id="aae72-157">Anger den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="aae72-157">Specifies the secret version.</span></span>
<span data-ttu-id="aae72-158">Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.</span><span class="sxs-lookup"><span data-stu-id="aae72-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae72-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae72-159">CommonParameters</span></span>
<span data-ttu-id="aae72-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae72-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae72-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aae72-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae72-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aae72-162">INPUTS</span></span>

### <span data-ttu-id="aae72-163">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="aae72-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="aae72-164">System. String</span><span class="sxs-lookup"><span data-stu-id="aae72-164">System.String</span></span>

## <span data-ttu-id="aae72-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aae72-165">OUTPUTS</span></span>

### <span data-ttu-id="aae72-166">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aae72-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="aae72-167">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aae72-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="aae72-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aae72-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="aae72-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aae72-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="aae72-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aae72-170">NOTES</span></span>

## <span data-ttu-id="aae72-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aae72-171">RELATED LINKS</span></span>

[<span data-ttu-id="aae72-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aae72-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="aae72-173">Ångra-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="aae72-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="aae72-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aae72-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

