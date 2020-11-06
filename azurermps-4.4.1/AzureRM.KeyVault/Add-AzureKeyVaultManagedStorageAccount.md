---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 820a1c84600a3fb143d2b3c34a81e1f7cedac0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586520"
---
# <span data-ttu-id="ed410-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed410-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ed410-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed410-102">SYNOPSIS</span></span>
<span data-ttu-id="ed410-103">Lägger till ett befintligt Azure Storage-konto till det angivna nyckel valvet för dess nycklar för att hanteras av nyckel valv tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed410-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed410-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed410-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed410-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed410-105">DESCRIPTION</span></span>
<span data-ttu-id="ed410-106">Konfigurerar ett befintligt Azure Storage-konto med nyckel valv för lagrings konto nycklar som ska hanteras av nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="ed410-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="ed410-107">Lagrings kontot måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="ed410-107">The Storage Account must already exist.</span></span> <span data-ttu-id="ed410-108">Lagrings nycklarna exponeras aldrig för den som ringer.</span><span class="sxs-lookup"><span data-stu-id="ed410-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="ed410-109">Key valv regenererar och växlar den aktiva nyckeln automatiskt baserat på återställnings perioden.</span><span class="sxs-lookup"><span data-stu-id="ed410-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="ed410-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed410-110">EXAMPLES</span></span>

### <span data-ttu-id="ed410-111">Exempel 1: Ange ett Azure Storage-konto med nyckel valv för att hantera dess nycklar</span><span class="sxs-lookup"><span data-stu-id="ed410-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="ed410-112">Ställer in ett lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="ed410-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="ed410-113">Den aktiva knappen är ' KEY1 '.</span><span class="sxs-lookup"><span data-stu-id="ed410-113">The active key set is 'key1'.</span></span> <span data-ttu-id="ed410-114">Denna nyckel används för att generera SAS-token.</span><span class="sxs-lookup"><span data-stu-id="ed410-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="ed410-115">Key valv återskapar ' key2 '-nyckeln efter återgenererings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ed410-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="ed410-116">Den här processen för automatisk förnyelse fortsätter mellan ' KEY1 ' och ' key2 ' med en lucka på 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="ed410-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="ed410-117">Exempel 2: Ange ett klassiskt Azure Storage-konto med nyckel valv för att hantera dess nycklar</span><span class="sxs-lookup"><span data-stu-id="ed410-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="ed410-118">Ställer in ett klassiskt lagrings konto med nyckel valv för dess nycklar för att hanteras av nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="ed410-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="ed410-119">Den aktiva tangenten är "primär".</span><span class="sxs-lookup"><span data-stu-id="ed410-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="ed410-120">Denna nyckel används för att generera SAS-token.</span><span class="sxs-lookup"><span data-stu-id="ed410-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="ed410-121">Key valv återskapar ' sekundär '-nyckeln efter återställnings perioden från tiden för det här kommandot och ange den som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ed410-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="ed410-122">Den här processen för automatisk förnyelse fortsätter mellan ' primär ' och ' sekundär ' med en lucka på 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="ed410-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="ed410-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed410-123">PARAMETERS</span></span>

### <span data-ttu-id="ed410-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed410-124">-AccountName</span></span>
<span data-ttu-id="ed410-125">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="ed410-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="ed410-126">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="ed410-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="ed410-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ed410-127">-AccountResourceId</span></span>
<span data-ttu-id="ed410-128">Azure Resource ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ed410-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="ed410-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="ed410-129">-ActiveKeyName</span></span>
<span data-ttu-id="ed410-130">Namn på lagrings konto nyckeln som måste användas för att skapa SAS-token.</span><span class="sxs-lookup"><span data-stu-id="ed410-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="ed410-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed410-131">-Confirm</span></span>
<span data-ttu-id="ed410-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed410-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed410-133">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="ed410-133">-Disable</span></span>
<span data-ttu-id="ed410-134">Inaktiverar användning av hanterat lagrings kontots nyckel för generering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="ed410-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="ed410-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ed410-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="ed410-136">Autoåterskapa-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ed410-136">Auto regenerate key.</span></span> <span data-ttu-id="ed410-137">Om värdet är true får det hanterade lagrings kontots inaktiva nycklar automatisk omgenerering och blir den nya aktiva nyckeln efter återställnings perioden.</span><span class="sxs-lookup"><span data-stu-id="ed410-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="ed410-138">Om det här är falskt skapas inte nycklar för hanterat lagrings konto automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ed410-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="ed410-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="ed410-139">-RegenerationPeriod</span></span>
<span data-ttu-id="ed410-140">Återställnings period.</span><span class="sxs-lookup"><span data-stu-id="ed410-140">Regeneration period.</span></span> <span data-ttu-id="ed410-141">Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatiskt återskapande lagrings konto och blir den nya aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ed410-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="ed410-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ed410-142">-Tag</span></span>
<span data-ttu-id="ed410-143">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ed410-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed410-144">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ed410-144">For example:</span></span>

<span data-ttu-id="ed410-145">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ed410-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ed410-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ed410-146">-VaultName</span></span>
<span data-ttu-id="ed410-147">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="ed410-147">Vault name.</span></span>
<span data-ttu-id="ed410-148">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="ed410-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ed410-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed410-149">-WhatIf</span></span>
<span data-ttu-id="ed410-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed410-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed410-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed410-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed410-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed410-152">-DefaultProfile</span></span>
<span data-ttu-id="ed410-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed410-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed410-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed410-154">CommonParameters</span></span>
<span data-ttu-id="ed410-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed410-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed410-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed410-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed410-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed410-157">INPUTS</span></span>

## <span data-ttu-id="ed410-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed410-158">OUTPUTS</span></span>

### <span data-ttu-id="ed410-159">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed410-159">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="ed410-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed410-160">NOTES</span></span>

## <span data-ttu-id="ed410-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed410-161">RELATED LINKS</span></span>

[<span data-ttu-id="ed410-162">AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ed410-162">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
