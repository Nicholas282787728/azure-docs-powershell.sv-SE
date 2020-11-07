---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: e8763fcb74c3177e91992996f00c670b32ffbbb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757079"
---
# <span data-ttu-id="bd824-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bd824-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="bd824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd824-102">SYNOPSIS</span></span>
<span data-ttu-id="bd824-103">Hämtar nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="bd824-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd824-104">SYNTAX</span></span>

### <span data-ttu-id="bd824-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="bd824-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="bd824-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bd824-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="bd824-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="bd824-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bd824-110">ByInputObjectKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="bd824-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="bd824-112">ByResourceIdKeyName</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd824-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bd824-113">ByResourceIdKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd824-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd824-114">DESCRIPTION</span></span>
<span data-ttu-id="bd824-115">Cmdleten **Get-AzureKeyVaultKey** hämtar nyckel valv för Azure.</span><span class="sxs-lookup"><span data-stu-id="bd824-115">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="bd824-116">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.</span><span class="sxs-lookup"><span data-stu-id="bd824-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="bd824-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd824-117">EXAMPLES</span></span>

### <span data-ttu-id="bd824-118">Exempel 1: Hämta alla nycklar i ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="bd824-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso'

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

<span data-ttu-id="bd824-119">Det här kommandot får alla nycklar i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="bd824-120">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="bd824-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

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

<span data-ttu-id="bd824-121">Med det här kommandot får du den aktuella versionen av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="bd824-122">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="bd824-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

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

<span data-ttu-id="bd824-123">Det här kommandot får alla versioner som heter ITPfx i vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="bd824-124">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="bd824-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

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

<span data-ttu-id="bd824-125">Det här kommandot får en specifik version av den Key som heter TEST1 i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="bd824-126">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="bd824-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="bd824-127">Exempel 5: Hämta alla de nycklar som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="bd824-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -InRemovedState

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

<span data-ttu-id="bd824-128">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="bd824-129">Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="bd824-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

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

<span data-ttu-id="bd824-130">Det här kommandot får den test3 som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="bd824-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="bd824-131">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="bd824-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="bd824-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd824-132">PARAMETERS</span></span>

### <span data-ttu-id="bd824-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd824-133">-DefaultProfile</span></span>
<span data-ttu-id="bd824-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bd824-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd824-135">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="bd824-135">-IncludeVersions</span></span>
<span data-ttu-id="bd824-136">Anger att denna cmdlet får alla versioner av en viktig.</span><span class="sxs-lookup"><span data-stu-id="bd824-136">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="bd824-137">Den aktuella versionen av en Key är den första som visas i listan.</span><span class="sxs-lookup"><span data-stu-id="bd824-137">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="bd824-138">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="bd824-138">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="bd824-139">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="bd824-139">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="bd824-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd824-140">-InputObject</span></span>
<span data-ttu-id="bd824-141">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="bd824-141">KeyVault object.</span></span>

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

### <span data-ttu-id="bd824-142">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bd824-142">-InRemovedState</span></span>
<span data-ttu-id="bd824-143">Anger om tidigare borttagna nycklar ska visas i resultatet</span><span class="sxs-lookup"><span data-stu-id="bd824-143">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="bd824-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd824-144">-Name</span></span>
<span data-ttu-id="bd824-145">Anger namnet på det Key-paket som ska visas.</span><span class="sxs-lookup"><span data-stu-id="bd824-145">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="bd824-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd824-146">-ResourceId</span></span>
<span data-ttu-id="bd824-147">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="bd824-147">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="bd824-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bd824-148">-VaultName</span></span>
<span data-ttu-id="bd824-149">Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.</span><span class="sxs-lookup"><span data-stu-id="bd824-149">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="bd824-150">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="bd824-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="bd824-151">-Version</span><span class="sxs-lookup"><span data-stu-id="bd824-151">-Version</span></span>
<span data-ttu-id="bd824-152">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="bd824-152">Specifies the key version.</span></span>
<span data-ttu-id="bd824-153">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="bd824-153">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="bd824-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd824-154">CommonParameters</span></span>
<span data-ttu-id="bd824-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd824-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd824-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd824-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd824-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd824-157">INPUTS</span></span>

### <span data-ttu-id="bd824-158">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bd824-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="bd824-159">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd824-159">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bd824-160">System. String</span><span class="sxs-lookup"><span data-stu-id="bd824-160">System.String</span></span>

## <span data-ttu-id="bd824-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd824-161">OUTPUTS</span></span>

### <span data-ttu-id="bd824-162">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bd824-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bd824-163">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bd824-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="bd824-164">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bd824-164">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bd824-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bd824-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="bd824-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd824-166">NOTES</span></span>

## <span data-ttu-id="bd824-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd824-167">RELATED LINKS</span></span>

[<span data-ttu-id="bd824-168">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bd824-168">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="bd824-169">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bd824-169">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="bd824-170">Ångra-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bd824-170">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="bd824-171">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="bd824-171">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

