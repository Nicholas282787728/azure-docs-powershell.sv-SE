---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754286"
---
# <span data-ttu-id="da9ef-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="da9ef-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="da9ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="da9ef-103">Tar bort en post från en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da9ef-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da9ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da9ef-104">SYNTAX</span></span>

### <span data-ttu-id="da9ef-105">RemoveByACLObject (standard)</span><span class="sxs-lookup"><span data-stu-id="da9ef-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da9ef-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="da9ef-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da9ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da9ef-107">DESCRIPTION</span></span>
<span data-ttu-id="da9ef-108">Cmdleten **Remove-AzDataLakeStoreItemAclEntry** tar bort en post (ACE) från åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da9ef-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da9ef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da9ef-109">EXAMPLES</span></span>

### <span data-ttu-id="da9ef-110">Exempel 1: ta bort en användar post</span><span class="sxs-lookup"><span data-stu-id="da9ef-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="da9ef-111">Det här kommandot tar bort användarens ACE för Patti Nilsson från ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="da9ef-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="da9ef-112">Exempel 2: ta bort en användar post rekursivt</span><span class="sxs-lookup"><span data-stu-id="da9ef-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="da9ef-113">Exempel 3: ta bort behörigheter för en ACE rekursivt med ACL-objekt</span><span class="sxs-lookup"><span data-stu-id="da9ef-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="da9ef-114">Det här kommandot tar bort användarens ACE för Patti Nilsson från roten och rekursivt från alla dess under kataloger och filer för konto ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="da9ef-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="da9ef-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da9ef-115">PARAMETERS</span></span>

### <span data-ttu-id="da9ef-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="da9ef-116">-Account</span></span>
<span data-ttu-id="da9ef-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="da9ef-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="da9ef-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="da9ef-118">-AceType</span></span>
<span data-ttu-id="da9ef-119">Anger den typ av ACE som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="da9ef-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="da9ef-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="da9ef-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da9ef-121">Användarläge</span><span class="sxs-lookup"><span data-stu-id="da9ef-121">User</span></span>
- <span data-ttu-id="da9ef-122">Mal</span><span class="sxs-lookup"><span data-stu-id="da9ef-122">Group</span></span>
- <span data-ttu-id="da9ef-123">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="da9ef-123">Mask</span></span>
- <span data-ttu-id="da9ef-124">Övrigt</span><span class="sxs-lookup"><span data-stu-id="da9ef-124">Other</span></span>

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

### <span data-ttu-id="da9ef-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="da9ef-125">-Acl</span></span>
<span data-ttu-id="da9ef-126">Anger det ACL-objekt som innehåller de poster som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="da9ef-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="da9ef-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="da9ef-127">-Concurrency</span></span>
<span data-ttu-id="da9ef-128">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="da9ef-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="da9ef-129">Valfritt: ett rimligt standardvärde väljs</span><span class="sxs-lookup"><span data-stu-id="da9ef-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="da9ef-130">-Standard</span><span class="sxs-lookup"><span data-stu-id="da9ef-130">-Default</span></span>
<span data-ttu-id="da9ef-131">Anger att den här åtgärden tar bort standard åtkomst posten från angiven ACL.</span><span class="sxs-lookup"><span data-stu-id="da9ef-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="da9ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9ef-132">-DefaultProfile</span></span>
<span data-ttu-id="da9ef-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da9ef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da9ef-134">-ID</span><span class="sxs-lookup"><span data-stu-id="da9ef-134">-Id</span></span>
<span data-ttu-id="da9ef-135">Anger objekt-ID: t för den AzureActive-katalog användare, grupp eller tjänst som en åtkomst kontroll ska tas bort för.</span><span class="sxs-lookup"><span data-stu-id="da9ef-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="da9ef-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da9ef-136">-PassThru</span></span>
<span data-ttu-id="da9ef-137">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="da9ef-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="da9ef-138">-Path</span><span class="sxs-lookup"><span data-stu-id="da9ef-138">-Path</span></span>
<span data-ttu-id="da9ef-139">Anger den data Lake Store-sökvägen för det objekt som du vill ta bort en ACE från och börja med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="da9ef-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="da9ef-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="da9ef-140">-Recurse</span></span>
<span data-ttu-id="da9ef-141">Anger att ACL ska tas bort rekursivt för underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="da9ef-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="da9ef-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="da9ef-142">-ShowProgress</span></span>
<span data-ttu-id="da9ef-143">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="da9ef-143">If passed then progress status is showed.</span></span> <span data-ttu-id="da9ef-144">Gäller endast när rekursiv ACL Remove är klar.</span><span class="sxs-lookup"><span data-stu-id="da9ef-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="da9ef-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da9ef-145">-Confirm</span></span>
<span data-ttu-id="da9ef-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da9ef-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da9ef-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da9ef-147">-WhatIf</span></span>
<span data-ttu-id="da9ef-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da9ef-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da9ef-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da9ef-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da9ef-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9ef-150">CommonParameters</span></span>
<span data-ttu-id="da9ef-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9ef-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9ef-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9ef-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9ef-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da9ef-153">INPUTS</span></span>

### <span data-ttu-id="da9ef-154">System. String</span><span class="sxs-lookup"><span data-stu-id="da9ef-154">System.String</span></span>

### <span data-ttu-id="da9ef-155">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="da9ef-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="da9ef-156">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="da9ef-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="da9ef-157">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="da9ef-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="da9ef-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="da9ef-158">System.Guid</span></span>

### <span data-ttu-id="da9ef-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da9ef-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="da9ef-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da9ef-160">System.Int32</span></span>

## <span data-ttu-id="da9ef-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da9ef-161">OUTPUTS</span></span>

### <span data-ttu-id="da9ef-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da9ef-162">System.Boolean</span></span>

## <span data-ttu-id="da9ef-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da9ef-163">NOTES</span></span>

## <span data-ttu-id="da9ef-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da9ef-164">RELATED LINKS</span></span>

[<span data-ttu-id="da9ef-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="da9ef-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)

