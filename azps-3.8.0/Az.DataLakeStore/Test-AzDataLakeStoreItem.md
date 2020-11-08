---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 83f44ced24587340f063f24a17036184115cf299
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928194"
---
# <span data-ttu-id="cfa54-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="cfa54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfa54-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa54-103">Testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa54-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cfa54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfa54-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa54-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfa54-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa54-106">**Test-AzDataLakeStoreItem-** cmdleten testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa54-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cfa54-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfa54-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa54-108">Exempel 1: testa en fil</span><span class="sxs-lookup"><span data-stu-id="cfa54-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="cfa54-109">Det här kommandot testar om filen Test.csv finns i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="cfa54-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="cfa54-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfa54-110">PARAMETERS</span></span>

### <span data-ttu-id="cfa54-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="cfa54-111">-Account</span></span>
<span data-ttu-id="cfa54-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="cfa54-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cfa54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa54-113">-DefaultProfile</span></span>
<span data-ttu-id="cfa54-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa54-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa54-115">-Path</span><span class="sxs-lookup"><span data-stu-id="cfa54-115">-Path</span></span>
<span data-ttu-id="cfa54-116">Anger data Lake Store-sökvägen för objektet som ska testas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="cfa54-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cfa54-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="cfa54-117">-PathType</span></span>
<span data-ttu-id="cfa54-118">Anger vilken typ av objekt som ska testas.</span><span class="sxs-lookup"><span data-stu-id="cfa54-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="cfa54-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cfa54-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfa54-120">Eventuell</span><span class="sxs-lookup"><span data-stu-id="cfa54-120">Any</span></span> 
- <span data-ttu-id="cfa54-121">Fil</span><span class="sxs-lookup"><span data-stu-id="cfa54-121">File</span></span> 
- <span data-ttu-id="cfa54-122">Visningsmapp</span><span class="sxs-lookup"><span data-stu-id="cfa54-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa54-123">CommonParameters</span></span>
<span data-ttu-id="cfa54-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa54-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa54-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa54-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfa54-126">INPUTS</span></span>

### <span data-ttu-id="cfa54-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa54-127">System.String</span></span>

### <span data-ttu-id="cfa54-128">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="cfa54-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="cfa54-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="cfa54-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="cfa54-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfa54-130">OUTPUTS</span></span>

### <span data-ttu-id="cfa54-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cfa54-131">System.Boolean</span></span>

## <span data-ttu-id="cfa54-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfa54-132">NOTES</span></span>

## <span data-ttu-id="cfa54-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfa54-133">RELATED LINKS</span></span>

[<span data-ttu-id="cfa54-134">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="cfa54-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="cfa54-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="cfa54-137">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="cfa54-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="cfa54-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cfa54-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

