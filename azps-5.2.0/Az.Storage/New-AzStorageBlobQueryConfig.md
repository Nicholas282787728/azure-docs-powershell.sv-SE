---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404120"
---
# <span data-ttu-id="8d829-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="8d829-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="8d829-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d829-102">SYNOPSIS</span></span>
<span data-ttu-id="8d829-103">Skapar ett BLOB-frågeinställningar som kan användas i get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="8d829-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="8d829-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d829-104">SYNTAX</span></span>

### <span data-ttu-id="8d829-105">CSV (standard)</span><span class="sxs-lookup"><span data-stu-id="8d829-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="8d829-106">JSON</span><span class="sxs-lookup"><span data-stu-id="8d829-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="8d829-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d829-107">DESCRIPTION</span></span>
<span data-ttu-id="8d829-108">Cmdleten **New-AzStorageBlobQueryConfig** skapar ett BLOB-frågeinställningar som kan användas i get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="8d829-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="8d829-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d829-109">EXAMPLES</span></span>

### <span data-ttu-id="8d829-110">Exempel 1: skapa BLOB-fråga konfigurerar och fråga en BLOB</span><span class="sxs-lookup"><span data-stu-id="8d829-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="8d829-111">Det här kommandot skapar först autokonfigurations objekt som CSV och utgående konfigurations objekt som JSON och använder sedan 2-konfigurationerna för att fråga blob.</span><span class="sxs-lookup"><span data-stu-id="8d829-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="8d829-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d829-112">PARAMETERS</span></span>

### <span data-ttu-id="8d829-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="8d829-113">-AsCsv</span></span>
<span data-ttu-id="8d829-114">Ange att du vill skapa en BLOB-frågeinställningar för CSV.</span><span class="sxs-lookup"><span data-stu-id="8d829-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d829-115">-AsJob</span></span>
<span data-ttu-id="8d829-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8d829-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-117">-Inter-JSON</span><span class="sxs-lookup"><span data-stu-id="8d829-117">-AsJson</span></span>
<span data-ttu-id="8d829-118">Ange att du vill skapa en BLOB-frågeinställningar för JSON.</span><span class="sxs-lookup"><span data-stu-id="8d829-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="8d829-119">-ColumnSeparator</span></span>
<span data-ttu-id="8d829-120">Skriver.</span><span class="sxs-lookup"><span data-stu-id="8d829-120">Optional.</span></span>
<span data-ttu-id="8d829-121">Strängen som används för att avgränsa kolumner.</span><span class="sxs-lookup"><span data-stu-id="8d829-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="8d829-122">-EscapeCharacter</span></span>
<span data-ttu-id="8d829-123">Skriver.</span><span class="sxs-lookup"><span data-stu-id="8d829-123">Optional.</span></span>
<span data-ttu-id="8d829-124">Tecken som används som escape-tecken.</span><span class="sxs-lookup"><span data-stu-id="8d829-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="8d829-125">-HasHeader</span></span>
<span data-ttu-id="8d829-126">Skriver.</span><span class="sxs-lookup"><span data-stu-id="8d829-126">Optional.</span></span>
<span data-ttu-id="8d829-127">Visa att den representerar data som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="8d829-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="8d829-128">-QuotationCharacter</span></span>
<span data-ttu-id="8d829-129">Skriver.</span><span class="sxs-lookup"><span data-stu-id="8d829-129">Optional.</span></span>
<span data-ttu-id="8d829-130">Tecken som används för att citera ett visst fält.</span><span class="sxs-lookup"><span data-stu-id="8d829-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d829-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="8d829-131">-RecordSeparator</span></span>
<span data-ttu-id="8d829-132">Skriver.</span><span class="sxs-lookup"><span data-stu-id="8d829-132">Optional.</span></span>
<span data-ttu-id="8d829-133">Strängen som används för att separera poster.</span><span class="sxs-lookup"><span data-stu-id="8d829-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="8d829-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d829-134">CommonParameters</span></span>
<span data-ttu-id="8d829-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d829-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d829-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d829-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d829-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d829-137">INPUTS</span></span>

### <span data-ttu-id="8d829-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="8d829-138">None</span></span>

## <span data-ttu-id="8d829-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d829-139">OUTPUTS</span></span>

### <span data-ttu-id="8d829-140">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d829-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="8d829-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d829-141">NOTES</span></span>

## <span data-ttu-id="8d829-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d829-142">RELATED LINKS</span></span>
