---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574293"
---
# <span data-ttu-id="bcf7a-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bcf7a-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="bcf7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcf7a-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf7a-103">Ändrar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcf7a-104">SYNTAX</span></span>

### <span data-ttu-id="bcf7a-105">SetByACLObject (standard)</span><span class="sxs-lookup"><span data-stu-id="bcf7a-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf7a-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="bcf7a-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf7a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcf7a-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf7a-108">Cmdleten **set-AzureRmDataLakeStoreItemAclEntry** ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bcf7a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcf7a-109">EXAMPLES</span></span>

### <span data-ttu-id="bcf7a-110">Exempel 1: ändra behörigheter för en ACE</span><span class="sxs-lookup"><span data-stu-id="bcf7a-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="bcf7a-111">Det här kommandot ändrar ess för Patti Nilsson till att ha alla behörigheter.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="bcf7a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcf7a-112">PARAMETERS</span></span>

### <span data-ttu-id="bcf7a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="bcf7a-113">-Account</span></span>
<span data-ttu-id="bcf7a-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="bcf7a-115">-AceType</span></span>
<span data-ttu-id="bcf7a-116">Anger den typ av ACE som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="bcf7a-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bcf7a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcf7a-118">Användarläge</span><span class="sxs-lookup"><span data-stu-id="bcf7a-118">User</span></span> 
- <span data-ttu-id="bcf7a-119">Mal</span><span class="sxs-lookup"><span data-stu-id="bcf7a-119">Group</span></span> 
- <span data-ttu-id="bcf7a-120">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="bcf7a-120">Mask</span></span> 
- <span data-ttu-id="bcf7a-121">Övrigt</span><span class="sxs-lookup"><span data-stu-id="bcf7a-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="bcf7a-122">-Acl</span></span>
<span data-ttu-id="bcf7a-123">Anger det ACL-objekt som innehåller de poster som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-124">-Standard</span><span class="sxs-lookup"><span data-stu-id="bcf7a-124">-Default</span></span>
<span data-ttu-id="bcf7a-125">Anger att den här åtgärden ändrar standard åtkomst kontroll för den angivna åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf7a-126">-DefaultProfile</span></span>
<span data-ttu-id="bcf7a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf7a-128">-ID</span><span class="sxs-lookup"><span data-stu-id="bcf7a-128">-Id</span></span>
<span data-ttu-id="bcf7a-129">Anger objekt-ID: t för den AzureActive katalog användare, grupp eller tjänstens huvud namn som en åtkomst kontroll ska ändras för.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcf7a-130">-PassThru</span></span>
<span data-ttu-id="bcf7a-131">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-132">-Path</span><span class="sxs-lookup"><span data-stu-id="bcf7a-132">-Path</span></span>
<span data-ttu-id="bcf7a-133">Anger den data Lake Store-sökvägen för det objekt som du vill ändra en ACE för, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="bcf7a-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-134">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="bcf7a-134">-Permissions</span></span>
<span data-ttu-id="bcf7a-135">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="bcf7a-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bcf7a-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcf7a-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="bcf7a-137">None</span></span>
- <span data-ttu-id="bcf7a-138">Genomför</span><span class="sxs-lookup"><span data-stu-id="bcf7a-138">Execute</span></span>
- <span data-ttu-id="bcf7a-139">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="bcf7a-139">Write</span></span>
- <span data-ttu-id="bcf7a-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="bcf7a-140">WriteExecute</span></span>
- <span data-ttu-id="bcf7a-141">Läst</span><span class="sxs-lookup"><span data-stu-id="bcf7a-141">Read</span></span>
- <span data-ttu-id="bcf7a-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="bcf7a-142">ReadExecute</span></span>
- <span data-ttu-id="bcf7a-143">Läs</span><span class="sxs-lookup"><span data-stu-id="bcf7a-143">ReadWrite</span></span>
- <span data-ttu-id="bcf7a-144">Alla</span><span class="sxs-lookup"><span data-stu-id="bcf7a-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bcf7a-145">-Confirm</span></span>
<span data-ttu-id="bcf7a-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf7a-147">-WhatIf</span></span>
<span data-ttu-id="bcf7a-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf7a-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf7a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf7a-150">CommonParameters</span></span>
<span data-ttu-id="bcf7a-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf7a-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf7a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf7a-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcf7a-153">INPUTS</span></span>

### <span data-ttu-id="bcf7a-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="bcf7a-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="bcf7a-155">Parametern ' ACL ' godkänner värdet av typen ' DataLakeStoreItemAce [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bcf7a-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="bcf7a-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcf7a-156">OUTPUTS</span></span>

### <span data-ttu-id="bcf7a-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="bcf7a-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="bcf7a-158">Om PassThru anges returnerar den resulterande listan med ACL-poster.</span><span class="sxs-lookup"><span data-stu-id="bcf7a-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="bcf7a-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcf7a-159">NOTES</span></span>

## <span data-ttu-id="bcf7a-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcf7a-160">RELATED LINKS</span></span>

[<span data-ttu-id="bcf7a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bcf7a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


