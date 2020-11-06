---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580640"
---
# <span data-ttu-id="fc8fd-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="fc8fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8fd-103">Testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc8fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc8fd-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc8fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc8fd-105">DESCRIPTION</span></span>
<span data-ttu-id="fc8fd-106">**Test-AzureRmDataLakeStoreItem-** cmdleten testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc8fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc8fd-107">EXAMPLES</span></span>

### <span data-ttu-id="fc8fd-108">Exempel 1: testa en fil</span><span class="sxs-lookup"><span data-stu-id="fc8fd-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="fc8fd-109">Det här kommandot testar om filen Test.csv finns i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="fc8fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc8fd-110">PARAMETERS</span></span>

### <span data-ttu-id="fc8fd-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="fc8fd-111">-Account</span></span>
<span data-ttu-id="fc8fd-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fc8fd-113">-Path</span><span class="sxs-lookup"><span data-stu-id="fc8fd-113">-Path</span></span>
<span data-ttu-id="fc8fd-114">Anger data Lake Store-sökvägen för objektet som ska testas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="fc8fd-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fc8fd-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="fc8fd-115">-PathType</span></span>
<span data-ttu-id="fc8fd-116">Anger vilken typ av objekt som ska testas.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="fc8fd-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fc8fd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc8fd-118">Eventuell</span><span class="sxs-lookup"><span data-stu-id="fc8fd-118">Any</span></span> 
- <span data-ttu-id="fc8fd-119">Fil</span><span class="sxs-lookup"><span data-stu-id="fc8fd-119">File</span></span> 
- <span data-ttu-id="fc8fd-120">Visningsmapp</span><span class="sxs-lookup"><span data-stu-id="fc8fd-120">Folder</span></span>

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

### <span data-ttu-id="fc8fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8fd-121">-DefaultProfile</span></span>
<span data-ttu-id="fc8fd-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc8fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8fd-123">CommonParameters</span></span>
<span data-ttu-id="fc8fd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8fd-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8fd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc8fd-126">INPUTS</span></span>

## <span data-ttu-id="fc8fd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc8fd-127">OUTPUTS</span></span>

### <span data-ttu-id="fc8fd-128">bool</span><span class="sxs-lookup"><span data-stu-id="fc8fd-128">bool</span></span>
<span data-ttu-id="fc8fd-129">True eller false anger att den angivna filen eller mappen existerar.</span><span class="sxs-lookup"><span data-stu-id="fc8fd-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="fc8fd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc8fd-130">NOTES</span></span>

## <span data-ttu-id="fc8fd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc8fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc8fd-132">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc8fd-133">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc8fd-134">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc8fd-135">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc8fd-136">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc8fd-137">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc8fd-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


