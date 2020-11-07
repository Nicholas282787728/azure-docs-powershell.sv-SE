---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756973"
---
# <span data-ttu-id="81fd7-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="81fd7-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="81fd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="81fd7-103">Tar bort en post från en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81fd7-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81fd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81fd7-104">SYNTAX</span></span>

### <span data-ttu-id="81fd7-105">Ta bort ACL-poster med ACL-objekt (standard)</span><span class="sxs-lookup"><span data-stu-id="81fd7-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81fd7-106">Ta bort specifik ACE</span><span class="sxs-lookup"><span data-stu-id="81fd7-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81fd7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81fd7-107">DESCRIPTION</span></span>
<span data-ttu-id="81fd7-108">Cmdleten **Remove-AzureRmDataLakeStoreItemAclEntry** tar bort en post (ACE) från åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81fd7-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="81fd7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81fd7-109">EXAMPLES</span></span>

### <span data-ttu-id="81fd7-110">Exempel 1: ta bort en användar post</span><span class="sxs-lookup"><span data-stu-id="81fd7-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="81fd7-111">Det här kommandot tar bort användarens ACE för Patti Nilsson från ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="81fd7-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="81fd7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81fd7-112">PARAMETERS</span></span>

### <span data-ttu-id="81fd7-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="81fd7-113">-Account</span></span>
<span data-ttu-id="81fd7-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="81fd7-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="81fd7-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="81fd7-115">-AceType</span></span>
<span data-ttu-id="81fd7-116">Anger den typ av ACE som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="81fd7-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="81fd7-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="81fd7-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81fd7-118">Användarläge</span><span class="sxs-lookup"><span data-stu-id="81fd7-118">User</span></span>
- <span data-ttu-id="81fd7-119">Mal</span><span class="sxs-lookup"><span data-stu-id="81fd7-119">Group</span></span>
- <span data-ttu-id="81fd7-120">Urklippsmasker</span><span class="sxs-lookup"><span data-stu-id="81fd7-120">Mask</span></span>
- <span data-ttu-id="81fd7-121">Övrigt</span><span class="sxs-lookup"><span data-stu-id="81fd7-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81fd7-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="81fd7-122">-Acl</span></span>
<span data-ttu-id="81fd7-123">Anger det ACL-objekt som innehåller de poster som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="81fd7-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81fd7-124">-Standard</span><span class="sxs-lookup"><span data-stu-id="81fd7-124">-Default</span></span>
<span data-ttu-id="81fd7-125">Anger att den här åtgärden tar bort standard åtkomst posten från angiven ACL.</span><span class="sxs-lookup"><span data-stu-id="81fd7-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81fd7-126">-ID</span><span class="sxs-lookup"><span data-stu-id="81fd7-126">-Id</span></span>
<span data-ttu-id="81fd7-127">Anger objekt-ID: t för den AzureActive-katalog användare, grupp eller tjänst som en åtkomst kontroll ska tas bort för.</span><span class="sxs-lookup"><span data-stu-id="81fd7-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81fd7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81fd7-128">-PassThru</span></span>
<span data-ttu-id="81fd7-129">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="81fd7-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="81fd7-130">-Path</span><span class="sxs-lookup"><span data-stu-id="81fd7-130">-Path</span></span>
<span data-ttu-id="81fd7-131">Anger den data Lake Store-sökvägen för det objekt som du vill ta bort en ACE från och börja med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="81fd7-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="81fd7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81fd7-132">-Confirm</span></span>
<span data-ttu-id="81fd7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81fd7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81fd7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81fd7-134">-WhatIf</span></span>
<span data-ttu-id="81fd7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81fd7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81fd7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81fd7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81fd7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fd7-137">-DefaultProfile</span></span>
<span data-ttu-id="81fd7-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81fd7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81fd7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fd7-139">CommonParameters</span></span>
<span data-ttu-id="81fd7-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fd7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fd7-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81fd7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fd7-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81fd7-142">INPUTS</span></span>

### <span data-ttu-id="81fd7-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="81fd7-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="81fd7-144">Parametern ' ACL ' godkänner värdet av typen ' DataLakeStoreItemAce [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="81fd7-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="81fd7-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81fd7-145">OUTPUTS</span></span>

### <span data-ttu-id="81fd7-146">bool</span><span class="sxs-lookup"><span data-stu-id="81fd7-146">bool</span></span>
<span data-ttu-id="81fd7-147">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="81fd7-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="81fd7-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81fd7-148">NOTES</span></span>

## <span data-ttu-id="81fd7-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81fd7-149">RELATED LINKS</span></span>

[<span data-ttu-id="81fd7-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="81fd7-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


