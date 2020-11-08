---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270408"
---
# <span data-ttu-id="af748-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="af748-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="af748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af748-102">SYNOPSIS</span></span>
<span data-ttu-id="af748-103">Skapar ett BLOB-frågeinställningar som kan användas i get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="af748-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="af748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af748-104">SYNTAX</span></span>

### <span data-ttu-id="af748-105">CSV (standard)</span><span class="sxs-lookup"><span data-stu-id="af748-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="af748-106">JSON</span><span class="sxs-lookup"><span data-stu-id="af748-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="af748-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af748-107">DESCRIPTION</span></span>
<span data-ttu-id="af748-108">Cmdleten **New-AzStorageBlobQueryConfig** skapar ett BLOB-frågeinställningar som kan användas i get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="af748-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="af748-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af748-109">EXAMPLES</span></span>

### <span data-ttu-id="af748-110">Exempel 1: skapa BLOB-fråga konfigurerar och fråga en BLOB</span><span class="sxs-lookup"><span data-stu-id="af748-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="af748-111">Det här kommandot skapar först autokonfigurations objekt som CSV och utgående konfigurations objekt som JSON och använder sedan 2-konfigurationerna för att fråga blob.</span><span class="sxs-lookup"><span data-stu-id="af748-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="af748-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af748-112">PARAMETERS</span></span>

### <span data-ttu-id="af748-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="af748-113">-AsCsv</span></span>
<span data-ttu-id="af748-114">Ange att du vill skapa en BLOB-frågeinställningar för CSV.</span><span class="sxs-lookup"><span data-stu-id="af748-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="af748-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af748-115">-AsJob</span></span>
<span data-ttu-id="af748-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="af748-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af748-117">-Inter-JSON</span><span class="sxs-lookup"><span data-stu-id="af748-117">-AsJson</span></span>
<span data-ttu-id="af748-118">Ange att du vill skapa en BLOB-frågeinställningar för JSON.</span><span class="sxs-lookup"><span data-stu-id="af748-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="af748-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="af748-119">-ColumnSeparator</span></span>
<span data-ttu-id="af748-120">Skriver.</span><span class="sxs-lookup"><span data-stu-id="af748-120">Optional.</span></span>
<span data-ttu-id="af748-121">Strängen som används för att avgränsa kolumner.</span><span class="sxs-lookup"><span data-stu-id="af748-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="af748-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="af748-122">-EscapeCharacter</span></span>
<span data-ttu-id="af748-123">Skriver.</span><span class="sxs-lookup"><span data-stu-id="af748-123">Optional.</span></span>
<span data-ttu-id="af748-124">Tecken som används som escape-tecken.</span><span class="sxs-lookup"><span data-stu-id="af748-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="af748-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="af748-125">-HasHeader</span></span>
<span data-ttu-id="af748-126">Skriver.</span><span class="sxs-lookup"><span data-stu-id="af748-126">Optional.</span></span>
<span data-ttu-id="af748-127">Visa att den representerar data som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="af748-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="af748-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="af748-128">-QuotationCharacter</span></span>
<span data-ttu-id="af748-129">Skriver.</span><span class="sxs-lookup"><span data-stu-id="af748-129">Optional.</span></span>
<span data-ttu-id="af748-130">Tecken som används för att citera ett visst fält.</span><span class="sxs-lookup"><span data-stu-id="af748-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="af748-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="af748-131">-RecordSeparator</span></span>
<span data-ttu-id="af748-132">Skriver.</span><span class="sxs-lookup"><span data-stu-id="af748-132">Optional.</span></span>
<span data-ttu-id="af748-133">Strängen som används för att separera poster.</span><span class="sxs-lookup"><span data-stu-id="af748-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="af748-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af748-134">CommonParameters</span></span>
<span data-ttu-id="af748-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af748-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af748-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af748-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af748-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af748-137">INPUTS</span></span>

### <span data-ttu-id="af748-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="af748-138">None</span></span>

## <span data-ttu-id="af748-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af748-139">OUTPUTS</span></span>

### <span data-ttu-id="af748-140">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="af748-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="af748-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af748-141">NOTES</span></span>

## <span data-ttu-id="af748-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af748-142">RELATED LINKS</span></span>
