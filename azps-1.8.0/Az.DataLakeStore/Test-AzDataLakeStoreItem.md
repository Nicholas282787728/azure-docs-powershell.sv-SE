---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754274"
---
# <span data-ttu-id="58bf3-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="58bf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="58bf3-103">Testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="58bf3-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="58bf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58bf3-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58bf3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="58bf3-106">**Test-AzDataLakeStoreItem-** cmdleten testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="58bf3-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="58bf3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="58bf3-108">Exempel 1: testa en fil</span><span class="sxs-lookup"><span data-stu-id="58bf3-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="58bf3-109">Det här kommandot testar om filen Test.csv finns i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="58bf3-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="58bf3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="58bf3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="58bf3-111">-Account</span></span>
<span data-ttu-id="58bf3-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="58bf3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="58bf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bf3-113">-DefaultProfile</span></span>
<span data-ttu-id="58bf3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58bf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58bf3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="58bf3-115">-Path</span></span>
<span data-ttu-id="58bf3-116">Anger data Lake Store-sökvägen för objektet som ska testas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="58bf3-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="58bf3-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="58bf3-117">-PathType</span></span>
<span data-ttu-id="58bf3-118">Anger vilken typ av objekt som ska testas.</span><span class="sxs-lookup"><span data-stu-id="58bf3-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="58bf3-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="58bf3-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58bf3-120">Eventuell</span><span class="sxs-lookup"><span data-stu-id="58bf3-120">Any</span></span> 
- <span data-ttu-id="58bf3-121">Fil</span><span class="sxs-lookup"><span data-stu-id="58bf3-121">File</span></span> 
- <span data-ttu-id="58bf3-122">Visningsmapp</span><span class="sxs-lookup"><span data-stu-id="58bf3-122">Folder</span></span>

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

### <span data-ttu-id="58bf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bf3-123">CommonParameters</span></span>
<span data-ttu-id="58bf3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58bf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bf3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bf3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bf3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58bf3-126">INPUTS</span></span>

### <span data-ttu-id="58bf3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="58bf3-127">System.String</span></span>

### <span data-ttu-id="58bf3-128">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="58bf3-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="58bf3-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="58bf3-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="58bf3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58bf3-130">OUTPUTS</span></span>

### <span data-ttu-id="58bf3-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58bf3-131">System.Boolean</span></span>

## <span data-ttu-id="58bf3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58bf3-132">NOTES</span></span>

## <span data-ttu-id="58bf3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58bf3-133">RELATED LINKS</span></span>

[<span data-ttu-id="58bf3-134">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="58bf3-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="58bf3-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="58bf3-137">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="58bf3-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="58bf3-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="58bf3-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


