---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: cca517246f548deb64cba1b4bc737de88628e7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920760"
---
# <span data-ttu-id="b0604-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b0604-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="b0604-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0604-102">SYNOPSIS</span></span>
<span data-ttu-id="b0604-103">Stänger fil referenser till en fil resurs, en fil katalog eller en fil.</span><span class="sxs-lookup"><span data-stu-id="b0604-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="b0604-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0604-104">SYNTAX</span></span>

### <span data-ttu-id="b0604-105">ShareNameCloseAll (standard)</span><span class="sxs-lookup"><span data-stu-id="b0604-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0604-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="b0604-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0604-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="b0604-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0604-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="b0604-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0604-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="b0604-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0604-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="b0604-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0604-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0604-111">DESCRIPTION</span></span>
<span data-ttu-id="b0604-112">Cmdleten **Close-AzStorageFileHandle** stänger fil referenser till en fil resurs eller fil katalog eller en fil.</span><span class="sxs-lookup"><span data-stu-id="b0604-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="b0604-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0604-113">EXAMPLES</span></span>

### <span data-ttu-id="b0604-114">Exempel 1: listar alla fil resurser för det aktuella lagrings kontot och Stäng alla fil referenser för fil resurserna rekursivt.</span><span class="sxs-lookup"><span data-stu-id="b0604-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="b0604-115">Det här kommandot listar alla fil resurser för det aktuella lagrings kontot och stänger alla fil handtag i fil resurserna rekursivt..</span><span class="sxs-lookup"><span data-stu-id="b0604-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="b0604-116">Exempel 2: Stäng alla fil handtag på en fil katalog rekursivt och visa det stängda fil handtaget</span><span class="sxs-lookup"><span data-stu-id="b0604-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="b0604-117">Det här kommandot stänger alla fil handtag på en fil katalog och visar antalet stängda fil referenser.</span><span class="sxs-lookup"><span data-stu-id="b0604-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="b0604-118">Exempel 3: Stäng alla fil referenser som öppnats för 1 dag sedan på en fil katalog</span><span class="sxs-lookup"><span data-stu-id="b0604-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="b0604-119">Det här kommandot listar alla fil referenser i en fil katalog rekursivt, filtrerar bort handtagen som öppnats 1 dag sedan och sedan stänger dem.</span><span class="sxs-lookup"><span data-stu-id="b0604-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="b0604-120">Exempel 4: Stäng alla fil handtag på en fil</span><span class="sxs-lookup"><span data-stu-id="b0604-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="b0604-121">Det här kommandot stänger alla fil handtag på en fil.</span><span class="sxs-lookup"><span data-stu-id="b0604-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="b0604-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0604-122">PARAMETERS</span></span>

### <span data-ttu-id="b0604-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0604-123">-AsJob</span></span>
<span data-ttu-id="b0604-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0604-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0604-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0604-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b0604-126">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b0604-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="b0604-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="b0604-127">-CloseAll</span></span>
<span data-ttu-id="b0604-128">Tvinga alla fil referenser att stängas.</span><span class="sxs-lookup"><span data-stu-id="b0604-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b0604-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b0604-130">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="b0604-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b0604-131">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b0604-131">The default value is 10.</span></span>

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

### <span data-ttu-id="b0604-132">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b0604-132">-Context</span></span>
<span data-ttu-id="b0604-133">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="b0604-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0604-134">-DefaultProfile</span></span>
<span data-ttu-id="b0604-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0604-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0604-136">-Katalog</span><span class="sxs-lookup"><span data-stu-id="b0604-136">-Directory</span></span>
<span data-ttu-id="b0604-137">CloudFileDirectory-objektet angav bas mappen där filerna/katalogerna listas.</span><span class="sxs-lookup"><span data-stu-id="b0604-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-138">-Fil</span><span class="sxs-lookup"><span data-stu-id="b0604-138">-File</span></span>
<span data-ttu-id="b0604-139">CloudFile-objektet angav filen för att stänga handtaget.</span><span class="sxs-lookup"><span data-stu-id="b0604-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="b0604-140">-FileHandle</span></span>
<span data-ttu-id="b0604-141">Fil handtaget för att stänga.</span><span class="sxs-lookup"><span data-stu-id="b0604-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0604-142">-PassThru</span></span>
<span data-ttu-id="b0604-143">Returnera antalet stängda fil referenser.</span><span class="sxs-lookup"><span data-stu-id="b0604-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="b0604-144">-Path</span><span class="sxs-lookup"><span data-stu-id="b0604-144">-Path</span></span>
<span data-ttu-id="b0604-145">Sökväg till en befintlig fil/katalog.</span><span class="sxs-lookup"><span data-stu-id="b0604-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-146">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="b0604-146">-Recursive</span></span>
<span data-ttu-id="b0604-147">List handtag rekursivt.</span><span class="sxs-lookup"><span data-stu-id="b0604-147">List handles Recursively.</span></span>
<span data-ttu-id="b0604-148">Fungerar bara på fil katalogen.</span><span class="sxs-lookup"><span data-stu-id="b0604-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0604-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b0604-150">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b0604-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="b0604-151">-Dela</span><span class="sxs-lookup"><span data-stu-id="b0604-151">-Share</span></span>
<span data-ttu-id="b0604-152">CloudFileShare-objekt indikerade i vilken plats filerna/katalogerna listas.</span><span class="sxs-lookup"><span data-stu-id="b0604-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b0604-153">-ShareName</span></span>
<span data-ttu-id="b0604-154">Namnet på fil resursen där filerna/katalogerna visas.</span><span class="sxs-lookup"><span data-stu-id="b0604-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0604-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0604-155">-Confirm</span></span>
<span data-ttu-id="b0604-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0604-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0604-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0604-157">-WhatIf</span></span>
<span data-ttu-id="b0604-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0604-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0604-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0604-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0604-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0604-160">CommonParameters</span></span>
<span data-ttu-id="b0604-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0604-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0604-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0604-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0604-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0604-163">INPUTS</span></span>

### <span data-ttu-id="b0604-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b0604-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b0604-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b0604-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b0604-166">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0604-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0604-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0604-167">OUTPUTS</span></span>

### <span data-ttu-id="b0604-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="b0604-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="b0604-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0604-169">NOTES</span></span>

## <span data-ttu-id="b0604-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0604-170">RELATED LINKS</span></span>
