---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403299"
---
# <span data-ttu-id="65ce6-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="65ce6-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="65ce6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="65ce6-103">Överför innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="65ce6-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="65ce6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65ce6-104">SYNTAX</span></span>

### <span data-ttu-id="65ce6-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="65ce6-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="65ce6-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="65ce6-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="65ce6-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="65ce6-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="65ce6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65ce6-108">DESCRIPTION</span></span>
<span data-ttu-id="65ce6-109">Cmdleten **set-AzStorageFileContent** laddar upp innehållet i en fil till en fil på en angiven resurs.</span><span class="sxs-lookup"><span data-stu-id="65ce6-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="65ce6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65ce6-110">EXAMPLES</span></span>

### <span data-ttu-id="65ce6-111">Exempel 1: Ladda upp en fil i den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="65ce6-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="65ce6-112">Det här kommandot laddar upp en fil med namnet DataFile37 i den aktuella mappen som en fil med namnet CurrentDataFile i mappen som heter ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="65ce6-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="65ce6-113">Exempel 2: Ladda upp alla filer i den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="65ce6-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="65ce6-114">I det här exemplet används flera vanliga Windows PowerShell-cmdlets och den aktuella cmdleten för att ladda upp alla filer från den aktuella mappen till rotmappen med ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="65ce6-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="65ce6-115">Det första kommandot får namnet på den aktuella mappen och lagrar det i $CurrentFolder variabeln.</span><span class="sxs-lookup"><span data-stu-id="65ce6-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="65ce6-116">Det andra kommandot använder cmdleten **Get-AzStorageShare** för att hämta fil resursen med namnet ContosoShare06 och lagrar den sedan i $container variabel.</span><span class="sxs-lookup"><span data-stu-id="65ce6-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="65ce6-117">Det sista kommandot får innehållet i den aktuella mappen och skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="65ce6-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65ce6-118">Denna cmdlet filtrerar bort objekt som inte är filer och överför sedan filerna till ForEach-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ce6-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="65ce6-119">Denna cmdlet kör ett skript block för varje fil som skapar en lämplig sökväg för den och använder sedan den aktuella cmdleten för att ladda upp filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="65ce6-120">Resultatet har samma namn och samma relativa position som de andra filerna som det här exemplet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="65ce6-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="65ce6-121">Om du vill ha mer information om skript block skriver du `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="65ce6-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="65ce6-122">Exempel 3: Ladda upp en lokal fil till en Azure-fil och perserve den lokala filen SMB-egenskaper (fil Attributtes, fil skapande tid, fil senaste skrivning) i Azure-filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="65ce6-123">Det här exemplet laddar upp en lokal fil till en Azure-fil och perserves de lokala filerna SMB-egenskaper (fil Attributtes, fil skapande tid, senaste skrivnings tid) i Azure-filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="65ce6-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65ce6-124">PARAMETERS</span></span>

### <span data-ttu-id="65ce6-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65ce6-125">-AsJob</span></span>
<span data-ttu-id="65ce6-126">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="65ce6-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="65ce6-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65ce6-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="65ce6-128">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="65ce6-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65ce6-129">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65ce6-130">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="65ce6-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65ce6-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="65ce6-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="65ce6-132">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="65ce6-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="65ce6-133">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="65ce6-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="65ce6-134">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="65ce6-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="65ce6-135">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="65ce6-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="65ce6-136">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="65ce6-136">The default value is 10.</span></span>

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

### <span data-ttu-id="65ce6-137">-Kontext</span><span class="sxs-lookup"><span data-stu-id="65ce6-137">-Context</span></span>
<span data-ttu-id="65ce6-138">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="65ce6-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="65ce6-139">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="65ce6-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="65ce6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ce6-140">-DefaultProfile</span></span>
<span data-ttu-id="65ce6-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65ce6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ce6-142">-Katalog</span><span class="sxs-lookup"><span data-stu-id="65ce6-142">-Directory</span></span>
<span data-ttu-id="65ce6-143">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="65ce6-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="65ce6-144">Denna cmdlet laddar upp filen till mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="65ce6-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="65ce6-145">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="65ce6-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="65ce6-146">Du kan också använda Get-AzStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="65ce6-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="65ce6-147">-Force</span><span class="sxs-lookup"><span data-stu-id="65ce6-147">-Force</span></span>
<span data-ttu-id="65ce6-148">Anger att denna cmdlet skriver över en befintlig Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="65ce6-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="65ce6-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65ce6-149">-PassThru</span></span>
<span data-ttu-id="65ce6-150">Anger att den här cmdleten returnerar **AzureStorageFile** -objektet som skapas eller upprättas.</span><span class="sxs-lookup"><span data-stu-id="65ce6-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="65ce6-151">-Path</span><span class="sxs-lookup"><span data-stu-id="65ce6-151">-Path</span></span>
<span data-ttu-id="65ce6-152">Anger sökvägen till en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="65ce6-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="65ce6-153">Denna cmdlet laddar upp innehåll till filen som den här parametern anger, eller till en fil i mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="65ce6-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="65ce6-154">Om du anger en mapp skapar denna cmdlet en fil med samma namn som käll filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="65ce6-155">Om du anger en sökväg till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="65ce6-156">Om du anger en fil som redan finns och du anger parametern _Force_ skriver denna cmdlet över innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="65ce6-157">Om du anger en fil som redan finns och du inte anger _Force_, gör denna cmdlet ingen ändring och returnerar ett fel.</span><span class="sxs-lookup"><span data-stu-id="65ce6-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="65ce6-158">Om du anger en sökväg till en mapp som inte finns görs ingen ändring av denna cmdlet och ett fel returneras.</span><span class="sxs-lookup"><span data-stu-id="65ce6-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ce6-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="65ce6-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="65ce6-160">Behåll käll filens SMB-egenskaper (fil Attributtes, fil skapande tid, senaste skrivnings tid) i målfil.</span><span class="sxs-lookup"><span data-stu-id="65ce6-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="65ce6-161">Denna parameter är endast tillgänglig i Windows.</span><span class="sxs-lookup"><span data-stu-id="65ce6-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="65ce6-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65ce6-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="65ce6-163">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="65ce6-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="65ce6-164">-Dela</span><span class="sxs-lookup"><span data-stu-id="65ce6-164">-Share</span></span>
<span data-ttu-id="65ce6-165">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="65ce6-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="65ce6-166">Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="65ce6-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="65ce6-167">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="65ce6-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="65ce6-168">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="65ce6-168">This object contains the storage context.</span></span>
<span data-ttu-id="65ce6-169">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="65ce6-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="65ce6-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="65ce6-170">-ShareName</span></span>
<span data-ttu-id="65ce6-171">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="65ce6-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="65ce6-172">Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="65ce6-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="65ce6-173">-Källa</span><span class="sxs-lookup"><span data-stu-id="65ce6-173">-Source</span></span>
<span data-ttu-id="65ce6-174">Anger den källfil som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="65ce6-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="65ce6-175">Om du anger en fil som inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="65ce6-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ce6-176">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65ce6-176">-Confirm</span></span>
<span data-ttu-id="65ce6-177">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65ce6-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ce6-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ce6-178">-WhatIf</span></span>
<span data-ttu-id="65ce6-179">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65ce6-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ce6-180">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65ce6-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ce6-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ce6-181">CommonParameters</span></span>
<span data-ttu-id="65ce6-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ce6-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ce6-183">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ce6-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ce6-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65ce6-184">INPUTS</span></span>

### <span data-ttu-id="65ce6-185">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="65ce6-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="65ce6-186">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="65ce6-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="65ce6-187">System. String</span><span class="sxs-lookup"><span data-stu-id="65ce6-187">System.String</span></span>

### <span data-ttu-id="65ce6-188">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65ce6-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65ce6-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65ce6-189">OUTPUTS</span></span>

### <span data-ttu-id="65ce6-190">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="65ce6-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="65ce6-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65ce6-191">NOTES</span></span>

## <span data-ttu-id="65ce6-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65ce6-192">RELATED LINKS</span></span>

[<span data-ttu-id="65ce6-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="65ce6-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="65ce6-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="65ce6-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="65ce6-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="65ce6-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
