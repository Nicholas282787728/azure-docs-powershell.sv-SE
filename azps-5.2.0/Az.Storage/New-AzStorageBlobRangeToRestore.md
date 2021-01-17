---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388800"
---
# <span data-ttu-id="d2b05-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="d2b05-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="d2b05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2b05-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b05-103">Skapar ett BLOB Range-objekt som återställer ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2b05-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="d2b05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2b05-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2b05-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b05-106">Cmdleten **New-AzStorageBlobRangeToRestore** skapar ett BLOB Range-objekt som kan användas i Återställ-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="d2b05-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="d2b05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2b05-107">EXAMPLES</span></span>

### <span data-ttu-id="d2b05-108">Exempel 1: skapar ett BLOB-intervall att återställa</span><span class="sxs-lookup"><span data-stu-id="d2b05-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="d2b05-109">Det här kommandot skapar ett BLOB-intervall som ska återställas, som börjar på container1/blob1 (include) och slutar på container2/blob2 (exclude).</span><span class="sxs-lookup"><span data-stu-id="d2b05-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="d2b05-110">Exempel 2: skapar ett BLOB-intervall som återställs från första blobben i alfabetisk ordning till en specifik BLOB (exkludera)</span><span class="sxs-lookup"><span data-stu-id="d2b05-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="d2b05-111">Det här kommandot skapar ett BLOB-intervall som återställs från första blobben i alfabetisk ordning till en specifik BLOB-container2/blob2 (exkludera)</span><span class="sxs-lookup"><span data-stu-id="d2b05-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="d2b05-112">Exempel 3: skapar ett BLOB-intervall som återställs från en specifik BLOB (include) till sista blobben i alfabetisk ordning</span><span class="sxs-lookup"><span data-stu-id="d2b05-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="d2b05-113">Det här kommandot skapar ett BLOB-intervall som återställs från en specifik BLOB-container1/blob1 (include) till sista blobben i alfabetisk ordning.</span><span class="sxs-lookup"><span data-stu-id="d2b05-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="d2b05-114">Exempel 4: skapar ett BLOB-intervall som återställer alla blobbar</span><span class="sxs-lookup"><span data-stu-id="d2b05-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="d2b05-115">Det här kommandot skapar ett BLOB-intervall som återställer alla blobbar.</span><span class="sxs-lookup"><span data-stu-id="d2b05-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="d2b05-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2b05-116">PARAMETERS</span></span>

### <span data-ttu-id="d2b05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b05-117">-DefaultProfile</span></span>
<span data-ttu-id="d2b05-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b05-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="d2b05-119">-EndRange</span></span>
<span data-ttu-id="d2b05-120">Ange slut intervallet för BLOB-återställning.</span><span class="sxs-lookup"><span data-stu-id="d2b05-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="d2b05-121">Slut intervallet utesluts i återställda blobs.</span><span class="sxs-lookup"><span data-stu-id="d2b05-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="d2b05-122">Ange den som Tom Strng för att återställa till slutet.</span><span class="sxs-lookup"><span data-stu-id="d2b05-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b05-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="d2b05-123">-StartRange</span></span>
<span data-ttu-id="d2b05-124">Ange start intervallet för BLOB-återställning.</span><span class="sxs-lookup"><span data-stu-id="d2b05-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="d2b05-125">Start intervall tas med i återställda blobs.</span><span class="sxs-lookup"><span data-stu-id="d2b05-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="d2b05-126">Ange den som en tom sträng för att återställa från början.</span><span class="sxs-lookup"><span data-stu-id="d2b05-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b05-127">CommonParameters</span></span>
<span data-ttu-id="d2b05-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b05-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b05-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b05-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2b05-130">INPUTS</span></span>

### <span data-ttu-id="d2b05-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="d2b05-131">None</span></span>

## <span data-ttu-id="d2b05-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2b05-132">OUTPUTS</span></span>

### <span data-ttu-id="d2b05-133">Microsoft. Azure. commands. Management. Storage. Models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="d2b05-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="d2b05-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2b05-134">NOTES</span></span>

## <span data-ttu-id="d2b05-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2b05-135">RELATED LINKS</span></span>
