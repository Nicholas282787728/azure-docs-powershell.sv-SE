---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: e37236e4e5fbced90a6dbd5f33d22d02947b20d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757075"
---
# <span data-ttu-id="f2ac9-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f2ac9-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f2ac9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ac9-103">Hämtar SAS-definitioner för hanterade nycklar för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ac9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2ac9-104">SYNTAX</span></span>

### <span data-ttu-id="f2ac9-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="f2ac9-105">ByDefinitionName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ac9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2ac9-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ac9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2ac9-107">DESCRIPTION</span></span>
<span data-ttu-id="f2ac9-108">Hämtar en säkerhets beskrivning för Managed Storage för viktiga nycklar om namnet på definitionen anges.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="f2ac9-109">Om du inte anger något definitions namn visas alla SAS-definitioner som är kopplade till det angivna lagrings kontot för Key valv som hanteras i valvet.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="f2ac9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2ac9-110">EXAMPLES</span></span>

### <span data-ttu-id="f2ac9-111">Exempel 1: lista alla sa-definitioner för hanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="f2ac9-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="f2ac9-112">Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' online Vault '</span><span class="sxs-lookup"><span data-stu-id="f2ac9-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="f2ac9-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="f2ac9-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="f2ac9-114">Hämtar information om SAS-definitionen, "konton", som är associerad med Key valv Managed Storage-konto ' mystorageaccount ' som hanteras av valvet.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="f2ac9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2ac9-115">PARAMETERS</span></span>

### <span data-ttu-id="f2ac9-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2ac9-116">-AccountName</span></span>
<span data-ttu-id="f2ac9-117">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-117">Vault name.</span></span>
<span data-ttu-id="f2ac9-118">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ac9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ac9-119">-DefaultProfile</span></span>
<span data-ttu-id="f2ac9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f2ac9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2ac9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2ac9-121">-InputObject</span></span>
<span data-ttu-id="f2ac9-122">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-122">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ac9-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f2ac9-123">-InRemovedState</span></span>
<span data-ttu-id="f2ac9-124">Anger om de tidigare borttagna säkerhets associationerna för lagring ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-124">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="f2ac9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2ac9-125">-Name</span></span>
<span data-ttu-id="f2ac9-126">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-126">Storage sas definition name.</span></span>
<span data-ttu-id="f2ac9-127">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ac9-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f2ac9-128">-VaultName</span></span>
<span data-ttu-id="f2ac9-129">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-129">Vault name.</span></span>
<span data-ttu-id="f2ac9-130">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ac9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ac9-131">CommonParameters</span></span>
<span data-ttu-id="f2ac9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ac9-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ac9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ac9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2ac9-134">INPUTS</span></span>

### <span data-ttu-id="f2ac9-135">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2ac9-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="f2ac9-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2ac9-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f2ac9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2ac9-137">OUTPUTS</span></span>

### <span data-ttu-id="f2ac9-138">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2ac9-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="f2ac9-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f2ac9-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="f2ac9-140">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f2ac9-140">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="f2ac9-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2ac9-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="f2ac9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2ac9-142">NOTES</span></span>

## <span data-ttu-id="f2ac9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2ac9-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

