---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103218"
---
# <span data-ttu-id="77f03-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77f03-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="77f03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77f03-102">SYNOPSIS</span></span>
<span data-ttu-id="77f03-103">Lägger till ett befintligt Azure Storage-konto till det angivna nyckel valvet för dess nycklar för att hanteras av nyckel valv tjänsten.</span><span class="sxs-lookup"><span data-stu-id="77f03-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="77f03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77f03-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77f03-105">DESCRIPTION</span></span>
<span data-ttu-id="77f03-106">Konfigurerar ett befintligt Azure Storage-konto med nyckel valv för lagrings konto nycklar som ska hanteras av nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="77f03-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="77f03-107">Lagrings kontot måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="77f03-107">The Storage Account must already exist.</span></span> <span data-ttu-id="77f03-108">Lagrings nycklarna exponeras aldrig för den som ringer.</span><span class="sxs-lookup"><span data-stu-id="77f03-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="77f03-109">Key valv regenererar och växlar den aktiva nyckeln automatiskt baserat på återställnings perioden.</span><span class="sxs-lookup"><span data-stu-id="77f03-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="77f03-110">Se [hanterat lagrings konto för Azure Key valv – PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) för en översikt över den här funktionen.</span><span class="sxs-lookup"><span data-stu-id="77f03-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="77f03-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77f03-111">EXAMPLES</span></span>

### <span data-ttu-id="77f03-112">Exempel 1: Ange ett Azure Storage-konto med nyckel valv för att hantera dess nycklar</span><span class="sxs-lookup"><span data-stu-id="77f03-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="77f03-113">Ställer in ett lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="77f03-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="77f03-114">Den aktiva knappen är ' KEY1 '.</span><span class="sxs-lookup"><span data-stu-id="77f03-114">The active key set is 'key1'.</span></span> <span data-ttu-id="77f03-115">Denna nyckel används för att generera SAS-token.</span><span class="sxs-lookup"><span data-stu-id="77f03-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="77f03-116">Key valv återskapar ' key2 '-nyckeln efter återgenererings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="77f03-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="77f03-117">Den här processen för automatisk förnyelse fortsätter mellan ' KEY1 ' och ' key2 ' med en lucka på 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="77f03-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="77f03-118">Exempel 2: Ange ett klassiskt Azure Storage-konto med nyckel valv för att hantera dess nycklar</span><span class="sxs-lookup"><span data-stu-id="77f03-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="77f03-119">Ställer in ett klassiskt lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="77f03-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="77f03-120">Den aktiva tangenten är "primär".</span><span class="sxs-lookup"><span data-stu-id="77f03-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="77f03-121">Denna nyckel används för att generera SAS-token.</span><span class="sxs-lookup"><span data-stu-id="77f03-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="77f03-122">Key valv återskapar ' sekundär '-nyckeln efter återställnings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="77f03-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="77f03-123">Den här processen för automatisk förnyelse fortsätter mellan ' primär ' och ' sekundär ' med en lucka på 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="77f03-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="77f03-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77f03-124">PARAMETERS</span></span>

### <span data-ttu-id="77f03-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77f03-125">-AccountName</span></span>
<span data-ttu-id="77f03-126">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="77f03-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="77f03-127">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="77f03-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="77f03-128">-AccountResourceId</span></span>
<span data-ttu-id="77f03-129">Azure Resource ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="77f03-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="77f03-130">-ActiveKeyName</span></span>
<span data-ttu-id="77f03-131">Namn på lagrings konto nyckeln som måste användas för att skapa SAS-token.</span><span class="sxs-lookup"><span data-stu-id="77f03-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f03-132">-DefaultProfile</span></span>
<span data-ttu-id="77f03-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="77f03-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77f03-134">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="77f03-134">-Disable</span></span>
<span data-ttu-id="77f03-135">Inaktiverar användning av hanterat lagrings kontots nyckel för generering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="77f03-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="77f03-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="77f03-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="77f03-137">Autoåterskapa-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="77f03-137">Auto regenerate key.</span></span> <span data-ttu-id="77f03-138">Om värdet är true får det hanterade lagrings kontots inaktiva nycklar automatisk omgenerering och blir den nya aktiva nyckeln efter återställnings perioden.</span><span class="sxs-lookup"><span data-stu-id="77f03-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="77f03-139">Om det här är falskt skapas inte nycklar för hanterat lagrings konto automatiskt.</span><span class="sxs-lookup"><span data-stu-id="77f03-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="77f03-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="77f03-140">-RegenerationPeriod</span></span>
<span data-ttu-id="77f03-141">Återställnings period.</span><span class="sxs-lookup"><span data-stu-id="77f03-141">Regeneration period.</span></span> <span data-ttu-id="77f03-142">Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatiskt återskapande lagrings konto och blir den nya aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="77f03-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="77f03-143">-Tag</span></span>
<span data-ttu-id="77f03-144">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="77f03-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="77f03-145">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="77f03-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77f03-146">-VaultName</span></span>
<span data-ttu-id="77f03-147">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="77f03-147">Vault name.</span></span>
<span data-ttu-id="77f03-148">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="77f03-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f03-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77f03-149">-Confirm</span></span>
<span data-ttu-id="77f03-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77f03-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f03-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f03-151">-WhatIf</span></span>
<span data-ttu-id="77f03-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77f03-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f03-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77f03-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f03-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f03-154">CommonParameters</span></span>
<span data-ttu-id="77f03-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f03-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f03-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f03-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f03-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77f03-157">INPUTS</span></span>

### <span data-ttu-id="77f03-158">System. String</span><span class="sxs-lookup"><span data-stu-id="77f03-158">System.String</span></span>

### <span data-ttu-id="77f03-159">System. Nullable ' 1 [[system. TimeSpan, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77f03-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77f03-160">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="77f03-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="77f03-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77f03-161">OUTPUTS</span></span>

### <span data-ttu-id="77f03-162">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77f03-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="77f03-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77f03-163">NOTES</span></span>

## <span data-ttu-id="77f03-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77f03-164">RELATED LINKS</span></span>

[<span data-ttu-id="77f03-165">AZ.</span><span class="sxs-lookup"><span data-stu-id="77f03-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
