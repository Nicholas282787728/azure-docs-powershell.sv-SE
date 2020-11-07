---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916842"
---
# <span data-ttu-id="eef92-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="eef92-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="eef92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eef92-102">SYNOPSIS</span></span>
<span data-ttu-id="eef92-103">Ändrar åtkomst kontroll för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eef92-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="eef92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eef92-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eef92-105">DESCRIPTION</span></span>
<span data-ttu-id="eef92-106">Cmdleten **set-AzDataLakeStoreItemAcl** ändrar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eef92-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="eef92-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eef92-107">EXAMPLES</span></span>

### <span data-ttu-id="eef92-108">Exempel 1: ange ACL för en fil och en mapp</span><span class="sxs-lookup"><span data-stu-id="eef92-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="eef92-109">Det första kommandot får ACL för rot katalogen för ContosoADL-kontot och lagrar den sedan i $ACL variabel.</span><span class="sxs-lookup"><span data-stu-id="eef92-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="eef92-110">Med det andra kommandot anges åtkomst kontrol listan för filen Test.txt till den i $ACL.</span><span class="sxs-lookup"><span data-stu-id="eef92-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="eef92-111">Exempel 2: ange ACL för mappen rekursivt</span><span class="sxs-lookup"><span data-stu-id="eef92-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="eef92-112">Det första kommandot får ACL: en för katalog-Mapp1 för ContosoADL-kontot och lagrar det sedan i $ACL variabel.</span><span class="sxs-lookup"><span data-stu-id="eef92-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="eef92-113">Det andra kommandot ställer in ACL rekursivt på till och med dess under kataloger och filer i $ACL.</span><span class="sxs-lookup"><span data-stu-id="eef92-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="eef92-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eef92-114">PARAMETERS</span></span>

### <span data-ttu-id="eef92-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="eef92-115">-Account</span></span>
<span data-ttu-id="eef92-116">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="eef92-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="eef92-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="eef92-117">-Acl</span></span>
<span data-ttu-id="eef92-118">Anger en ACL för en fil eller en mapp.</span><span class="sxs-lookup"><span data-stu-id="eef92-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eef92-119">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="eef92-119">-Concurrency</span></span>
<span data-ttu-id="eef92-120">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="eef92-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="eef92-121">Valfritt: ett rimligt standardvärde väljas.</span><span class="sxs-lookup"><span data-stu-id="eef92-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="eef92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef92-122">-DefaultProfile</span></span>
<span data-ttu-id="eef92-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eef92-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef92-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eef92-124">-PassThru</span></span>
<span data-ttu-id="eef92-125">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="eef92-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="eef92-126">-Path</span><span class="sxs-lookup"><span data-stu-id="eef92-126">-Path</span></span>
<span data-ttu-id="eef92-127">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="eef92-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="eef92-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="eef92-128">-Recurse</span></span>
<span data-ttu-id="eef92-129">Anger den ACL som ska anges rekursivt för underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="eef92-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="eef92-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="eef92-130">-ShowProgress</span></span>
<span data-ttu-id="eef92-131">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="eef92-131">If passed then progress status is showed.</span></span> <span data-ttu-id="eef92-132">Gäller endast när rekursiv ACL-uppsättning är klar.</span><span class="sxs-lookup"><span data-stu-id="eef92-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="eef92-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eef92-133">-Confirm</span></span>
<span data-ttu-id="eef92-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eef92-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef92-135">-WhatIf</span></span>
<span data-ttu-id="eef92-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eef92-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eef92-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eef92-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef92-138">CommonParameters</span></span>
<span data-ttu-id="eef92-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef92-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef92-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef92-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eef92-141">INPUTS</span></span>

### <span data-ttu-id="eef92-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eef92-142">System.String</span></span>

### <span data-ttu-id="eef92-143">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="eef92-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="eef92-144">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="eef92-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="eef92-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eef92-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="eef92-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="eef92-146">System.Int32</span></span>

## <span data-ttu-id="eef92-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eef92-147">OUTPUTS</span></span>

### <span data-ttu-id="eef92-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="eef92-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="eef92-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eef92-149">NOTES</span></span>

## <span data-ttu-id="eef92-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eef92-150">RELATED LINKS</span></span>
