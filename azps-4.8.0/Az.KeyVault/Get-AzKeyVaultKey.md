---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 0de3582d9a5cbdaba8555cf53bd9038d3eaf15b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259465"
---
# <span data-ttu-id="c341e-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c341e-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="c341e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c341e-102">SYNOPSIS</span></span>
<span data-ttu-id="c341e-103">Hämtar nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="c341e-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="c341e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c341e-104">SYNTAX</span></span>

### <span data-ttu-id="c341e-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="c341e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="c341e-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="c341e-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="c341e-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="c341e-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="c341e-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="c341e-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="c341e-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c341e-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="c341e-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c341e-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c341e-114">DESCRIPTION</span></span>
<span data-ttu-id="c341e-115">Cmdleten **Get-AzKeyVaultKey** hämtar nyckel valv för Azure.</span><span class="sxs-lookup"><span data-stu-id="c341e-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="c341e-116">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.</span><span class="sxs-lookup"><span data-stu-id="c341e-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="c341e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c341e-117">EXAMPLES</span></span>

### <span data-ttu-id="c341e-118">Exempel 1: Hämta alla nycklar i ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="c341e-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="c341e-119">Det här kommandot får alla nycklar i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="c341e-120">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="c341e-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="c341e-121">Med det här kommandot får du den aktuella versionen av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="c341e-122">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="c341e-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="c341e-123">Det här kommandot får alla versioner som heter ITPfx i vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="c341e-124">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="c341e-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="c341e-125">Det här kommandot får en specifik version av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="c341e-126">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="c341e-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="c341e-127">Exempel 5: Hämta alla de nycklar som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="c341e-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="c341e-128">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="c341e-129">Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="c341e-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="c341e-130">Det här kommandot får den test3 som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="c341e-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="c341e-131">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="c341e-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="c341e-132">Exempel 7: Hämta alla nycklar i ett nyckel valv med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="c341e-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="c341e-133">Det här kommandot får alla nycklar i nyckel valvet contoso som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="c341e-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="c341e-134">Exempel 8: Ladda ned en offentlig fil som en. PEM-fil</span><span class="sxs-lookup"><span data-stu-id="c341e-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="c341e-135">Du kan ladda ned den offentliga knappen för en RSA-fil genom att ange `-OutFile` parametern.</span><span class="sxs-lookup"><span data-stu-id="c341e-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="c341e-136">Det här är ett steg i Importera HSM-skyddade nycklar till Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c341e-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="c341e-137">Se https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="c341e-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="c341e-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c341e-138">PARAMETERS</span></span>

### <span data-ttu-id="c341e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c341e-139">-DefaultProfile</span></span>
<span data-ttu-id="c341e-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c341e-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c341e-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="c341e-141">-IncludeVersions</span></span>
<span data-ttu-id="c341e-142">Anger att denna cmdlet får alla versioner av en viktig.</span><span class="sxs-lookup"><span data-stu-id="c341e-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="c341e-143">Den aktuella versionen av en Key är den första som visas i listan.</span><span class="sxs-lookup"><span data-stu-id="c341e-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="c341e-144">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="c341e-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="c341e-145">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="c341e-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341e-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c341e-146">-InputObject</span></span>
<span data-ttu-id="c341e-147">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="c341e-147">KeyVault object.</span></span>

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

### <span data-ttu-id="c341e-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c341e-148">-InRemovedState</span></span>
<span data-ttu-id="c341e-149">Anger om tidigare borttagna nycklar ska visas i resultatet</span><span class="sxs-lookup"><span data-stu-id="c341e-149">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="c341e-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="c341e-150">-Name</span></span>
<span data-ttu-id="c341e-151">Anger namnet på det Key-paket som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c341e-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341e-152">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="c341e-152">-OutFile</span></span>
<span data-ttu-id="c341e-153">Anger den utdatafil som den här cmdleten sparar för.</span><span class="sxs-lookup"><span data-stu-id="c341e-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="c341e-154">Den offentliga knappen sparas som standard i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="c341e-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="c341e-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c341e-155">-ResourceId</span></span>
<span data-ttu-id="c341e-156">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="c341e-156">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="c341e-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c341e-157">-VaultName</span></span>
<span data-ttu-id="c341e-158">Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.</span><span class="sxs-lookup"><span data-stu-id="c341e-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="c341e-159">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="c341e-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="c341e-160">-Version</span><span class="sxs-lookup"><span data-stu-id="c341e-160">-Version</span></span>
<span data-ttu-id="c341e-161">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="c341e-161">Specifies the key version.</span></span>
<span data-ttu-id="c341e-162">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="c341e-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c341e-163">CommonParameters</span></span>
<span data-ttu-id="c341e-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c341e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c341e-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c341e-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c341e-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c341e-166">INPUTS</span></span>

### <span data-ttu-id="c341e-167">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c341e-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c341e-168">System. String</span><span class="sxs-lookup"><span data-stu-id="c341e-168">System.String</span></span>

## <span data-ttu-id="c341e-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c341e-169">OUTPUTS</span></span>

### <span data-ttu-id="c341e-170">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c341e-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="c341e-171">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c341e-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="c341e-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c341e-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="c341e-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c341e-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="c341e-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c341e-174">NOTES</span></span>

## <span data-ttu-id="c341e-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c341e-175">RELATED LINKS</span></span>

[<span data-ttu-id="c341e-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c341e-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="c341e-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c341e-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="c341e-178">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="c341e-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="c341e-179">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="c341e-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

