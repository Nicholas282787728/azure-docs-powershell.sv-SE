---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319912"
---
# <span data-ttu-id="60b71-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="60b71-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="60b71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60b71-102">SYNOPSIS</span></span>
<span data-ttu-id="60b71-103">Hämtar SAS-definitioner för hanterade nycklar för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="60b71-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="60b71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60b71-104">SYNTAX</span></span>

### <span data-ttu-id="60b71-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="60b71-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60b71-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60b71-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b71-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60b71-107">DESCRIPTION</span></span>
<span data-ttu-id="60b71-108">Hämtar en säkerhets beskrivning för Managed Storage för viktiga nycklar om namnet på definitionen anges.</span><span class="sxs-lookup"><span data-stu-id="60b71-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="60b71-109">Om du inte anger något definitions namn visas alla SAS-definitioner som är kopplade till det angivna lagrings kontot för Key valv som hanteras i valvet.</span><span class="sxs-lookup"><span data-stu-id="60b71-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="60b71-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60b71-110">EXAMPLES</span></span>

### <span data-ttu-id="60b71-111">Exempel 1: lista alla sa-definitioner för hanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="60b71-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="60b71-112">Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' online Vault '</span><span class="sxs-lookup"><span data-stu-id="60b71-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="60b71-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="60b71-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

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

<span data-ttu-id="60b71-114">Hämtar information om SAS-definitionen, "konton", som är associerad med Key valv Managed Storage-konto ' mystorageaccount ' som hanteras av valvet.</span><span class="sxs-lookup"><span data-stu-id="60b71-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="60b71-115">Exempel 3: lista alla associationer för hanterade säkerhets nycklar för viktiga valv med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="60b71-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="60b71-116">Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' prevalv ' som börjar med "Account".</span><span class="sxs-lookup"><span data-stu-id="60b71-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="60b71-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60b71-117">PARAMETERS</span></span>

### <span data-ttu-id="60b71-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60b71-118">-AccountName</span></span>
<span data-ttu-id="60b71-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="60b71-119">Vault name.</span></span>
<span data-ttu-id="60b71-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="60b71-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="60b71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b71-121">-DefaultProfile</span></span>
<span data-ttu-id="60b71-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="60b71-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60b71-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60b71-123">-InputObject</span></span>
<span data-ttu-id="60b71-124">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="60b71-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="60b71-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="60b71-125">-InRemovedState</span></span>
<span data-ttu-id="60b71-126">Anger om de tidigare borttagna säkerhets associationerna för lagring ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="60b71-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="60b71-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="60b71-127">-Name</span></span>
<span data-ttu-id="60b71-128">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="60b71-128">Storage sas definition name.</span></span>
<span data-ttu-id="60b71-129">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="60b71-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="60b71-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="60b71-130">-VaultName</span></span>
<span data-ttu-id="60b71-131">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="60b71-131">Vault name.</span></span>
<span data-ttu-id="60b71-132">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="60b71-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="60b71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b71-133">CommonParameters</span></span>
<span data-ttu-id="60b71-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b71-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60b71-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b71-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60b71-136">INPUTS</span></span>

### <span data-ttu-id="60b71-137">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="60b71-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="60b71-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60b71-138">OUTPUTS</span></span>

### <span data-ttu-id="60b71-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="60b71-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="60b71-140">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="60b71-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="60b71-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="60b71-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="60b71-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="60b71-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="60b71-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60b71-143">NOTES</span></span>

## <span data-ttu-id="60b71-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60b71-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

