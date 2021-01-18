---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: fa53affab7fe530defcf23f169458ee6813722a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525976"
---
# <span data-ttu-id="0099f-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0099f-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="0099f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0099f-102">SYNOPSIS</span></span>
<span data-ttu-id="0099f-103">Hämtar nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="0099f-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="0099f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0099f-104">SYNTAX</span></span>

### <span data-ttu-id="0099f-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="0099f-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="0099f-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0099f-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0099f-123">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0099f-123">DESCRIPTION</span></span>
<span data-ttu-id="0099f-124">Cmdleten **Get-AzKeyVaultKey** hämtar nyckel valv för Azure.</span><span class="sxs-lookup"><span data-stu-id="0099f-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="0099f-125">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.</span><span class="sxs-lookup"><span data-stu-id="0099f-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="0099f-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0099f-126">EXAMPLES</span></span>

### <span data-ttu-id="0099f-127">Exempel 1: Hämta alla nycklar i ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="0099f-127">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0099f-128">Det här kommandot får alla nycklar i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="0099f-129">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="0099f-129">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0099f-130">Med det här kommandot får du den aktuella versionen av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0099f-131">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="0099f-131">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0099f-132">Det här kommandot får alla versioner som heter ITPfx i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="0099f-133">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="0099f-133">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0099f-134">Det här kommandot får en specifik version av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="0099f-135">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="0099f-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="0099f-136">Exempel 5: Hämta alla nycklar som har tagits bort men inte rensats för detta nyckel valv</span><span class="sxs-lookup"><span data-stu-id="0099f-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="0099f-137">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0099f-138">Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="0099f-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="0099f-139">Det här kommandot får den test3 som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="0099f-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0099f-140">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="0099f-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="0099f-141">Exempel 7: Hämta alla nycklar i ett nyckel valv med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="0099f-141">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0099f-142">Det här kommandot får alla nycklar i nyckel valvet contoso som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="0099f-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="0099f-143">Exempel 8: Ladda ned en offentlig fil som en. PEM-fil</span><span class="sxs-lookup"><span data-stu-id="0099f-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="0099f-144">Du kan ladda ned den offentliga knappen för en RSA-fil genom att ange `-OutFile` parametern.</span><span class="sxs-lookup"><span data-stu-id="0099f-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="0099f-145">Det här är ett steg i Importera HSM-skyddade nycklar till Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0099f-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="0099f-146">Se https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="0099f-146">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="0099f-147">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0099f-147">PARAMETERS</span></span>

### <span data-ttu-id="0099f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0099f-148">-DefaultProfile</span></span>
<span data-ttu-id="0099f-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0099f-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0099f-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0099f-150">-HsmName</span></span>
<span data-ttu-id="0099f-151">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="0099f-151">HSM name.</span></span> <span data-ttu-id="0099f-152">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="0099f-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="0099f-153">-HsmObject</span></span>
<span data-ttu-id="0099f-154">HSM-objekt.</span><span class="sxs-lookup"><span data-stu-id="0099f-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="0099f-155">-HsmResourceId</span></span>
<span data-ttu-id="0099f-156">HSM-resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0099f-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0099f-157">-IncludeVersions</span></span>
<span data-ttu-id="0099f-158">Anger att denna cmdlet får alla versioner av en viktig.</span><span class="sxs-lookup"><span data-stu-id="0099f-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="0099f-159">Den aktuella versionen av en Key är den första som visas i listan.</span><span class="sxs-lookup"><span data-stu-id="0099f-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="0099f-160">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="0099f-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="0099f-161">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="0099f-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0099f-162">-InputObject</span></span>
<span data-ttu-id="0099f-163">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="0099f-163">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0099f-164">-InRemovedState</span></span>
<span data-ttu-id="0099f-165">Anger om tidigare borttagna nycklar ska visas i resultatet</span><span class="sxs-lookup"><span data-stu-id="0099f-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-166">-Namn</span><span class="sxs-lookup"><span data-stu-id="0099f-166">-Name</span></span>
<span data-ttu-id="0099f-167">Anger namnet på det Key-paket som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0099f-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0099f-168">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="0099f-168">-OutFile</span></span>
<span data-ttu-id="0099f-169">Anger den utdatafil som den här cmdleten sparar för.</span><span class="sxs-lookup"><span data-stu-id="0099f-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="0099f-170">Den offentliga knappen sparas som standard i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="0099f-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="0099f-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0099f-171">-ResourceId</span></span>
<span data-ttu-id="0099f-172">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="0099f-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0099f-173">-VaultName</span></span>
<span data-ttu-id="0099f-174">Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.</span><span class="sxs-lookup"><span data-stu-id="0099f-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="0099f-175">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="0099f-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-176">-Version</span><span class="sxs-lookup"><span data-stu-id="0099f-176">-Version</span></span>
<span data-ttu-id="0099f-177">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="0099f-177">Specifies the key version.</span></span>
<span data-ttu-id="0099f-178">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="0099f-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0099f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0099f-179">CommonParameters</span></span>
<span data-ttu-id="0099f-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0099f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0099f-181">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0099f-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0099f-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0099f-182">INPUTS</span></span>

### <span data-ttu-id="0099f-183">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0099f-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0099f-184">System. String</span><span class="sxs-lookup"><span data-stu-id="0099f-184">System.String</span></span>

## <span data-ttu-id="0099f-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0099f-185">OUTPUTS</span></span>

### <span data-ttu-id="0099f-186">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0099f-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0099f-187">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0099f-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="0099f-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0099f-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0099f-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0099f-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="0099f-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0099f-190">NOTES</span></span>

## <span data-ttu-id="0099f-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0099f-191">RELATED LINKS</span></span>

[<span data-ttu-id="0099f-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0099f-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0099f-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0099f-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0099f-194">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0099f-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="0099f-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="0099f-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

