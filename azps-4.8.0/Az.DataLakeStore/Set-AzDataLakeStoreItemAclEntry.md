---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260786"
---
# <span data-ttu-id="1dd47-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1dd47-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="1dd47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dd47-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd47-103">Ändrar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1dd47-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1dd47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dd47-104">SYNTAX</span></span>

### <span data-ttu-id="1dd47-105">SetByACLObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1dd47-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd47-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="1dd47-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd47-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dd47-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd47-108">Cmdleten **set-AzDataLakeStoreItemAclEntry** ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1dd47-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1dd47-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dd47-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd47-110">Exempel 1: ändra behörigheter för en ACE</span><span class="sxs-lookup"><span data-stu-id="1dd47-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="1dd47-111">Det här kommandot ändrar ess för Patti Nilsson till att ha alla behörigheter.</span><span class="sxs-lookup"><span data-stu-id="1dd47-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="1dd47-112">Exempel 2: ändra behörigheter för en ACE rekursivt</span><span class="sxs-lookup"><span data-stu-id="1dd47-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="1dd47-113">Exempel 3: ändra behörigheter för en ACE rekursivt med ACL-objekt</span><span class="sxs-lookup"><span data-stu-id="1dd47-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="1dd47-114">Det här kommandot ändrar ACE för Patti Nilsson rekursivt för att ha alla behörigheter till rot och alla dess under kataloger och filer.</span><span class="sxs-lookup"><span data-stu-id="1dd47-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="1dd47-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dd47-115">PARAMETERS</span></span>

### <span data-ttu-id="1dd47-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="1dd47-116">-Account</span></span>
<span data-ttu-id="1dd47-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="1dd47-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1dd47-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="1dd47-118">-AceType</span></span>
<span data-ttu-id="1dd47-119">Anger den typ av ACE som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="1dd47-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="1dd47-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1dd47-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1dd47-121">Användarläge</span><span class="sxs-lookup"><span data-stu-id="1dd47-121">User</span></span> 
- <span data-ttu-id="1dd47-122">Mal</span><span class="sxs-lookup"><span data-stu-id="1dd47-122">Group</span></span> 
- <span data-ttu-id="1dd47-123">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="1dd47-123">Mask</span></span> 
- <span data-ttu-id="1dd47-124">Övrigt</span><span class="sxs-lookup"><span data-stu-id="1dd47-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd47-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="1dd47-125">-Acl</span></span>
<span data-ttu-id="1dd47-126">Anger det ACL-objekt som innehåller de poster som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="1dd47-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd47-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="1dd47-127">-Concurrency</span></span>
<span data-ttu-id="1dd47-128">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="1dd47-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="1dd47-129">Valfritt: ett rimligt standardvärde väljs</span><span class="sxs-lookup"><span data-stu-id="1dd47-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="1dd47-130">-Standard</span><span class="sxs-lookup"><span data-stu-id="1dd47-130">-Default</span></span>
<span data-ttu-id="1dd47-131">Anger att den här åtgärden ändrar standard åtkomst kontroll för den angivna åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="1dd47-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd47-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd47-132">-DefaultProfile</span></span>
<span data-ttu-id="1dd47-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd47-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dd47-134">-ID</span><span class="sxs-lookup"><span data-stu-id="1dd47-134">-Id</span></span>
<span data-ttu-id="1dd47-135">Anger objekt-ID: t för den AzureActive katalog användare, grupp eller tjänstens huvud namn som en åtkomst kontroll ska ändras för.</span><span class="sxs-lookup"><span data-stu-id="1dd47-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd47-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dd47-136">-PassThru</span></span>
<span data-ttu-id="1dd47-137">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="1dd47-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="1dd47-138">-Path</span><span class="sxs-lookup"><span data-stu-id="1dd47-138">-Path</span></span>
<span data-ttu-id="1dd47-139">Anger den data Lake Store-sökvägen för det objekt som du vill ändra en ACE för, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="1dd47-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1dd47-140">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="1dd47-140">-Permissions</span></span>
<span data-ttu-id="1dd47-141">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="1dd47-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="1dd47-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1dd47-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1dd47-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="1dd47-143">None</span></span>
- <span data-ttu-id="1dd47-144">Genomför</span><span class="sxs-lookup"><span data-stu-id="1dd47-144">Execute</span></span>
- <span data-ttu-id="1dd47-145">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="1dd47-145">Write</span></span>
- <span data-ttu-id="1dd47-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="1dd47-146">WriteExecute</span></span>
- <span data-ttu-id="1dd47-147">Läst</span><span class="sxs-lookup"><span data-stu-id="1dd47-147">Read</span></span>
- <span data-ttu-id="1dd47-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="1dd47-148">ReadExecute</span></span>
- <span data-ttu-id="1dd47-149">Läs</span><span class="sxs-lookup"><span data-stu-id="1dd47-149">ReadWrite</span></span>
- <span data-ttu-id="1dd47-150">Alla</span><span class="sxs-lookup"><span data-stu-id="1dd47-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd47-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="1dd47-151">-Recurse</span></span>
<span data-ttu-id="1dd47-152">Anger den ACL som ska ändras rekursivt till underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="1dd47-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="1dd47-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="1dd47-153">-ShowProgress</span></span>
<span data-ttu-id="1dd47-154">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="1dd47-154">If passed then progress status is showed.</span></span> <span data-ttu-id="1dd47-155">Gäller endast när rekursiv ACL-ändring är klar.</span><span class="sxs-lookup"><span data-stu-id="1dd47-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="1dd47-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dd47-156">-Confirm</span></span>
<span data-ttu-id="1dd47-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dd47-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd47-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd47-158">-WhatIf</span></span>
<span data-ttu-id="1dd47-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dd47-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd47-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dd47-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd47-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd47-161">CommonParameters</span></span>
<span data-ttu-id="1dd47-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd47-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd47-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd47-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd47-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dd47-164">INPUTS</span></span>

### <span data-ttu-id="1dd47-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd47-165">System.String</span></span>

### <span data-ttu-id="1dd47-166">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1dd47-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1dd47-167">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="1dd47-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="1dd47-168">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="1dd47-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="1dd47-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1dd47-169">System.Guid</span></span>

### <span data-ttu-id="1dd47-170">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + permission</span><span class="sxs-lookup"><span data-stu-id="1dd47-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="1dd47-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1dd47-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1dd47-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1dd47-172">System.Int32</span></span>

## <span data-ttu-id="1dd47-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dd47-173">OUTPUTS</span></span>

### <span data-ttu-id="1dd47-174">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="1dd47-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="1dd47-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dd47-175">NOTES</span></span>

## <span data-ttu-id="1dd47-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dd47-176">RELATED LINKS</span></span>

[<span data-ttu-id="1dd47-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1dd47-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

