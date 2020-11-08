---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 76490987a6a4d016a1d07b29cd69484305ddf849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916898"
---
# <span data-ttu-id="5efda-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="5efda-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="5efda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5efda-102">SYNOPSIS</span></span>
<span data-ttu-id="5efda-103">Hämtar sammanfattningen av Total storlek, filer och kataloger i den angivna sökvägen</span><span class="sxs-lookup"><span data-stu-id="5efda-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="5efda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5efda-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5efda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5efda-105">DESCRIPTION</span></span>
<span data-ttu-id="5efda-106">Med **Get-AzDataLakeStoreChildItemSummary** hämtas innehålls sammanfattningen för en given sökväg.</span><span class="sxs-lookup"><span data-stu-id="5efda-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="5efda-107">Det totala antalet filer, kataloger och Total storlek för alla filer under den angivna sökvägen rekursivt beräknas.</span><span class="sxs-lookup"><span data-stu-id="5efda-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="5efda-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5efda-108">EXAMPLES</span></span>

### <span data-ttu-id="5efda-109">Exempel 1: Hämta innehålls sammanfattningen för en mapp</span><span class="sxs-lookup"><span data-stu-id="5efda-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="5efda-110">Här listas antalet kataloger, filer och deras storlek som finns under/a.</span><span class="sxs-lookup"><span data-stu-id="5efda-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="5efda-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5efda-111">PARAMETERS</span></span>

### <span data-ttu-id="5efda-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="5efda-112">-Account</span></span>
<span data-ttu-id="5efda-113">Data Lake Store-kontot för att köra filesystem-åtgärden i</span><span class="sxs-lookup"><span data-stu-id="5efda-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="5efda-114">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="5efda-114">-Concurrency</span></span>
<span data-ttu-id="5efda-115">Anger antalet filer/kataloger som har bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="5efda-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="5efda-116">Standard beräknas som en bästa ansträngning baserat på systemets specifikation.</span><span class="sxs-lookup"><span data-stu-id="5efda-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="5efda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efda-117">-DefaultProfile</span></span>
<span data-ttu-id="5efda-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5efda-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5efda-119">-Path</span><span class="sxs-lookup"><span data-stu-id="5efda-119">-Path</span></span>
<span data-ttu-id="5efda-120">Sökvägen för det data Lake-konto som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="5efda-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="5efda-121">Kan vara en fil eller mapp i formatet '/Folder/file.txt ', där "/" efter DNS anger fil systemets rot.</span><span class="sxs-lookup"><span data-stu-id="5efda-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5efda-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5efda-122">-Confirm</span></span>
<span data-ttu-id="5efda-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5efda-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5efda-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5efda-124">-WhatIf</span></span>
<span data-ttu-id="5efda-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5efda-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5efda-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5efda-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5efda-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efda-127">CommonParameters</span></span>
<span data-ttu-id="5efda-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5efda-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efda-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5efda-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efda-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5efda-130">INPUTS</span></span>

### <span data-ttu-id="5efda-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5efda-131">System.String</span></span>

### <span data-ttu-id="5efda-132">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5efda-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5efda-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5efda-133">System.Int32</span></span>

## <span data-ttu-id="5efda-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5efda-134">OUTPUTS</span></span>

### <span data-ttu-id="5efda-135">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="5efda-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="5efda-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5efda-136">NOTES</span></span>

## <span data-ttu-id="5efda-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5efda-137">RELATED LINKS</span></span>