---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574658"
---
# <span data-ttu-id="7bd35-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7bd35-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="7bd35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bd35-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd35-103">Hämtar nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="7bd35-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bd35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bd35-104">SYNTAX</span></span>

### <span data-ttu-id="7bd35-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="7bd35-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd35-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="7bd35-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd35-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="7bd35-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd35-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="7bd35-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd35-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bd35-109">DESCRIPTION</span></span>
<span data-ttu-id="7bd35-110">Cmdleten **Get-AzureKeyVaultKey** hämtar nyckel valv för Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd35-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="7bd35-111">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. Key valv. Key Vault.-paket** eller en lista över alla **paket** -objekt i ett nyckelord eller efter version.</span><span class="sxs-lookup"><span data-stu-id="7bd35-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="7bd35-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bd35-112">EXAMPLES</span></span>

### <span data-ttu-id="7bd35-113">Exempel 1: Hämta alla nycklar i ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="7bd35-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="7bd35-114">Det här kommandot får alla nycklar i nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="7bd35-115">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="7bd35-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="7bd35-116">Med det här kommandot får du den aktuella versionen av den Key som heter ITPfx i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="7bd35-117">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="7bd35-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="7bd35-118">Det här kommandot får alla versioner som heter ITPfx i vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="7bd35-119">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="7bd35-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="7bd35-120">Det här kommandot får en specifik version av den Key som heter ITPfx i nyckelordet contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="7bd35-121">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="7bd35-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="7bd35-122">Exempel 5: Hämta alla de nycklar som har tagits bort men inte rensats för detta nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="7bd35-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="7bd35-123">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i nyckel valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7bd35-124">Exempel 6: hämtar det ITPfx som har tagits bort men inte rensats för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="7bd35-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="7bd35-125">Det här kommandot får den ITPfx som du har tagit bort tidigare, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="7bd35-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7bd35-126">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="7bd35-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="7bd35-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bd35-127">PARAMETERS</span></span>

### <span data-ttu-id="7bd35-128">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7bd35-128">-IncludeVersions</span></span>
<span data-ttu-id="7bd35-129">Anger att denna cmdlet får alla versioner av en viktig.</span><span class="sxs-lookup"><span data-stu-id="7bd35-129">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="7bd35-130">Den aktuella versionen av en Key är den första som visas i listan.</span><span class="sxs-lookup"><span data-stu-id="7bd35-130">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="7bd35-131">Om du anger den här parametern måste du också ange parametrarna *namn* och *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="7bd35-131">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="7bd35-132">Om du inte anger parametern *IncludeVersions* får denna cmdlet den aktuella versionen av nycklarna med det angivna *namnet*.</span><span class="sxs-lookup"><span data-stu-id="7bd35-132">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd35-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7bd35-133">-InRemovedState</span></span>
<span data-ttu-id="7bd35-134">Anger om tidigare borttagna nycklar ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="7bd35-134">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd35-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bd35-135">-Name</span></span>
<span data-ttu-id="7bd35-136">Anger namnet på det Key-paket som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7bd35-136">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd35-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7bd35-137">-VaultName</span></span>
<span data-ttu-id="7bd35-138">Anger namnet på det nyckel valv från vilket denna cmdlet hämtar nycklar.</span><span class="sxs-lookup"><span data-stu-id="7bd35-138">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="7bd35-139">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.</span><span class="sxs-lookup"><span data-stu-id="7bd35-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd35-140">-Version</span><span class="sxs-lookup"><span data-stu-id="7bd35-140">-Version</span></span>
<span data-ttu-id="7bd35-141">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="7bd35-141">Specifies the key version.</span></span>
<span data-ttu-id="7bd35-142">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="7bd35-142">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd35-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd35-143">-DefaultProfile</span></span>
<span data-ttu-id="7bd35-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd35-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bd35-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd35-145">CommonParameters</span></span>
<span data-ttu-id="7bd35-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd35-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd35-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd35-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd35-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bd35-148">INPUTS</span></span>

### <span data-ttu-id="7bd35-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="7bd35-149">String</span></span>

## <span data-ttu-id="7bd35-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bd35-150">OUTPUTS</span></span>

### <span data-ttu-id="7bd35-151">List<Microsoft. Azure. kommandon. DeletedKeyIdentityItem. Models. KeyIdentityItem>, Microsoft. Azure. kommandon.-paket, list<Microsoft. Azure. commands.. Models.>, Microsoft. Azure. commands. Vault. Models.</span><span class="sxs-lookup"><span data-stu-id="7bd35-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="7bd35-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bd35-152">NOTES</span></span>

## <span data-ttu-id="7bd35-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bd35-153">RELATED LINKS</span></span>

[<span data-ttu-id="7bd35-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7bd35-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="7bd35-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7bd35-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="7bd35-156">Ångra-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7bd35-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="7bd35-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="7bd35-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

