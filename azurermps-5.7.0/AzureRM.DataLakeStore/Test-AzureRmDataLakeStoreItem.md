---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: bf754e335753efc5350d3c0979db9f0f7057f010
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757263"
---
# <span data-ttu-id="3c5c4-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3c5c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5c4-103">Testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c5c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c5c4-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c5c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="3c5c4-106">**Test-AzureRmDataLakeStoreItem-** cmdleten testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3c5c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c5c4-107">EXAMPLES</span></span>

### <span data-ttu-id="3c5c4-108">Exempel 1: testa en fil</span><span class="sxs-lookup"><span data-stu-id="3c5c4-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="3c5c4-109">Det här kommandot testar om filen Test.csv finns i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="3c5c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c5c4-110">PARAMETERS</span></span>

### <span data-ttu-id="3c5c4-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3c5c4-111">-Account</span></span>
<span data-ttu-id="3c5c4-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3c5c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5c4-113">-DefaultProfile</span></span>
<span data-ttu-id="3c5c4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c5c4-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3c5c4-115">-Path</span></span>
<span data-ttu-id="3c5c4-116">Anger data Lake Store-sökvägen för objektet som ska testas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3c5c4-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3c5c4-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="3c5c4-117">-PathType</span></span>
<span data-ttu-id="3c5c4-118">Anger vilken typ av objekt som ska testas.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="3c5c4-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3c5c4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c5c4-120">Eventuell</span><span class="sxs-lookup"><span data-stu-id="3c5c4-120">Any</span></span> 
- <span data-ttu-id="3c5c4-121">Fil</span><span class="sxs-lookup"><span data-stu-id="3c5c4-121">File</span></span> 
- <span data-ttu-id="3c5c4-122">Visningsmapp</span><span class="sxs-lookup"><span data-stu-id="3c5c4-122">Folder</span></span>

```yaml
Type: PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5c4-123">CommonParameters</span></span>
<span data-ttu-id="3c5c4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5c4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c5c4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5c4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c5c4-126">INPUTS</span></span>

### <span data-ttu-id="3c5c4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c5c4-127">None</span></span>
<span data-ttu-id="3c5c4-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c5c4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c5c4-129">OUTPUTS</span></span>

### <span data-ttu-id="3c5c4-130">bool</span><span class="sxs-lookup"><span data-stu-id="3c5c4-130">bool</span></span>
<span data-ttu-id="3c5c4-131">True eller false anger att den angivna filen eller mappen existerar.</span><span class="sxs-lookup"><span data-stu-id="3c5c4-131">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="3c5c4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c5c4-132">NOTES</span></span>

## <span data-ttu-id="3c5c4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c5c4-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c5c4-134">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3c5c4-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3c5c4-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3c5c4-137">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3c5c4-138">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3c5c4-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c5c4-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


