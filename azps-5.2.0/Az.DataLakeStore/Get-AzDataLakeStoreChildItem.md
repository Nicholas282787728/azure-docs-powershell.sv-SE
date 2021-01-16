---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406376"
---
# <span data-ttu-id="20ff3-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="20ff3-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="20ff3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="20ff3-103">Hämtar listan med objekt i en mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ff3-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="20ff3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20ff3-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ff3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="20ff3-106">Cmdleten **Get-AzDataLakeStoreChildItem** hämtar listan med objekt i en mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ff3-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="20ff3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="20ff3-108">Exempel 1: Hämta underordnade objekt till en mapp</span><span class="sxs-lookup"><span data-stu-id="20ff3-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="20ff3-109">Det här kommandot får underordnade objekt till mappen Mina filer.</span><span class="sxs-lookup"><span data-stu-id="20ff3-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="20ff3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20ff3-110">PARAMETERS</span></span>

### <span data-ttu-id="20ff3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="20ff3-111">-Account</span></span>
<span data-ttu-id="20ff3-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="20ff3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="20ff3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ff3-113">-DefaultProfile</span></span>
<span data-ttu-id="20ff3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20ff3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ff3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="20ff3-115">-Path</span></span>
<span data-ttu-id="20ff3-116">Anger data Lake Store-sökvägen till mappen, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="20ff3-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="20ff3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ff3-117">CommonParameters</span></span>
<span data-ttu-id="20ff3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ff3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ff3-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ff3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ff3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20ff3-120">INPUTS</span></span>

### <span data-ttu-id="20ff3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="20ff3-121">System.String</span></span>

### <span data-ttu-id="20ff3-122">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="20ff3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="20ff3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20ff3-123">OUTPUTS</span></span>

### <span data-ttu-id="20ff3-124">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20ff3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="20ff3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20ff3-125">NOTES</span></span>

## <span data-ttu-id="20ff3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20ff3-126">RELATED LINKS</span></span>
