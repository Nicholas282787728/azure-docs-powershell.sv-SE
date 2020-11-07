---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 343823960e63276da66c522af91ebeb7b6f6044e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743881"
---
# <span data-ttu-id="c65fd-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c65fd-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c65fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c65fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c65fd-103">Återställer ett hanterat lagrings konto i ett nyckeltal från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="c65fd-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="c65fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c65fd-104">SYNTAX</span></span>

### <span data-ttu-id="c65fd-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="c65fd-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c65fd-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65fd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c65fd-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65fd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c65fd-108">DESCRIPTION</span></span>
<span data-ttu-id="c65fd-109">Cmdleten **restore-AzKeyVaultManagedStorageAccount** skapar ett hanterat lagrings konto i det angivna nyckelvärdet från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="c65fd-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="c65fd-110">Det här hanterade lagrings kontot är en replik av det säkerhetskopierade hanterade lagrings kontot i indatafilen och har samma namn som det ursprungliga.</span><span class="sxs-lookup"><span data-stu-id="c65fd-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="c65fd-111">Om det redan finns ett hanterat lagrings konto med samma namn i huvud valvet Miss lyckas denna cmdlet i stället för att skriva över originalet.</span><span class="sxs-lookup"><span data-stu-id="c65fd-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="c65fd-112">Huvud valvet som du återställer det hanterade lagrings kontot till kan skilja sig från det viktiga valv som du säkerhetskopierade det hanterade lagrings kontot från.</span><span class="sxs-lookup"><span data-stu-id="c65fd-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="c65fd-113">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="c65fd-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="c65fd-114">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="c65fd-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="c65fd-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c65fd-115">EXAMPLES</span></span>

### <span data-ttu-id="c65fd-116">Exempel 1: återställa ett säkerhetskopierat lagrings konto som hanteras</span><span class="sxs-lookup"><span data-stu-id="c65fd-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
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

<span data-ttu-id="c65fd-117">Det här kommandot återställer ett hanterat lagrings konto, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="c65fd-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="c65fd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c65fd-118">PARAMETERS</span></span>

### <span data-ttu-id="c65fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65fd-119">-DefaultProfile</span></span>
<span data-ttu-id="c65fd-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c65fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65fd-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c65fd-121">-InputFile</span></span>
<span data-ttu-id="c65fd-122">Indatafil.</span><span class="sxs-lookup"><span data-stu-id="c65fd-122">Input file.</span></span>
<span data-ttu-id="c65fd-123">Den indatafil som innehåller den säkerhetskopierade blobben</span><span class="sxs-lookup"><span data-stu-id="c65fd-123">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65fd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65fd-124">-InputObject</span></span>
<span data-ttu-id="c65fd-125">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="c65fd-125">KeyVault object</span></span>

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

### <span data-ttu-id="c65fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c65fd-126">-ResourceId</span></span>
<span data-ttu-id="c65fd-127">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="c65fd-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="c65fd-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c65fd-128">-VaultName</span></span>
<span data-ttu-id="c65fd-129">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="c65fd-129">Vault name.</span></span>
<span data-ttu-id="c65fd-130">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="c65fd-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65fd-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c65fd-131">-Confirm</span></span>
<span data-ttu-id="c65fd-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c65fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65fd-133">-WhatIf</span></span>
<span data-ttu-id="c65fd-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c65fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65fd-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c65fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65fd-136">CommonParameters</span></span>
<span data-ttu-id="c65fd-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65fd-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65fd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65fd-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c65fd-139">INPUTS</span></span>

### <span data-ttu-id="c65fd-140">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c65fd-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c65fd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c65fd-141">System.String</span></span>

## <span data-ttu-id="c65fd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c65fd-142">OUTPUTS</span></span>

### <span data-ttu-id="c65fd-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c65fd-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c65fd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c65fd-144">NOTES</span></span>

## <span data-ttu-id="c65fd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c65fd-145">RELATED LINKS</span></span>