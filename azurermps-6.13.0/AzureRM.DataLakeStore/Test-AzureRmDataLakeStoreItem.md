---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582696"
---
# <span data-ttu-id="92845-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="92845-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92845-102">SYNOPSIS</span></span>
<span data-ttu-id="92845-103">Testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92845-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92845-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92845-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92845-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92845-105">DESCRIPTION</span></span>
<span data-ttu-id="92845-106">**Test-AzureRmDataLakeStoreItem-** cmdleten testar förekomsten av en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92845-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92845-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92845-107">EXAMPLES</span></span>

### <span data-ttu-id="92845-108">Exempel 1: testa en fil</span><span class="sxs-lookup"><span data-stu-id="92845-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="92845-109">Det här kommandot testar om filen Test.csv finns i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="92845-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="92845-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92845-110">PARAMETERS</span></span>

### <span data-ttu-id="92845-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="92845-111">-Account</span></span>
<span data-ttu-id="92845-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="92845-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="92845-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92845-113">-DefaultProfile</span></span>
<span data-ttu-id="92845-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92845-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92845-115">-Path</span><span class="sxs-lookup"><span data-stu-id="92845-115">-Path</span></span>
<span data-ttu-id="92845-116">Anger data Lake Store-sökvägen för objektet som ska testas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="92845-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92845-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="92845-117">-PathType</span></span>
<span data-ttu-id="92845-118">Anger vilken typ av objekt som ska testas.</span><span class="sxs-lookup"><span data-stu-id="92845-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="92845-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="92845-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92845-120">Eventuell</span><span class="sxs-lookup"><span data-stu-id="92845-120">Any</span></span> 
- <span data-ttu-id="92845-121">Fil</span><span class="sxs-lookup"><span data-stu-id="92845-121">File</span></span> 
- <span data-ttu-id="92845-122">Visningsmapp</span><span class="sxs-lookup"><span data-stu-id="92845-122">Folder</span></span>

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

### <span data-ttu-id="92845-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92845-123">CommonParameters</span></span>
<span data-ttu-id="92845-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92845-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92845-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92845-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92845-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92845-126">INPUTS</span></span>

### <span data-ttu-id="92845-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92845-127">System.String</span></span>

### <span data-ttu-id="92845-128">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="92845-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="92845-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="92845-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="92845-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92845-130">OUTPUTS</span></span>

### <span data-ttu-id="92845-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92845-131">System.Boolean</span></span>

## <span data-ttu-id="92845-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92845-132">NOTES</span></span>

## <span data-ttu-id="92845-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92845-133">RELATED LINKS</span></span>

[<span data-ttu-id="92845-134">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="92845-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="92845-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="92845-137">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="92845-138">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="92845-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92845-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


