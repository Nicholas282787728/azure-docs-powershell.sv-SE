---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756985"
---
# <span data-ttu-id="3e9d2-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3e9d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9d2-103">Hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e9d2-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e9d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="3e9d2-106">Cmdleten **Get-AzureRmDataLakeStoreItem** hämtar information om en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3e9d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e9d2-107">EXAMPLES</span></span>

### <span data-ttu-id="3e9d2-108">Exempel 1: Hämta information om en fil från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3e9d2-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="3e9d2-109">Det här kommandot får information om filen Test.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="3e9d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e9d2-110">PARAMETERS</span></span>

### <span data-ttu-id="3e9d2-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3e9d2-111">-Account</span></span>
<span data-ttu-id="3e9d2-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3e9d2-113">-Path</span><span class="sxs-lookup"><span data-stu-id="3e9d2-113">-Path</span></span>
<span data-ttu-id="3e9d2-114">Anger sökvägen till data Lake Store från vilken du vill få information om ett objekt, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3e9d2-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3e9d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9d2-115">-DefaultProfile</span></span>
<span data-ttu-id="3e9d2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e9d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9d2-117">CommonParameters</span></span>
<span data-ttu-id="3e9d2-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9d2-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9d2-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e9d2-120">INPUTS</span></span>

## <span data-ttu-id="3e9d2-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e9d2-121">OUTPUTS</span></span>

### <span data-ttu-id="3e9d2-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-122">DataLakeStoreItem</span></span>
<span data-ttu-id="3e9d2-123">Filen eller mappen på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="3e9d2-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e9d2-124">NOTES</span></span>

## <span data-ttu-id="3e9d2-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e9d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="3e9d2-126">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="3e9d2-128">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-129">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-130">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-131">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-132">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3e9d2-133">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3e9d2-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


