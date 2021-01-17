---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419891"
---
# <span data-ttu-id="4a030-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4a030-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="4a030-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a030-102">SYNOPSIS</span></span>
<span data-ttu-id="4a030-103">Ändra en krypterings omfattning för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4a030-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="4a030-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a030-104">SYNTAX</span></span>

### <span data-ttu-id="4a030-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="4a030-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a030-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="4a030-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a030-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4a030-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a030-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="4a030-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a030-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="4a030-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a030-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="4a030-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a030-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a030-111">DESCRIPTION</span></span>
<span data-ttu-id="4a030-112">Cmdleten **Update-AzStorageEncryptionScope** ändrar en krypterings omfattning för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4a030-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="4a030-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a030-113">EXAMPLES</span></span>

### <span data-ttu-id="4a030-114">Exempel 1: inaktivera en krypterings omfattning</span><span class="sxs-lookup"><span data-stu-id="4a030-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="4a030-115">Det här kommandot inaktiverar en krypterings omfattning.</span><span class="sxs-lookup"><span data-stu-id="4a030-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="4a030-116">Exempel 2: Aktivera en krypterings omfattning</span><span class="sxs-lookup"><span data-stu-id="4a030-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="4a030-117">Det här kommandot aktiverar en krypterings omfattning.</span><span class="sxs-lookup"><span data-stu-id="4a030-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="4a030-118">Exempel 3: uppdatera en krypterings omfattning för att använda lagrings kryptering</span><span class="sxs-lookup"><span data-stu-id="4a030-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="4a030-119">Det här kommandot uppdaterar en krypterings omfattning för att använda lagrings kryptering.</span><span class="sxs-lookup"><span data-stu-id="4a030-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="4a030-120">Exempel 4: uppdatera en krypterings omfattning för att använda valv kryptering</span><span class="sxs-lookup"><span data-stu-id="4a030-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="4a030-121">Det här kommandot updtaes ett krypterings omfång för att använda valv kryptering.</span><span class="sxs-lookup"><span data-stu-id="4a030-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="4a030-122">Lagrings kontots identitet måste ha get, wrapkey, unwrapkey-behörigheter till Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="4a030-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="4a030-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a030-123">PARAMETERS</span></span>

### <span data-ttu-id="4a030-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a030-124">-DefaultProfile</span></span>
<span data-ttu-id="4a030-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a030-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a030-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="4a030-126">-EncryptionScopeName</span></span>
<span data-ttu-id="4a030-127">Namn på Azure-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4a030-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a030-128">-InputObject</span></span>
<span data-ttu-id="4a030-129">EncryptionScope-objekt</span><span class="sxs-lookup"><span data-stu-id="4a030-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="4a030-130">-KeyUri</span></span>
<span data-ttu-id="4a030-131">Key URI</span><span class="sxs-lookup"><span data-stu-id="4a030-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="4a030-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="4a030-133">Skapa krypterings omfång med Minin as Microsoft.-valv</span><span class="sxs-lookup"><span data-stu-id="4a030-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a030-134">-ResourceGroupName</span></span>
<span data-ttu-id="4a030-135">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4a030-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-136">-State</span><span class="sxs-lookup"><span data-stu-id="4a030-136">-State</span></span>
<span data-ttu-id="4a030-137">Uppdatering krypterings omfattning, möjliga värden inkluderar: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="4a030-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a030-138">-StorageAccount</span></span>
<span data-ttu-id="4a030-139">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="4a030-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a030-140">-StorageAccountName</span></span>
<span data-ttu-id="4a030-141">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4a030-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="4a030-142">-StorageEncryption</span></span>
<span data-ttu-id="4a030-143">Skapa krypterings omfång med Minin källkod som Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="4a030-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a030-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a030-144">-Confirm</span></span>
<span data-ttu-id="4a030-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a030-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a030-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a030-146">-WhatIf</span></span>
<span data-ttu-id="4a030-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a030-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a030-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a030-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a030-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a030-149">CommonParameters</span></span>
<span data-ttu-id="4a030-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a030-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a030-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a030-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a030-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a030-152">INPUTS</span></span>

### <span data-ttu-id="4a030-153">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a030-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4a030-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a030-154">OUTPUTS</span></span>

### <span data-ttu-id="4a030-155">Microsoft. Azure. commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4a030-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="4a030-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a030-156">NOTES</span></span>

## <span data-ttu-id="4a030-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a030-157">RELATED LINKS</span></span>
