---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755496"
---
# <span data-ttu-id="22ac9-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="22ac9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="22ac9-103">Hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22ac9-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22ac9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22ac9-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ac9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="22ac9-106">Cmdleten **Get-AzureRmDataLakeStoreItem** hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22ac9-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="22ac9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="22ac9-108">Exempel 1: Hämta information om en fil från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="22ac9-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="22ac9-109">Det här kommandot får information om filen Test.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22ac9-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="22ac9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="22ac9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="22ac9-111">-Account</span></span>
<span data-ttu-id="22ac9-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="22ac9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="22ac9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ac9-113">-DefaultProfile</span></span>
<span data-ttu-id="22ac9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22ac9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ac9-115">-Path</span><span class="sxs-lookup"><span data-stu-id="22ac9-115">-Path</span></span>
<span data-ttu-id="22ac9-116">Anger sökvägen till data Lake Store från vilken du vill få information om ett objekt, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="22ac9-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="22ac9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ac9-117">CommonParameters</span></span>
<span data-ttu-id="22ac9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ac9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ac9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ac9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ac9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22ac9-120">INPUTS</span></span>

### <span data-ttu-id="22ac9-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="22ac9-121">None</span></span>
<span data-ttu-id="22ac9-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="22ac9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22ac9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22ac9-123">OUTPUTS</span></span>

### <span data-ttu-id="22ac9-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-124">DataLakeStoreItem</span></span>
<span data-ttu-id="22ac9-125">Filen eller mappen på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="22ac9-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="22ac9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22ac9-126">NOTES</span></span>

## <span data-ttu-id="22ac9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22ac9-127">RELATED LINKS</span></span>

[<span data-ttu-id="22ac9-128">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-129">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="22ac9-130">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-131">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-132">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-133">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-134">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="22ac9-135">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="22ac9-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


