---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ea3d16ec55186017852df30f6ff745f79703f224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924417"
---
# <span data-ttu-id="65f8f-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65f8f-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="65f8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="65f8f-103">Uppdatera redigerbara attribut för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="65f8f-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="65f8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65f8f-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65f8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="65f8f-106">Uppdatera de redigerbara attributen för ett Key valv-hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="65f8f-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="65f8f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="65f8f-108">Exempel 1: uppdatera den aktiva knappen till ' key2 ' på ett hanterat Azure Storage-konto på Key valv.</span><span class="sxs-lookup"><span data-stu-id="65f8f-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="65f8f-109">Uppdaterar den centrala Key valv-hanterade Azure Storage-kontots aktiva nycklar till ' key2 '.</span><span class="sxs-lookup"><span data-stu-id="65f8f-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="65f8f-110">' key2 ' kommer att användas för att skapa SAS-token efter den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="65f8f-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="65f8f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65f8f-111">PARAMETERS</span></span>

### <span data-ttu-id="65f8f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65f8f-112">-AccountName</span></span>
<span data-ttu-id="65f8f-113">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="65f8f-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="65f8f-114">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="65f8f-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="65f8f-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="65f8f-115">-ActiveKeyName</span></span>
<span data-ttu-id="65f8f-116">Namn på aktiva nycklar.</span><span class="sxs-lookup"><span data-stu-id="65f8f-116">Active key name.</span></span>
<span data-ttu-id="65f8f-117">Om det inte anges ändras inte det befintliga värdet för hanterat lagrings kontots aktiva namn</span><span class="sxs-lookup"><span data-stu-id="65f8f-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="65f8f-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="65f8f-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="65f8f-119">Autoåterskapa-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="65f8f-119">Auto regenerate key.</span></span>
<span data-ttu-id="65f8f-120">Om det inte anges ändras inte det befintliga värdet för automatisk återskapande av hanterade lagrings konton</span><span class="sxs-lookup"><span data-stu-id="65f8f-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="65f8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f8f-121">-DefaultProfile</span></span>
<span data-ttu-id="65f8f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="65f8f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65f8f-123">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="65f8f-123">-Enable</span></span>
<span data-ttu-id="65f8f-124">Om du presenterar kan du använda en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är sant.</span><span class="sxs-lookup"><span data-stu-id="65f8f-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="65f8f-125">Inaktiverar användning av en nyckel för hanterad lagrings konto för att skapa SAS-token om värdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="65f8f-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="65f8f-126">Om inget anges ändras inte det befintliga värdet för lagrings kontots status med aktiverat/inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="65f8f-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="65f8f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65f8f-127">-PassThru</span></span>
<span data-ttu-id="65f8f-128">Cmdlet returnerar inte objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="65f8f-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="65f8f-129">Om den här växeln anges kan du returnera hanterat lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="65f8f-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="65f8f-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="65f8f-130">-RegenerationPeriod</span></span>
<span data-ttu-id="65f8f-131">Återställnings period.</span><span class="sxs-lookup"><span data-stu-id="65f8f-131">Regeneration period.</span></span> <span data-ttu-id="65f8f-132">Om automatisk återskapande-nyckeln är aktive rad anger det TimeSpan efter vilket hanterat inaktivt automatisk omgenerering av nycklar och blir den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="65f8f-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="65f8f-133">Om du inte anger det befintliga värdet för återställnings periodens nycklar för hanterade lagrings konton är oförändrade</span><span class="sxs-lookup"><span data-stu-id="65f8f-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="65f8f-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="65f8f-134">-Tag</span></span>
<span data-ttu-id="65f8f-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="65f8f-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65f8f-136">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="65f8f-136">For example:</span></span>

<span data-ttu-id="65f8f-137">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="65f8f-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="65f8f-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="65f8f-138">-VaultName</span></span>
<span data-ttu-id="65f8f-139">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="65f8f-139">Vault name.</span></span>
<span data-ttu-id="65f8f-140">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="65f8f-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="65f8f-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65f8f-141">-Confirm</span></span>
<span data-ttu-id="65f8f-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65f8f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f8f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f8f-143">-WhatIf</span></span>
<span data-ttu-id="65f8f-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65f8f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f8f-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65f8f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f8f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f8f-146">CommonParameters</span></span>
<span data-ttu-id="65f8f-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f8f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f8f-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65f8f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f8f-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65f8f-149">INPUTS</span></span>

### <span data-ttu-id="65f8f-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="65f8f-150">None</span></span>
<span data-ttu-id="65f8f-151">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="65f8f-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65f8f-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65f8f-152">OUTPUTS</span></span>

### <span data-ttu-id="65f8f-153">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65f8f-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="65f8f-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65f8f-154">NOTES</span></span>

## <span data-ttu-id="65f8f-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65f8f-155">RELATED LINKS</span></span>

[<span data-ttu-id="65f8f-156">AZ.</span><span class="sxs-lookup"><span data-stu-id="65f8f-156">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
