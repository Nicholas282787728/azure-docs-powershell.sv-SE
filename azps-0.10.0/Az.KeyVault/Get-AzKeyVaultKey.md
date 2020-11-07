---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922718"
---
# <span data-ttu-id="1c3ba-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1c3ba-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="1c3ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3ba-103">Hämtar nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="1c3ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c3ba-104">SYNTAX</span></span>

### <span data-ttu-id="1c3ba-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="1c3ba-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ba-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="1c3ba-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ba-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1c3ba-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ba-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="1c3ba-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c3ba-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c3ba-109">DESCRIPTION</span></span>
<span data-ttu-id="1c3ba-110">Cmdleten **Get-AzKeyVaultKey** hämtar nyckel valv för Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="1c3ba-111">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="1c3ba-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c3ba-112">EXAMPLES</span></span>

### <span data-ttu-id="1c3ba-113">Exempel 1: Hämta alla nycklar i ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="1c3ba-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="1c3ba-114">Det här kommandot får alla nycklar i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="1c3ba-115">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="1c3ba-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="1c3ba-116">Med det här kommandot får du den aktuella versionen av den Key som heter ITPfx i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="1c3ba-117">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="1c3ba-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="1c3ba-118">Det här kommandot får alla versioner som heter ITPfx i vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="1c3ba-119">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="1c3ba-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="1c3ba-120">Det här kommandot får en specifik version av den Key som heter ITPfx i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="1c3ba-121">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="1c3ba-122">Exempel 5: Hämta alla de nycklar som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="1c3ba-123">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1c3ba-124">Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="1c3ba-125">Det här kommandot får den ITPfx som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1c3ba-126">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="1c3ba-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c3ba-127">PARAMETERS</span></span>

### <span data-ttu-id="1c3ba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3ba-128">-DefaultProfile</span></span>
<span data-ttu-id="1c3ba-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c3ba-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c3ba-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1c3ba-130">-IncludeVersions</span></span>
<span data-ttu-id="1c3ba-131">Anger att denna cmdlet får alla versioner av en viktig.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="1c3ba-132">Den aktuella versionen av en Key är den första som visas i listan.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="1c3ba-133">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="1c3ba-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="1c3ba-134">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ba-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1c3ba-135">-InRemovedState</span></span>
<span data-ttu-id="1c3ba-136">Anger om tidigare borttagna nycklar ska visas i resultatet</span><span class="sxs-lookup"><span data-stu-id="1c3ba-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ba-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c3ba-137">-Name</span></span>
<span data-ttu-id="1c3ba-138">Anger namnet på det Key-paket som ska visas.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ba-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1c3ba-139">-VaultName</span></span>
<span data-ttu-id="1c3ba-140">Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="1c3ba-141">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="1c3ba-142">-Version</span><span class="sxs-lookup"><span data-stu-id="1c3ba-142">-Version</span></span>
<span data-ttu-id="1c3ba-143">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-143">Specifies the key version.</span></span>
<span data-ttu-id="1c3ba-144">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3ba-145">CommonParameters</span></span>
<span data-ttu-id="1c3ba-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3ba-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3ba-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3ba-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c3ba-148">INPUTS</span></span>

### <span data-ttu-id="1c3ba-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="1c3ba-149">String</span></span>

## <span data-ttu-id="1c3ba-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c3ba-150">OUTPUTS</span></span>

### <span data-ttu-id="1c3ba-151">List<Microsoft. Azure. kommandon. DeletedKeyIdentityItem. Models. KeyIdentityItem>, Microsoft. Azure. kommandon.-paket, list<Microsoft. Azure. commands.. Models.>, Microsoft. Azure. commands. Vault. Models.</span><span class="sxs-lookup"><span data-stu-id="1c3ba-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="1c3ba-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c3ba-152">NOTES</span></span>

## <span data-ttu-id="1c3ba-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c3ba-153">RELATED LINKS</span></span>

[<span data-ttu-id="1c3ba-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1c3ba-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1c3ba-155">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1c3ba-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1c3ba-156">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1c3ba-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="1c3ba-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1c3ba-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

