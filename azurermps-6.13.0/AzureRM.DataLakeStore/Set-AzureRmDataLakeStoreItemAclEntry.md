---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: acf0b53ba6ad03de117e9171ec64d30ee627a927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576315"
---
# <span data-ttu-id="e422b-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e422b-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="e422b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e422b-102">SYNOPSIS</span></span>
<span data-ttu-id="e422b-103">Ändrar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e422b-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e422b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e422b-104">SYNTAX</span></span>

### <span data-ttu-id="e422b-105">SetByACLObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e422b-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e422b-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="e422b-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse]
 [-Concurrency <Int32>] [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e422b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e422b-107">DESCRIPTION</span></span>
<span data-ttu-id="e422b-108">Cmdleten **set-AzureRmDataLakeStoreItemAclEntry** ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e422b-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e422b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e422b-109">EXAMPLES</span></span>

### <span data-ttu-id="e422b-110">Exempel 1: ändra behörigheter för en ACE</span><span class="sxs-lookup"><span data-stu-id="e422b-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="e422b-111">Det här kommandot ändrar ess för Patti Nilsson till att ha alla behörigheter.</span><span class="sxs-lookup"><span data-stu-id="e422b-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="e422b-112">Exempel 2: ändra behörigheter för en ACE rekursivt</span><span class="sxs-lookup"><span data-stu-id="e422b-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="e422b-113">Exempel 3: ändra behörigheter för en ACE rekursivt med ACL-objekt</span><span class="sxs-lookup"><span data-stu-id="e422b-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="e422b-114">Det här kommandot ändrar ACE för Patti Nilsson rekursivt för att ha alla behörigheter till rot och alla dess under kataloger och filer.</span><span class="sxs-lookup"><span data-stu-id="e422b-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="e422b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e422b-115">PARAMETERS</span></span>

### <span data-ttu-id="e422b-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="e422b-116">-Account</span></span>
<span data-ttu-id="e422b-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e422b-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e422b-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="e422b-118">-AceType</span></span>
<span data-ttu-id="e422b-119">Anger den typ av ACE som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e422b-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="e422b-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e422b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e422b-121">Användarläge</span><span class="sxs-lookup"><span data-stu-id="e422b-121">User</span></span> 
- <span data-ttu-id="e422b-122">Mal</span><span class="sxs-lookup"><span data-stu-id="e422b-122">Group</span></span> 
- <span data-ttu-id="e422b-123">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="e422b-123">Mask</span></span> 
- <span data-ttu-id="e422b-124">Övrigt</span><span class="sxs-lookup"><span data-stu-id="e422b-124">Other</span></span>

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

### <span data-ttu-id="e422b-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="e422b-125">-Acl</span></span>
<span data-ttu-id="e422b-126">Anger det ACL-objekt som innehåller de poster som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e422b-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="e422b-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="e422b-127">-Concurrency</span></span>
<span data-ttu-id="e422b-128">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="e422b-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="e422b-129">Valfritt: ett rimligt standardvärde väljs</span><span class="sxs-lookup"><span data-stu-id="e422b-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="e422b-130">-Standard</span><span class="sxs-lookup"><span data-stu-id="e422b-130">-Default</span></span>
<span data-ttu-id="e422b-131">Anger att den här åtgärden ändrar standard åtkomst kontroll för den angivna åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="e422b-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="e422b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e422b-132">-DefaultProfile</span></span>
<span data-ttu-id="e422b-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e422b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e422b-134">-ID</span><span class="sxs-lookup"><span data-stu-id="e422b-134">-Id</span></span>
<span data-ttu-id="e422b-135">Anger objekt-ID: t för den AzureActive katalog användare, grupp eller tjänstens huvud namn som en åtkomst kontroll ska ändras för.</span><span class="sxs-lookup"><span data-stu-id="e422b-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="e422b-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e422b-136">-PassThru</span></span>
<span data-ttu-id="e422b-137">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="e422b-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="e422b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="e422b-138">-Path</span></span>
<span data-ttu-id="e422b-139">Anger den data Lake Store-sökvägen för det objekt som du vill ändra en ACE för, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="e422b-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e422b-140">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="e422b-140">-Permissions</span></span>
<span data-ttu-id="e422b-141">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="e422b-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="e422b-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e422b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e422b-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="e422b-143">None</span></span>
- <span data-ttu-id="e422b-144">Genomför</span><span class="sxs-lookup"><span data-stu-id="e422b-144">Execute</span></span>
- <span data-ttu-id="e422b-145">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="e422b-145">Write</span></span>
- <span data-ttu-id="e422b-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="e422b-146">WriteExecute</span></span>
- <span data-ttu-id="e422b-147">Läst</span><span class="sxs-lookup"><span data-stu-id="e422b-147">Read</span></span>
- <span data-ttu-id="e422b-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="e422b-148">ReadExecute</span></span>
- <span data-ttu-id="e422b-149">Läs</span><span class="sxs-lookup"><span data-stu-id="e422b-149">ReadWrite</span></span>
- <span data-ttu-id="e422b-150">Alla</span><span class="sxs-lookup"><span data-stu-id="e422b-150">All</span></span>

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

### <span data-ttu-id="e422b-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e422b-151">-Recurse</span></span>
<span data-ttu-id="e422b-152">Anger den ACL som ska ändras rekursivt till underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="e422b-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="e422b-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="e422b-153">-ShowProgress</span></span>
<span data-ttu-id="e422b-154">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="e422b-154">If passed then progress status is showed.</span></span> <span data-ttu-id="e422b-155">Gäller endast när rekursiv ACL-ändring är klar.</span><span class="sxs-lookup"><span data-stu-id="e422b-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="e422b-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e422b-156">-Confirm</span></span>
<span data-ttu-id="e422b-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e422b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e422b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e422b-158">-WhatIf</span></span>
<span data-ttu-id="e422b-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e422b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e422b-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e422b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e422b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e422b-161">CommonParameters</span></span>
<span data-ttu-id="e422b-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e422b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e422b-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e422b-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e422b-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e422b-164">INPUTS</span></span>

### <span data-ttu-id="e422b-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e422b-165">System.String</span></span>

### <span data-ttu-id="e422b-166">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e422b-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e422b-167">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="e422b-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="e422b-168">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="e422b-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="e422b-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e422b-169">System.Guid</span></span>

### <span data-ttu-id="e422b-170">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + permission</span><span class="sxs-lookup"><span data-stu-id="e422b-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="e422b-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e422b-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e422b-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e422b-172">System.Int32</span></span>

## <span data-ttu-id="e422b-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e422b-173">OUTPUTS</span></span>

### <span data-ttu-id="e422b-174">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="e422b-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="e422b-175">Om PassThru anges returnerar den resulterande listan med ACL-poster.</span><span class="sxs-lookup"><span data-stu-id="e422b-175">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="e422b-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e422b-176">NOTES</span></span>

## <span data-ttu-id="e422b-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e422b-177">RELATED LINKS</span></span>

[<span data-ttu-id="e422b-178">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e422b-178">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


