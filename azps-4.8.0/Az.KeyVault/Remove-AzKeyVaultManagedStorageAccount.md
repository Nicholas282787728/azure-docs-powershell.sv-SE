---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259451"
---
# <span data-ttu-id="db7c7-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db7c7-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="db7c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="db7c7-103">Tar bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="db7c7-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="db7c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db7c7-104">SYNTAX</span></span>

### <span data-ttu-id="db7c7-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="db7c7-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7c7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db7c7-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db7c7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db7c7-107">DESCRIPTION</span></span>
<span data-ttu-id="db7c7-108">Avassocierar ett Azure Storage-konto från Key Vault.</span><span class="sxs-lookup"><span data-stu-id="db7c7-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="db7c7-109">Detta tar inte bort ett Azure Storage-konto, men tar bort konto nycklarna från att hanteras av Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="db7c7-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="db7c7-110">Alla tillhör ande säkerhets associationer för hanterade nycklar för nyckelbaserad lagring tas också bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="db7c7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db7c7-111">EXAMPLES</span></span>

### <span data-ttu-id="db7c7-112">Exempel 1: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="db7c7-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

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

<span data-ttu-id="db7c7-113">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="db7c7-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="db7c7-114">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="db7c7-115">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="db7c7-116">Exempel 2: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande sa-definitioner utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db7c7-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

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

<span data-ttu-id="db7c7-117">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="db7c7-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="db7c7-118">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="db7c7-119">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="db7c7-120">Exempel 3: ta bort (rensa) ett nyckeltal som hanteras av Azure Storage-konto och alla tillhör ande sa-definitioner från ett valv med mjuka borttagningar.</span><span class="sxs-lookup"><span data-stu-id="db7c7-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="db7c7-121">I exemplet förutsätts att mjuk borttagning är aktiverat för det här valvet.</span><span class="sxs-lookup"><span data-stu-id="db7c7-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="db7c7-122">Kontrol lera om det är fallet genom att undersöka egenskaperna för valvet, eller RecoveryLevel-attributet för en entitet i valvet.</span><span class="sxs-lookup"><span data-stu-id="db7c7-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="db7c7-123">Den första cmdleten avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="db7c7-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="db7c7-124">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="db7c7-125">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="db7c7-126">Den andra cmdleten verifierar att lagrings kontot är i ett borttaget, men kan återställnings Bart.</span><span class="sxs-lookup"><span data-stu-id="db7c7-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="db7c7-127">Att nå detta tillstånd kan kräva lite tid, ange ~ 30s innan du försöker.</span><span class="sxs-lookup"><span data-stu-id="db7c7-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="db7c7-128">Den tredje cmdleten tar permanent bort lagrings kontot – återställning kommer inte längre att vara möjlig.</span><span class="sxs-lookup"><span data-stu-id="db7c7-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="db7c7-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db7c7-129">PARAMETERS</span></span>

### <span data-ttu-id="db7c7-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db7c7-130">-AccountName</span></span>
<span data-ttu-id="db7c7-131">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="db7c7-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="db7c7-132">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="db7c7-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7c7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7c7-133">-DefaultProfile</span></span>
<span data-ttu-id="db7c7-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="db7c7-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db7c7-135">-Force</span><span class="sxs-lookup"><span data-stu-id="db7c7-135">-Force</span></span>
<span data-ttu-id="db7c7-136">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db7c7-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="db7c7-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db7c7-137">-InputObject</span></span>
<span data-ttu-id="db7c7-138">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="db7c7-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="db7c7-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="db7c7-139">-InRemovedState</span></span>
<span data-ttu-id="db7c7-140">Ta bort tidigare borttagna lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="db7c7-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="db7c7-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db7c7-141">-PassThru</span></span>
<span data-ttu-id="db7c7-142">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="db7c7-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="db7c7-143">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="db7c7-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="db7c7-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="db7c7-144">-VaultName</span></span>
<span data-ttu-id="db7c7-145">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="db7c7-145">Vault name.</span></span>
<span data-ttu-id="db7c7-146">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="db7c7-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="db7c7-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db7c7-147">-Confirm</span></span>
<span data-ttu-id="db7c7-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db7c7-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7c7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7c7-149">-WhatIf</span></span>
<span data-ttu-id="db7c7-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db7c7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db7c7-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db7c7-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7c7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7c7-152">CommonParameters</span></span>
<span data-ttu-id="db7c7-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db7c7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7c7-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db7c7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7c7-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db7c7-155">INPUTS</span></span>

### <span data-ttu-id="db7c7-156">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="db7c7-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="db7c7-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db7c7-157">OUTPUTS</span></span>

### <span data-ttu-id="db7c7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db7c7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="db7c7-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db7c7-159">NOTES</span></span>

## <span data-ttu-id="db7c7-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db7c7-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

