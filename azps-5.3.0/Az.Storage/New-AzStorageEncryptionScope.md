---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522020"
---
# <span data-ttu-id="21d02-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="21d02-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="21d02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21d02-102">SYNOPSIS</span></span>
<span data-ttu-id="21d02-103">Skapar en krypterings omfattning för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="21d02-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="21d02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21d02-104">SYNTAX</span></span>

### <span data-ttu-id="21d02-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="21d02-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d02-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="21d02-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d02-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="21d02-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d02-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="21d02-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21d02-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21d02-109">DESCRIPTION</span></span>
<span data-ttu-id="21d02-110">Cmdleten **New-AzStorageEncryptionScope** skapar en krypterings omfattning för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="21d02-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="21d02-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21d02-111">EXAMPLES</span></span>

### <span data-ttu-id="21d02-112">Exempel 1: skapa ett krypterings omfång med lagrings kryptering</span><span class="sxs-lookup"><span data-stu-id="21d02-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="21d02-113">Det här kommandot skapar ett krypterings omfång med lagrings kryptering.</span><span class="sxs-lookup"><span data-stu-id="21d02-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="21d02-114">Exempel 2: skapa en krypterings omfattning med valv kryptering</span><span class="sxs-lookup"><span data-stu-id="21d02-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="21d02-115">Det här kommandot skapar en krypterings omfattning med valv kryptering.</span><span class="sxs-lookup"><span data-stu-id="21d02-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="21d02-116">Lagrings kontots identitet måste ha get, wrapkey, unwrapkey-behörigheter till Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="21d02-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="21d02-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21d02-117">PARAMETERS</span></span>

### <span data-ttu-id="21d02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d02-118">-DefaultProfile</span></span>
<span data-ttu-id="21d02-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21d02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d02-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="21d02-120">-EncryptionScopeName</span></span>
<span data-ttu-id="21d02-121">Namn på Azure-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="21d02-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d02-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="21d02-122">-KeyUri</span></span>
<span data-ttu-id="21d02-123">Key URI</span><span class="sxs-lookup"><span data-stu-id="21d02-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d02-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="21d02-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="21d02-125">Skapa krypterings omfång med Minin as Microsoft.-valv</span><span class="sxs-lookup"><span data-stu-id="21d02-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d02-126">-ResourceGroupName</span></span>
<span data-ttu-id="21d02-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="21d02-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="21d02-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21d02-128">-StorageAccount</span></span>
<span data-ttu-id="21d02-129">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="21d02-129">Storage account object</span></span>

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

### <span data-ttu-id="21d02-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21d02-130">-StorageAccountName</span></span>
<span data-ttu-id="21d02-131">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="21d02-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="21d02-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="21d02-132">-StorageEncryption</span></span>
<span data-ttu-id="21d02-133">Skapa krypterings omfång med Minin källkod som Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="21d02-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d02-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21d02-134">-Confirm</span></span>
<span data-ttu-id="21d02-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21d02-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21d02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d02-136">-WhatIf</span></span>
<span data-ttu-id="21d02-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21d02-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d02-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21d02-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21d02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d02-139">CommonParameters</span></span>
<span data-ttu-id="21d02-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d02-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d02-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d02-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21d02-142">INPUTS</span></span>

### <span data-ttu-id="21d02-143">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21d02-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="21d02-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21d02-144">OUTPUTS</span></span>

### <span data-ttu-id="21d02-145">Microsoft. Azure. commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="21d02-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="21d02-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21d02-146">NOTES</span></span>

## <span data-ttu-id="21d02-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21d02-147">RELATED LINKS</span></span>
