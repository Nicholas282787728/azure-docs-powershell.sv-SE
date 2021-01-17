---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405467"
---
# <span data-ttu-id="30a77-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="30a77-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="30a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30a77-102">SYNOPSIS</span></span>
<span data-ttu-id="30a77-103">Söker efter borttagna poster i pappers korgen som matchar filtret.</span><span class="sxs-lookup"><span data-stu-id="30a77-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="30a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30a77-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30a77-105">DESCRIPTION</span></span>
<span data-ttu-id="30a77-106">Cmdleten **Get-AzDataLakeStoreDeletedItem** söker igenom borttagna filer och mappar i data Lake Store som matchar angivet filter.</span><span class="sxs-lookup"><span data-stu-id="30a77-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="30a77-107">Här visas följande attribut för borttagna objekt – OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="30a77-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="30a77-108">Detta kan vara tids krävande att köra eftersom det kanske måste söka igenom miljon tals filer i pappers korgen och kan köras som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="30a77-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="30a77-109">Varning! det är en bra åtgärd att ta bort filer.</span><span class="sxs-lookup"><span data-stu-id="30a77-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="30a77-110">Det finns inga garantier för att en fil kan återställas när den har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="30a77-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="30a77-111">Användningen av detta API aktive ras via väggar.</span><span class="sxs-lookup"><span data-stu-id="30a77-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="30a77-112">Om ditt ADL-konto inte är whitelisted, följer detta API inte implementerat undantag.</span><span class="sxs-lookup"><span data-stu-id="30a77-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="30a77-113">Om du vill ha mer information kontaktar du Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="30a77-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="30a77-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30a77-114">EXAMPLES</span></span>

### <span data-ttu-id="30a77-115">Exempel: Hämta information om en fil från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="30a77-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="30a77-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30a77-116">PARAMETERS</span></span>

### <span data-ttu-id="30a77-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="30a77-117">-Account</span></span>
<span data-ttu-id="30a77-118">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="30a77-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="30a77-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30a77-119">-AsJob</span></span>
<span data-ttu-id="30a77-120">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="30a77-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="30a77-121">-Antal</span><span class="sxs-lookup"><span data-stu-id="30a77-121">-Count</span></span>
<span data-ttu-id="30a77-122">Anger antal resultat som användaren vill hitta.</span><span class="sxs-lookup"><span data-stu-id="30a77-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="30a77-123">Frågan körs tills den returnerar räknare eller söker igenom hela pappers korgen, vilket sker först.</span><span class="sxs-lookup"><span data-stu-id="30a77-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a77-124">-DefaultProfile</span></span>
<span data-ttu-id="30a77-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30a77-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a77-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="30a77-126">-Filter</span></span>
<span data-ttu-id="30a77-127">Anger Sök frågan.</span><span class="sxs-lookup"><span data-stu-id="30a77-127">Specifies the search query.</span></span> <span data-ttu-id="30a77-128">Ett mer specifikt värde ger mer relevanta resultat.</span><span class="sxs-lookup"><span data-stu-id="30a77-128">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a77-129">CommonParameters</span></span>
<span data-ttu-id="30a77-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a77-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30a77-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a77-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30a77-132">INPUTS</span></span>

### <span data-ttu-id="30a77-133">System. String</span><span class="sxs-lookup"><span data-stu-id="30a77-133">System.String</span></span>

## <span data-ttu-id="30a77-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30a77-134">OUTPUTS</span></span>

### <span data-ttu-id="30a77-135">System. Collections. Generic. list<Microsoft. Azure. kommandon. DataLakeStore. Models. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="30a77-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="30a77-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30a77-136">NOTES</span></span>

## <span data-ttu-id="30a77-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30a77-137">RELATED LINKS</span></span>

[<span data-ttu-id="30a77-138">Återställ-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="30a77-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)