---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522175"
---
# <span data-ttu-id="0974d-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="0974d-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="0974d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0974d-102">SYNOPSIS</span></span>
<span data-ttu-id="0974d-103">Tillämpar en enkel SQL-programsats (Structured Query Language) på en blobs innehåll och bara sparar den efterfrågade del mängden av data i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="0974d-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="0974d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0974d-104">SYNTAX</span></span>

### <span data-ttu-id="0974d-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="0974d-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0974d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0974d-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0974d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0974d-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0974d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0974d-108">DESCRIPTION</span></span>
<span data-ttu-id="0974d-109">Cmdleten **Get-AzStorageBlobQueryResult** tillämpar en enkel SQL-programsats (Structured Query Language) på en blobs innehåll och sparar den efterfrågade del mängden av data i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="0974d-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="0974d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0974d-110">EXAMPLES</span></span>

### <span data-ttu-id="0974d-111">Exempel 1: fråga a Blob</span><span class="sxs-lookup"><span data-stu-id="0974d-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="0974d-112">Det här kommandot frågar en BLOB-succsssfully med input config som CSV och utdata-config som JSON och sparar utdata i lokal fil "c:\resultfile.jspå".</span><span class="sxs-lookup"><span data-stu-id="0974d-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="0974d-113">Exempel 2: fråga en BLOB-ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="0974d-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="0974d-114">Det här kommandot får först ett BLOB-objekt för BLOB-ögonblicksbild och frågar sedan BLOB-ögonblicksbilden och visar resultatet include.</span><span class="sxs-lookup"><span data-stu-id="0974d-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="0974d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0974d-115">PARAMETERS</span></span>

### <span data-ttu-id="0974d-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0974d-116">-Blob</span></span>
<span data-ttu-id="0974d-117">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="0974d-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0974d-118">-BlobBaseClient</span></span>
<span data-ttu-id="0974d-119">BlobBaseClient-objekt</span><span class="sxs-lookup"><span data-stu-id="0974d-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="0974d-120">-BlobContainerClient</span></span>
<span data-ttu-id="0974d-121">BlobContainerClient-objekt</span><span class="sxs-lookup"><span data-stu-id="0974d-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0974d-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0974d-123">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0974d-123">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0974d-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0974d-125">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="0974d-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0974d-126">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="0974d-126">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-127">-Container</span><span class="sxs-lookup"><span data-stu-id="0974d-127">-Container</span></span>
<span data-ttu-id="0974d-128">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="0974d-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0974d-129">-Context</span></span>
<span data-ttu-id="0974d-130">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="0974d-130">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0974d-131">-DefaultProfile</span></span>
<span data-ttu-id="0974d-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0974d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0974d-133">-Force</span></span>
<span data-ttu-id="0974d-134">Tvinga att skriva över den befintliga filen.</span><span class="sxs-lookup"><span data-stu-id="0974d-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="0974d-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="0974d-135">-InputTextConfiguration</span></span>
<span data-ttu-id="0974d-136">Den konfiguration som används för att hantera frågeresultatet.</span><span class="sxs-lookup"><span data-stu-id="0974d-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="0974d-137">Skapa konfigurations objekt med New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="0974d-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="0974d-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="0974d-139">Den konfiguration som används för att hantera frågeresultatet.</span><span class="sxs-lookup"><span data-stu-id="0974d-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="0974d-140">Skapa konfigurations objekt med New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="0974d-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0974d-141">-PassThru</span></span>
<span data-ttu-id="0974d-142">Returnera om den angivna blobben har begärts.</span><span class="sxs-lookup"><span data-stu-id="0974d-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="0974d-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0974d-143">-QueryString</span></span>
<span data-ttu-id="0974d-144">Frågesträng, mer information finns i: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="0974d-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="0974d-145">-ResultFile</span></span>
<span data-ttu-id="0974d-146">Lokal fil Sök väg för att spara frågeresultatet.</span><span class="sxs-lookup"><span data-stu-id="0974d-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0974d-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0974d-148">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0974d-148">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0974d-149">-SnapshotTime</span></span>
<span data-ttu-id="0974d-150">Blobb SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0974d-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="0974d-151">-VersionId</span></span>
<span data-ttu-id="0974d-152">Blobb VersionId</span><span class="sxs-lookup"><span data-stu-id="0974d-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0974d-153">-Confirm</span></span>
<span data-ttu-id="0974d-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0974d-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0974d-155">-WhatIf</span></span>
<span data-ttu-id="0974d-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0974d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0974d-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0974d-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0974d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0974d-158">CommonParameters</span></span>
<span data-ttu-id="0974d-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0974d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0974d-160">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0974d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0974d-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0974d-161">INPUTS</span></span>

### <span data-ttu-id="0974d-162">Azure. Storage. blob. specialiserad. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0974d-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="0974d-163">Azure. Storage. blob. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="0974d-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="0974d-164">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0974d-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0974d-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0974d-165">OUTPUTS</span></span>

### <span data-ttu-id="0974d-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0974d-166">System.Boolean</span></span>

## <span data-ttu-id="0974d-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0974d-167">NOTES</span></span>

## <span data-ttu-id="0974d-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0974d-168">RELATED LINKS</span></span>
