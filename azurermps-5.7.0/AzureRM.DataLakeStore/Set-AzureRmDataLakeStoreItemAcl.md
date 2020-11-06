---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 313813bec61dac2f5b41f7ad2d36e5ee5ba1b44f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574956"
---
# <span data-ttu-id="e9b6e-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e9b6e-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="e9b6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b6e-103">Ändrar åtkomst kontroll för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9b6e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b6e-106">Cmdleten **set-AzureRmDataLakeStoreItemAcl** ändrar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e9b6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b6e-108">Exempel 1: ange ACL för en fil och en mapp</span><span class="sxs-lookup"><span data-stu-id="e9b6e-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="e9b6e-109">Det första kommandot får ACL för rot katalogen för ContosoADL-kontot och lagrar den sedan i $ACL variabel.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="e9b6e-110">Med det andra kommandot anges åtkomst kontrol listan för filen Test.txt till den i $ACL.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="e9b6e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9b6e-111">PARAMETERS</span></span>

### <span data-ttu-id="e9b6e-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="e9b6e-112">-Account</span></span>
<span data-ttu-id="e9b6e-113">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e9b6e-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="e9b6e-114">-Acl</span></span>
<span data-ttu-id="e9b6e-115">Anger en ACL för en fil eller en mapp.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b6e-116">-DefaultProfile</span></span>
<span data-ttu-id="e9b6e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b6e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9b6e-118">-PassThru</span></span>
<span data-ttu-id="e9b6e-119">Anger att den resulterande ACL-listan returneras.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-119">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="e9b6e-120">-Path</span><span class="sxs-lookup"><span data-stu-id="e9b6e-120">-Path</span></span>
<span data-ttu-id="e9b6e-121">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="e9b6e-121">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e9b6e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9b6e-122">-Confirm</span></span>
<span data-ttu-id="e9b6e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b6e-124">-WhatIf</span></span>
<span data-ttu-id="e9b6e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b6e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b6e-127">CommonParameters</span></span>
<span data-ttu-id="e9b6e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b6e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b6e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b6e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9b6e-130">INPUTS</span></span>

### <span data-ttu-id="e9b6e-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="e9b6e-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="e9b6e-132">Parametern ' ACL ' godkänner värdet av typen ' DataLakeStoreItemAce [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e9b6e-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="e9b6e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9b6e-133">OUTPUTS</span></span>

### <span data-ttu-id="e9b6e-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="e9b6e-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="e9b6e-135">Om PassThru anges returnerar den resulterande listan med ACL-poster.</span><span class="sxs-lookup"><span data-stu-id="e9b6e-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="e9b6e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9b6e-136">NOTES</span></span>

## <span data-ttu-id="e9b6e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9b6e-137">RELATED LINKS</span></span>

