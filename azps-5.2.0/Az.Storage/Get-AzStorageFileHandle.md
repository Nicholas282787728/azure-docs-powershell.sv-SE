---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404208"
---
# <span data-ttu-id="2bf84-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2bf84-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="2bf84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bf84-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf84-103">Visar en lista över fil referenser till en fil resurs, en fil katalog eller en fil.</span><span class="sxs-lookup"><span data-stu-id="2bf84-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="2bf84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bf84-104">SYNTAX</span></span>

### <span data-ttu-id="2bf84-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="2bf84-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2bf84-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="2bf84-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2bf84-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="2bf84-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2bf84-108">Fil</span><span class="sxs-lookup"><span data-stu-id="2bf84-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="2bf84-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bf84-109">DESCRIPTION</span></span>
<span data-ttu-id="2bf84-110">Cmdleten **Get-AzStorageFileHandle** visar fil referenser till en fil resurs eller fil katalog eller en fil.</span><span class="sxs-lookup"><span data-stu-id="2bf84-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="2bf84-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bf84-111">EXAMPLES</span></span>

### <span data-ttu-id="2bf84-112">Exempel 1: lista alla fil referenser på en fil resurs rekursivt och sortera efter ClientIp och opentime</span><span class="sxs-lookup"><span data-stu-id="2bf84-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="2bf84-113">Det här kommandot visar fil handtag på en fil resurs och sorterar utdata efter ClientIp, sedan efter opentime.</span><span class="sxs-lookup"><span data-stu-id="2bf84-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="2bf84-114">Exempel 2: lista de första 2 fil handtagen på en fil katalog rekursivt</span><span class="sxs-lookup"><span data-stu-id="2bf84-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="2bf84-115">Det här kommandot listar de första 2 fil handtagen på en fil katalog rekursivt.</span><span class="sxs-lookup"><span data-stu-id="2bf84-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="2bf84-116">Exempel 3: lista tredje till de 6 i fil handtagen på en fil</span><span class="sxs-lookup"><span data-stu-id="2bf84-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="2bf84-117">Det här kommandot visar den tredje till de 6: a fil handtagen på en fil.</span><span class="sxs-lookup"><span data-stu-id="2bf84-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="2bf84-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bf84-118">PARAMETERS</span></span>

### <span data-ttu-id="2bf84-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2bf84-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2bf84-120">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="2bf84-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="2bf84-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2bf84-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2bf84-122">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="2bf84-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="2bf84-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="2bf84-123">The default value is 10.</span></span>

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

### <span data-ttu-id="2bf84-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2bf84-124">-Context</span></span>
<span data-ttu-id="2bf84-125">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="2bf84-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf84-126">-DefaultProfile</span></span>
<span data-ttu-id="2bf84-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf84-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf84-128">-Katalog</span><span class="sxs-lookup"><span data-stu-id="2bf84-128">-Directory</span></span>
<span data-ttu-id="2bf84-129">CloudFileDirectory-objektet angav bas mappen där filerna/katalogerna listas.</span><span class="sxs-lookup"><span data-stu-id="2bf84-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-130">-Fil</span><span class="sxs-lookup"><span data-stu-id="2bf84-130">-File</span></span>
<span data-ttu-id="2bf84-131">CloudFile-objektet angav filens fil handtag.</span><span class="sxs-lookup"><span data-stu-id="2bf84-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-132">-Path</span><span class="sxs-lookup"><span data-stu-id="2bf84-132">-Path</span></span>
<span data-ttu-id="2bf84-133">Sökväg till en befintlig fil/katalog.</span><span class="sxs-lookup"><span data-stu-id="2bf84-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-134">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="2bf84-134">-Recursive</span></span>
<span data-ttu-id="2bf84-135">List handtag rekursivt.</span><span class="sxs-lookup"><span data-stu-id="2bf84-135">List handles Recursively.</span></span>
<span data-ttu-id="2bf84-136">Fungerar bara på fil katalogen.</span><span class="sxs-lookup"><span data-stu-id="2bf84-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="2bf84-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2bf84-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2bf84-138">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="2bf84-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="2bf84-139">-Dela</span><span class="sxs-lookup"><span data-stu-id="2bf84-139">-Share</span></span>
<span data-ttu-id="2bf84-140">CloudFileShare-objekt indikerade i vilken plats filerna/katalogerna listas.</span><span class="sxs-lookup"><span data-stu-id="2bf84-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2bf84-141">-ShareName</span></span>
<span data-ttu-id="2bf84-142">Namnet på fil resursen där filerna/katalogerna visas.</span><span class="sxs-lookup"><span data-stu-id="2bf84-142">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2bf84-143">-IncludeTotalCount</span></span>
<span data-ttu-id="2bf84-144">Rapporterar antalet objekt i data uppsättningen (ett heltal) följt av objekten.</span><span class="sxs-lookup"><span data-stu-id="2bf84-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="2bf84-145">Om cmdleten inte kan avgöra det totala antalet returnerar den värdet "okänt total count".</span><span class="sxs-lookup"><span data-stu-id="2bf84-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="2bf84-146">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="2bf84-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="2bf84-147">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="2bf84-147">-Skip</span></span>
<span data-ttu-id="2bf84-148">Ignorerar de första ' N' '-objekten och hämtar sedan de återstående objekten.</span><span class="sxs-lookup"><span data-stu-id="2bf84-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-149">-Först</span><span class="sxs-lookup"><span data-stu-id="2bf84-149">-First</span></span>
<span data-ttu-id="2bf84-150">Hämtar endast de första ' N' '-objekten.</span><span class="sxs-lookup"><span data-stu-id="2bf84-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf84-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf84-151">CommonParameters</span></span>
<span data-ttu-id="2bf84-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf84-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf84-153">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf84-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf84-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bf84-154">INPUTS</span></span>

### <span data-ttu-id="2bf84-155">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2bf84-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2bf84-156">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2bf84-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="2bf84-157">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2bf84-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2bf84-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bf84-158">OUTPUTS</span></span>

### <span data-ttu-id="2bf84-159">Microsoft. Azure. Storage. File. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="2bf84-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="2bf84-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bf84-160">NOTES</span></span>

## <span data-ttu-id="2bf84-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bf84-161">RELATED LINKS</span></span>
