---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584759"
---
# <span data-ttu-id="ec3e3-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ec3e3-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ec3e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3e3-103">Ändrar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec3e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec3e3-104">SYNTAX</span></span>

### <span data-ttu-id="ec3e3-105">Ange ACL-poster med ACL-objekt (standard)</span><span class="sxs-lookup"><span data-stu-id="ec3e3-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec3e3-106">Ange specifik ACE</span><span class="sxs-lookup"><span data-stu-id="ec3e3-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec3e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec3e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ec3e3-108">Cmdleten **set-AzureRmDataLakeStoreItemAclEntry** ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ec3e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec3e3-109">EXAMPLES</span></span>

### <span data-ttu-id="ec3e3-110">Exempel 1: ändra behörigheter för en ACE</span><span class="sxs-lookup"><span data-stu-id="ec3e3-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="ec3e3-111">Det här kommandot ändrar ess för Patti Nilsson till att ha alla behörigheter.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="ec3e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec3e3-112">PARAMETERS</span></span>

### <span data-ttu-id="ec3e3-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="ec3e3-113">-Account</span></span>
<span data-ttu-id="ec3e3-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ec3e3-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="ec3e3-115">-AceType</span></span>
<span data-ttu-id="ec3e3-116">Anger den typ av ACE som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="ec3e3-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ec3e3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec3e3-118">Användarläge</span><span class="sxs-lookup"><span data-stu-id="ec3e3-118">User</span></span> 
- <span data-ttu-id="ec3e3-119">Mal</span><span class="sxs-lookup"><span data-stu-id="ec3e3-119">Group</span></span> 
- <span data-ttu-id="ec3e3-120">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="ec3e3-120">Mask</span></span> 
- <span data-ttu-id="ec3e3-121">Övrigt</span><span class="sxs-lookup"><span data-stu-id="ec3e3-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e3-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="ec3e3-122">-Acl</span></span>
<span data-ttu-id="ec3e3-123">Anger det ACL-objekt som innehåller de poster som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e3-124">-Standard</span><span class="sxs-lookup"><span data-stu-id="ec3e3-124">-Default</span></span>
<span data-ttu-id="ec3e3-125">Anger att den här åtgärden ändrar standard åtkomst kontroll för den angivna åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e3-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ec3e3-126">-Id</span></span>
<span data-ttu-id="ec3e3-127">Anger objekt-ID: t för den AzureActive katalog användare, grupp eller tjänstens huvud namn som en åtkomst kontroll ska ändras för.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec3e3-128">-PassThru</span></span>
<span data-ttu-id="ec3e3-129">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="ec3e3-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ec3e3-130">-Path</span></span>
<span data-ttu-id="ec3e3-131">Anger den data Lake Store-sökvägen för det objekt som du vill ändra en ACE för, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="ec3e3-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ec3e3-132">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="ec3e3-132">-Permissions</span></span>
<span data-ttu-id="ec3e3-133">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="ec3e3-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ec3e3-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec3e3-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="ec3e3-135">None</span></span>
- <span data-ttu-id="ec3e3-136">Genomför</span><span class="sxs-lookup"><span data-stu-id="ec3e3-136">Execute</span></span>
- <span data-ttu-id="ec3e3-137">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="ec3e3-137">Write</span></span>
- <span data-ttu-id="ec3e3-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="ec3e3-138">WriteExecute</span></span>
- <span data-ttu-id="ec3e3-139">Läst</span><span class="sxs-lookup"><span data-stu-id="ec3e3-139">Read</span></span>
- <span data-ttu-id="ec3e3-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="ec3e3-140">ReadExecute</span></span>
- <span data-ttu-id="ec3e3-141">Läs</span><span class="sxs-lookup"><span data-stu-id="ec3e3-141">ReadWrite</span></span>
- <span data-ttu-id="ec3e3-142">Alla</span><span class="sxs-lookup"><span data-stu-id="ec3e3-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e3-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec3e3-143">-Confirm</span></span>
<span data-ttu-id="ec3e3-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec3e3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec3e3-145">-WhatIf</span></span>
<span data-ttu-id="ec3e3-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec3e3-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec3e3-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3e3-148">-DefaultProfile</span></span>
<span data-ttu-id="ec3e3-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec3e3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3e3-150">CommonParameters</span></span>
<span data-ttu-id="ec3e3-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3e3-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec3e3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3e3-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec3e3-153">INPUTS</span></span>

### <span data-ttu-id="ec3e3-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="ec3e3-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="ec3e3-155">Parametern ' ACL ' godkänner värdet av typen ' DataLakeStoreItemAce [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ec3e3-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="ec3e3-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec3e3-156">OUTPUTS</span></span>

### <span data-ttu-id="ec3e3-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="ec3e3-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="ec3e3-158">Om PassThru anges returnerar den resulterande listan med ACL-poster.</span><span class="sxs-lookup"><span data-stu-id="ec3e3-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="ec3e3-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec3e3-159">NOTES</span></span>

## <span data-ttu-id="ec3e3-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec3e3-160">RELATED LINKS</span></span>

[<span data-ttu-id="ec3e3-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ec3e3-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


