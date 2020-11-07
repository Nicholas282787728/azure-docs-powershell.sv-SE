---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 183618058d6400798dc2af74975fd45a0a397b16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743850"
---
# <span data-ttu-id="72fe4-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72fe4-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="72fe4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="72fe4-103">Uppdatera redigerbara attribut för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="72fe4-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="72fe4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72fe4-104">SYNTAX</span></span>

### <span data-ttu-id="72fe4-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="72fe4-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72fe4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="72fe4-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72fe4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="72fe4-108">Uppdatera de redigerbara attributen för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="72fe4-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="72fe4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="72fe4-110">Exempel 1: uppdatera den aktiva knappen till ' key2 ' på ett hanterat Azure Storage-konto på Key valv.</span><span class="sxs-lookup"><span data-stu-id="72fe4-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="72fe4-111">Uppdaterar den centrala Key valv-hanterade Azure Storage-kontots aktiva nycklar till ' key2 '.</span><span class="sxs-lookup"><span data-stu-id="72fe4-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="72fe4-112">' key2 ' kommer att användas för att skapa SAS-token efter den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="72fe4-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="72fe4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72fe4-113">PARAMETERS</span></span>

### <span data-ttu-id="72fe4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72fe4-114">-AccountName</span></span>
<span data-ttu-id="72fe4-115">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="72fe4-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="72fe4-116">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="72fe4-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="72fe4-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="72fe4-117">-ActiveKeyName</span></span>
<span data-ttu-id="72fe4-118">Namn på aktiva nycklar.</span><span class="sxs-lookup"><span data-stu-id="72fe4-118">Active key name.</span></span>
<span data-ttu-id="72fe4-119">Om det inte anges ändras inte det befintliga värdet för hanterat lagrings kontots aktiva namn</span><span class="sxs-lookup"><span data-stu-id="72fe4-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="72fe4-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="72fe4-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="72fe4-121">Autoåterskapa-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="72fe4-121">Auto regenerate key.</span></span>
<span data-ttu-id="72fe4-122">Om det inte anges ändras inte det befintliga värdet för automatisk återskapande av hanterade lagrings konton</span><span class="sxs-lookup"><span data-stu-id="72fe4-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fe4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fe4-123">-DefaultProfile</span></span>
<span data-ttu-id="72fe4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72fe4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72fe4-125">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="72fe4-125">-Enable</span></span>
<span data-ttu-id="72fe4-126">Om du presenterar kan du använda en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="72fe4-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="72fe4-127">Inaktiverar användning av en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="72fe4-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="72fe4-128">Om inget anges ändras inte det befintliga värdet för lagrings kontots status med aktiverat/inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="72fe4-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fe4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72fe4-129">-InputObject</span></span>
<span data-ttu-id="72fe4-130">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="72fe4-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="72fe4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72fe4-131">-PassThru</span></span>
<span data-ttu-id="72fe4-132">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="72fe4-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="72fe4-133">Om den här växeln anges kan du returnera hanterat lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="72fe4-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="72fe4-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="72fe4-134">-RegenerationPeriod</span></span>
<span data-ttu-id="72fe4-135">Återställnings period.</span><span class="sxs-lookup"><span data-stu-id="72fe4-135">Regeneration period.</span></span> <span data-ttu-id="72fe4-136">Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatisk omgenerering av nycklar och blir den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="72fe4-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="72fe4-137">Om du inte anger det befintliga värdet för återställnings periodens nycklar för hanterade lagrings konton är oförändrade</span><span class="sxs-lookup"><span data-stu-id="72fe4-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fe4-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="72fe4-138">-Tag</span></span>
<span data-ttu-id="72fe4-139">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="72fe4-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72fe4-140">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="72fe4-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fe4-141">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72fe4-141">-VaultName</span></span>
<span data-ttu-id="72fe4-142">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="72fe4-142">Vault name.</span></span>
<span data-ttu-id="72fe4-143">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="72fe4-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="72fe4-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72fe4-144">-Confirm</span></span>
<span data-ttu-id="72fe4-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72fe4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fe4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fe4-146">-WhatIf</span></span>
<span data-ttu-id="72fe4-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72fe4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fe4-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72fe4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fe4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fe4-149">CommonParameters</span></span>
<span data-ttu-id="72fe4-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fe4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fe4-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fe4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fe4-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72fe4-152">INPUTS</span></span>

### <span data-ttu-id="72fe4-153">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72fe4-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="72fe4-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72fe4-154">OUTPUTS</span></span>

### <span data-ttu-id="72fe4-155">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72fe4-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="72fe4-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72fe4-156">NOTES</span></span>

## <span data-ttu-id="72fe4-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72fe4-157">RELATED LINKS</span></span>

[<span data-ttu-id="72fe4-158">AZ.</span><span class="sxs-lookup"><span data-stu-id="72fe4-158">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
