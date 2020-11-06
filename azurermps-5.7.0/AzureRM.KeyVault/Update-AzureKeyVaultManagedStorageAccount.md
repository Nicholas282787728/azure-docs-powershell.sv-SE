---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575631"
---
# <span data-ttu-id="3e8ed-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e8ed-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3e8ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8ed-103">Uppdatera redigerbara attribut för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e8ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e8ed-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e8ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3e8ed-106">Uppdatera de redigerbara attributen för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3e8ed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="3e8ed-108">Exempel 1: uppdatera den aktiva knappen till ' key2 ' på ett hanterat Azure Storage-konto på Key valv.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="3e8ed-109">Uppdaterar den centrala Key valv-hanterade Azure Storage-kontots aktiva nycklar till ' key2 '.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="3e8ed-110">' key2 ' kommer att användas för att skapa SAS-token efter den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="3e8ed-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e8ed-111">PARAMETERS</span></span>

### <span data-ttu-id="3e8ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e8ed-112">-AccountName</span></span>
<span data-ttu-id="3e8ed-113">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="3e8ed-114">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="3e8ed-115">-ActiveKeyName</span></span>
<span data-ttu-id="3e8ed-116">Namn på aktiva nycklar.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-116">Active key name.</span></span>
<span data-ttu-id="3e8ed-117">Om det inte anges ändras inte det befintliga värdet för hanterat lagrings kontots aktiva namn</span><span class="sxs-lookup"><span data-stu-id="3e8ed-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="3e8ed-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="3e8ed-119">Autoåterskapa-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-119">Auto regenerate key.</span></span>
<span data-ttu-id="3e8ed-120">Om det inte anges ändras inte det befintliga värdet för automatisk återskapande av hanterade lagrings konton</span><span class="sxs-lookup"><span data-stu-id="3e8ed-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8ed-121">-DefaultProfile</span></span>
<span data-ttu-id="3e8ed-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3e8ed-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-123">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="3e8ed-123">-Enable</span></span>
<span data-ttu-id="3e8ed-124">Om du presenterar kan du använda en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="3e8ed-125">Inaktiverar användning av en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="3e8ed-126">Om inget anges ändras inte det befintliga värdet för lagrings kontots status med aktiverat/inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e8ed-127">-PassThru</span></span>
<span data-ttu-id="3e8ed-128">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="3e8ed-129">Om den här växeln anges kan du returnera hanterat lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-129">If this switch is specified, return managed storage account object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="3e8ed-130">-RegenerationPeriod</span></span>
<span data-ttu-id="3e8ed-131">Återställnings period.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-131">Regeneration period.</span></span> <span data-ttu-id="3e8ed-132">Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatisk omgenerering av nycklar och blir den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="3e8ed-133">Om du inte anger det befintliga värdet för återställnings periodens nycklar för hanterade lagrings konton är oförändrade</span><span class="sxs-lookup"><span data-stu-id="3e8ed-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e8ed-134">-Tag</span></span>
<span data-ttu-id="3e8ed-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e8ed-136">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3e8ed-136">For example:</span></span>

<span data-ttu-id="3e8ed-137">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3e8ed-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e8ed-138">-VaultName</span></span>
<span data-ttu-id="3e8ed-139">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-139">Vault name.</span></span>
<span data-ttu-id="3e8ed-140">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3e8ed-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e8ed-141">-Confirm</span></span>
<span data-ttu-id="3e8ed-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8ed-143">-WhatIf</span></span>
<span data-ttu-id="3e8ed-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8ed-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8ed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8ed-146">CommonParameters</span></span>
<span data-ttu-id="3e8ed-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8ed-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8ed-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8ed-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e8ed-149">INPUTS</span></span>

### <span data-ttu-id="3e8ed-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e8ed-150">None</span></span>
<span data-ttu-id="3e8ed-151">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e8ed-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e8ed-152">OUTPUTS</span></span>

### <span data-ttu-id="3e8ed-153">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e8ed-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="3e8ed-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e8ed-154">NOTES</span></span>

## <span data-ttu-id="3e8ed-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e8ed-155">RELATED LINKS</span></span>

[<span data-ttu-id="3e8ed-156">AzureRM.</span><span class="sxs-lookup"><span data-stu-id="3e8ed-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
