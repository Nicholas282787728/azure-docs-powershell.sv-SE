---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 165419eb13376becedf72b4e44ee17f0c3655ec4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916322"
---
# <span data-ttu-id="154cf-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="154cf-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="154cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="154cf-102">SYNOPSIS</span></span>
<span data-ttu-id="154cf-103">Hämtar Key valv-hanterade Azure Storage-konton.</span><span class="sxs-lookup"><span data-stu-id="154cf-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="154cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="154cf-104">SYNTAX</span></span>

### <span data-ttu-id="154cf-105">ByAccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="154cf-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="154cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="154cf-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="154cf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="154cf-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="154cf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="154cf-108">DESCRIPTION</span></span>
<span data-ttu-id="154cf-109">Hämtar ett nyckel valv hanterat Azure Storage-konto om namnet på kontot anges och konto nycklarna hanteras av det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="154cf-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="154cf-110">Om konto namnet inte anges visas alla konton vars nycklar hanteras av angivet valv.</span><span class="sxs-lookup"><span data-stu-id="154cf-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="154cf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="154cf-111">EXAMPLES</span></span>

### <span data-ttu-id="154cf-112">Exempel 1: lista alla hanterade lagrings konton för viktiga valv nycklar</span><span class="sxs-lookup"><span data-stu-id="154cf-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="154cf-113">Visar alla konton vars nycklar hanteras av valv ' Mina valv '</span><span class="sxs-lookup"><span data-stu-id="154cf-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="154cf-114">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="154cf-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="154cf-115">Hämtar information om Key valv Managed Storage-kontot för ' mystorageaccount ' om dess nycklar hanteras av valvet ' för valv '</span><span class="sxs-lookup"><span data-stu-id="154cf-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="154cf-116">Exempel 3: Visa alla hanterade lagrings konton för viktiga valv med filtrering</span><span class="sxs-lookup"><span data-stu-id="154cf-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="154cf-117">Visar alla konton vars nycklar hanteras av valvet "mina valv" som börjar med "test"</span><span class="sxs-lookup"><span data-stu-id="154cf-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="154cf-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="154cf-118">PARAMETERS</span></span>

### <span data-ttu-id="154cf-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="154cf-119">-AccountName</span></span>
<span data-ttu-id="154cf-120">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="154cf-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="154cf-121">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="154cf-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="154cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154cf-122">-DefaultProfile</span></span>
<span data-ttu-id="154cf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="154cf-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="154cf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154cf-124">-InputObject</span></span>
<span data-ttu-id="154cf-125">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="154cf-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="154cf-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="154cf-126">-InRemovedState</span></span>
<span data-ttu-id="154cf-127">Anger om tidigare borttagna lagrings konton ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="154cf-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="154cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154cf-128">-ResourceId</span></span>
<span data-ttu-id="154cf-129">Valv resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="154cf-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154cf-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="154cf-130">-VaultName</span></span>
<span data-ttu-id="154cf-131">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="154cf-131">Vault name.</span></span>
<span data-ttu-id="154cf-132">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="154cf-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154cf-133">CommonParameters</span></span>
<span data-ttu-id="154cf-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154cf-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="154cf-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154cf-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="154cf-136">INPUTS</span></span>

### <span data-ttu-id="154cf-137">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="154cf-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="154cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="154cf-138">System.String</span></span>

## <span data-ttu-id="154cf-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="154cf-139">OUTPUTS</span></span>

### <span data-ttu-id="154cf-140">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="154cf-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="154cf-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="154cf-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="154cf-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="154cf-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="154cf-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="154cf-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="154cf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="154cf-144">NOTES</span></span>

## <span data-ttu-id="154cf-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="154cf-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
