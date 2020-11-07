---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: b3118c11fa794fef71836a580e272ec481c72147
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916889"
---
# <span data-ttu-id="57ee1-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="57ee1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="57ee1-103">Hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57ee1-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="57ee1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57ee1-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ee1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="57ee1-106">Cmdleten **Get-AzDataLakeStoreItem** hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57ee1-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="57ee1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="57ee1-108">Exempel 1: Hämta information om en fil från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="57ee1-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="57ee1-109">Det här kommandot får information om filen Test.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57ee1-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="57ee1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57ee1-110">PARAMETERS</span></span>

### <span data-ttu-id="57ee1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="57ee1-111">-Account</span></span>
<span data-ttu-id="57ee1-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="57ee1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="57ee1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ee1-113">-DefaultProfile</span></span>
<span data-ttu-id="57ee1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57ee1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ee1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="57ee1-115">-Path</span></span>
<span data-ttu-id="57ee1-116">Anger sökvägen till data Lake Store från vilken du vill få information om ett objekt, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="57ee1-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="57ee1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ee1-117">CommonParameters</span></span>
<span data-ttu-id="57ee1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ee1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ee1-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ee1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ee1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57ee1-120">INPUTS</span></span>

### <span data-ttu-id="57ee1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="57ee1-121">System.String</span></span>

### <span data-ttu-id="57ee1-122">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="57ee1-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="57ee1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57ee1-123">OUTPUTS</span></span>

### <span data-ttu-id="57ee1-124">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="57ee1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57ee1-125">NOTES</span></span>

## <span data-ttu-id="57ee1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57ee1-126">RELATED LINKS</span></span>

[<span data-ttu-id="57ee1-127">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="57ee1-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-130">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="57ee1-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57ee1-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


