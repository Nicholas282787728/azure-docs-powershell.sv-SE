---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 45bf9fe3fb57eb6e627f1b2c7bc3e9146ccfd444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577048"
---
# <span data-ttu-id="0137b-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0137b-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="0137b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0137b-102">SYNOPSIS</span></span>
<span data-ttu-id="0137b-103">Ändrar åtkomst kontroll för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0137b-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0137b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0137b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0137b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0137b-105">DESCRIPTION</span></span>
<span data-ttu-id="0137b-106">Cmdleten **set-AzureRmDataLakeStoreItemAcl** ändrar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0137b-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0137b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0137b-107">EXAMPLES</span></span>

### <span data-ttu-id="0137b-108">Exempel 1: ange ACL för en fil och en mapp</span><span class="sxs-lookup"><span data-stu-id="0137b-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="0137b-109">Det första kommandot får ACL för rot katalogen för ContosoADL-kontot och lagrar den sedan i $ACL variabel.</span><span class="sxs-lookup"><span data-stu-id="0137b-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="0137b-110">Med det andra kommandot anges åtkomst kontrol listan för filen Test.txt till den i $ACL.</span><span class="sxs-lookup"><span data-stu-id="0137b-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="0137b-111">Exempel 2: ange ACL för mappen rekursivt</span><span class="sxs-lookup"><span data-stu-id="0137b-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="0137b-112">Det första kommandot får ACL: en för katalog-Mapp1 för ContosoADL-kontot och lagrar det sedan i $ACL variabel.</span><span class="sxs-lookup"><span data-stu-id="0137b-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="0137b-113">Det andra kommandot ställer in ACL rekursivt på till och med dess under kataloger och filer i $ACL.</span><span class="sxs-lookup"><span data-stu-id="0137b-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="0137b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0137b-114">PARAMETERS</span></span>

### <span data-ttu-id="0137b-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="0137b-115">-Account</span></span>
<span data-ttu-id="0137b-116">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="0137b-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0137b-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="0137b-117">-Acl</span></span>
<span data-ttu-id="0137b-118">Anger en ACL för en fil eller en mapp.</span><span class="sxs-lookup"><span data-stu-id="0137b-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="0137b-119">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="0137b-119">-Concurrency</span></span>
<span data-ttu-id="0137b-120">Antal filer/kataloger som bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="0137b-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="0137b-121">Valfritt: ett rimligt standardvärde väljas.</span><span class="sxs-lookup"><span data-stu-id="0137b-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="0137b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0137b-122">-DefaultProfile</span></span>
<span data-ttu-id="0137b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0137b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0137b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0137b-124">-PassThru</span></span>
<span data-ttu-id="0137b-125">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="0137b-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="0137b-126">-Path</span><span class="sxs-lookup"><span data-stu-id="0137b-126">-Path</span></span>
<span data-ttu-id="0137b-127">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="0137b-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0137b-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0137b-128">-Recurse</span></span>
<span data-ttu-id="0137b-129">Anger den ACL som ska anges rekursivt för underordnade under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="0137b-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="0137b-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="0137b-130">-ShowProgress</span></span>
<span data-ttu-id="0137b-131">Om förlopps statusen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="0137b-131">If passed then progress status is showed.</span></span> <span data-ttu-id="0137b-132">Gäller endast när rekursiv ACL-uppsättning är klar.</span><span class="sxs-lookup"><span data-stu-id="0137b-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="0137b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0137b-133">-Confirm</span></span>
<span data-ttu-id="0137b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0137b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0137b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0137b-135">-WhatIf</span></span>
<span data-ttu-id="0137b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0137b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0137b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0137b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0137b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0137b-138">CommonParameters</span></span>
<span data-ttu-id="0137b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0137b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0137b-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0137b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0137b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0137b-141">INPUTS</span></span>

### <span data-ttu-id="0137b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0137b-142">System.String</span></span>

### <span data-ttu-id="0137b-143">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0137b-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0137b-144">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="0137b-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="0137b-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0137b-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0137b-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0137b-146">System.Int32</span></span>

## <span data-ttu-id="0137b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0137b-147">OUTPUTS</span></span>

### <span data-ttu-id="0137b-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="0137b-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="0137b-149">Om PassThru anges returnerar den resulterande listan med ACL-poster.</span><span class="sxs-lookup"><span data-stu-id="0137b-149">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="0137b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0137b-150">NOTES</span></span>

## <span data-ttu-id="0137b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0137b-151">RELATED LINKS</span></span>
