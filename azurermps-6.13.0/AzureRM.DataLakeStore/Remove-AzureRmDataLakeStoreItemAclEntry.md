---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572792"
---
# <span data-ttu-id="54555-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="54555-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="54555-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54555-102">SYNOPSIS</span></span>
<span data-ttu-id="54555-103">Tar bort en post från en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="54555-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54555-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54555-104">SYNTAX</span></span>

### <span data-ttu-id="54555-105">RemoveByACLObject (standard)</span><span class="sxs-lookup"><span data-stu-id="54555-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54555-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="54555-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54555-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54555-107">DESCRIPTION</span></span>
<span data-ttu-id="54555-108">Cmdleten **Remove-AzureRmDataLakeStoreItemAclEntry** tar bort en post (ACE) från åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="54555-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="54555-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54555-109">EXAMPLES</span></span>

### <span data-ttu-id="54555-110">Exempel 1: ta bort en användar post</span><span class="sxs-lookup"><span data-stu-id="54555-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="54555-111">Det här kommandot tar bort användarens ACE för Patti Nilsson från ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="54555-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="54555-112">Exempel 2: ta bort en användar post rekursivt</span><span class="sxs-lookup"><span data-stu-id="54555-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="54555-113">Exempel 3: ta bort behörigheter för en ACE rekursivt med ACL-objekt</span><span class="sxs-lookup"><span data-stu-id="54555-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="54555-114">Det här kommandot tar bort användarens ACE för Patti Nilsson från roten och rekursivt från alla dess under kataloger och filer för konto ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="54555-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="54555-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54555-115">PARAMETERS</span></span>

### <span data-ttu-id="54555-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="54555-116">-Account</span></span>
<span data-ttu-id="54555-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="54555-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="54555-118">-AceType</span></span>
<span data-ttu-id="54555-119">Anger den typ av ACE som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="54555-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="54555-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="54555-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54555-121">Användarläge</span><span class="sxs-lookup"><span data-stu-id="54555-121">User</span></span>
- <span data-ttu-id="54555-122">Mal</span><span class="sxs-lookup"><span data-stu-id="54555-122">Group</span></span>
- <span data-ttu-id="54555-123">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="54555-123">Mask</span></span>
- <span data-ttu-id="54555-124">Övrigt</span><span class="sxs-lookup"><span data-stu-id="54555-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="54555-125">-Acl</span></span>
<span data-ttu-id="54555-126">Anger det ACL-objekt som innehåller de poster som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="54555-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="54555-127">-Concurrency</span></span>
<span data-ttu-id="54555-128">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="54555-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="54555-129">Valfritt: ett rimligt standardvärde väljs</span><span class="sxs-lookup"><span data-stu-id="54555-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-130">-Standard</span><span class="sxs-lookup"><span data-stu-id="54555-130">-Default</span></span>
<span data-ttu-id="54555-131">Anger att den här åtgärden tar bort standard åtkomst posten från angiven ACL.</span><span class="sxs-lookup"><span data-stu-id="54555-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54555-132">-DefaultProfile</span></span>
<span data-ttu-id="54555-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54555-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54555-134">-ID</span><span class="sxs-lookup"><span data-stu-id="54555-134">-Id</span></span>
<span data-ttu-id="54555-135">Anger objekt-ID: t för den AzureActive-katalog användare, grupp eller tjänst som en åtkomst kontroll ska tas bort för.</span><span class="sxs-lookup"><span data-stu-id="54555-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54555-136">-PassThru</span></span>
<span data-ttu-id="54555-137">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="54555-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-138">-Path</span><span class="sxs-lookup"><span data-stu-id="54555-138">-Path</span></span>
<span data-ttu-id="54555-139">Anger den data Lake Store-sökvägen för det objekt som du vill ta bort en ACE från och börja med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="54555-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="54555-140">-Recurse</span></span>
<span data-ttu-id="54555-141">Anger att ACL ska tas bort rekursivt för underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="54555-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54555-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="54555-142">-ShowProgress</span></span>
<span data-ttu-id="54555-143">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="54555-143">If passed then progress status is showed.</span></span> <span data-ttu-id="54555-144">Gäller endast när rekursiv ACL Remove är klar.</span><span class="sxs-lookup"><span data-stu-id="54555-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="54555-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54555-145">-Confirm</span></span>
<span data-ttu-id="54555-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54555-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54555-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54555-147">-WhatIf</span></span>
<span data-ttu-id="54555-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54555-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54555-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54555-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54555-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54555-150">CommonParameters</span></span>
<span data-ttu-id="54555-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54555-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54555-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54555-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54555-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54555-153">INPUTS</span></span>

### <span data-ttu-id="54555-154">System. String</span><span class="sxs-lookup"><span data-stu-id="54555-154">System.String</span></span>

### <span data-ttu-id="54555-155">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="54555-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="54555-156">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="54555-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="54555-157">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="54555-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="54555-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="54555-158">System.Guid</span></span>

### <span data-ttu-id="54555-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54555-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="54555-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="54555-160">System.Int32</span></span>

## <span data-ttu-id="54555-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54555-161">OUTPUTS</span></span>

### <span data-ttu-id="54555-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54555-162">System.Boolean</span></span>

## <span data-ttu-id="54555-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54555-163">NOTES</span></span>

## <span data-ttu-id="54555-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54555-164">RELATED LINKS</span></span>

[<span data-ttu-id="54555-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="54555-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


