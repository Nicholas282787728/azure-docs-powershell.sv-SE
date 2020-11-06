---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 84192a4715087d5ae896067e02ab07ef27574410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573112"
---
# <span data-ttu-id="8d862-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d862-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="8d862-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d862-102">SYNOPSIS</span></span>
<span data-ttu-id="8d862-103">Överför innehållet i en fil.</span><span class="sxs-lookup"><span data-stu-id="8d862-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d862-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d862-104">SYNTAX</span></span>

### <span data-ttu-id="8d862-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="8d862-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d862-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="8d862-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d862-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="8d862-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d862-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d862-108">DESCRIPTION</span></span>
<span data-ttu-id="8d862-109">Cmdleten **set-AzureStorageFileContent** laddar upp innehållet i en fil till en fil på en angiven resurs.</span><span class="sxs-lookup"><span data-stu-id="8d862-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="8d862-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d862-110">EXAMPLES</span></span>

### <span data-ttu-id="8d862-111">Exempel 1: Ladda upp en fil i den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="8d862-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="8d862-112">Det här kommandot laddar upp en fil med namnet DataFile37 i den aktuella mappen som en fil med namnet CurrentDataFile i mappen som heter ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="8d862-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="8d862-113">Exempel 2: Ladda upp alla filer i den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="8d862-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="8d862-114">I det här exemplet används flera vanliga Windows PowerShell-cmdlets och den aktuella cmdleten för att ladda upp alla filer från den aktuella mappen till rotmappen med ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8d862-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="8d862-115">Det första kommandot får namnet på den aktuella mappen och lagrar det i $CurrentFolder variabeln.</span><span class="sxs-lookup"><span data-stu-id="8d862-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="8d862-116">Det andra kommandot använder cmdleten **Get-AzureStorageShare** för att hämta fil resursen med namnet ContosoShare06 och lagrar den sedan i $container variabel.</span><span class="sxs-lookup"><span data-stu-id="8d862-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8d862-117">Det sista kommandot får innehållet i den aktuella mappen och skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="8d862-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d862-118">Denna cmdlet filtrerar bort objekt som inte är filer och överför sedan filerna till ForEach-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d862-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="8d862-119">Denna cmdlet kör ett skript block för varje fil som skapar en lämplig sökväg för den och använder sedan den aktuella cmdleten för att ladda upp filen.</span><span class="sxs-lookup"><span data-stu-id="8d862-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="8d862-120">Resultatet har samma namn och samma relativa position som de andra filerna som det här exemplet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="8d862-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="8d862-121">Om du vill ha mer information om skript block skriver du `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="8d862-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="8d862-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d862-122">PARAMETERS</span></span>

### <span data-ttu-id="8d862-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d862-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8d862-124">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="8d862-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8d862-125">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="8d862-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8d862-126">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="8d862-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d862-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8d862-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8d862-128">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8d862-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8d862-129">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8d862-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8d862-130">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="8d862-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8d862-131">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="8d862-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8d862-132">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="8d862-132">The default value is 10.</span></span>

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

### <span data-ttu-id="8d862-133">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8d862-133">-Context</span></span>
<span data-ttu-id="8d862-134">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="8d862-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d862-135">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="8d862-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8d862-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d862-136">-DefaultProfile</span></span>
<span data-ttu-id="8d862-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d862-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d862-138">-Katalog</span><span class="sxs-lookup"><span data-stu-id="8d862-138">-Directory</span></span>
<span data-ttu-id="8d862-139">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8d862-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8d862-140">Denna cmdlet laddar upp filen till mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8d862-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="8d862-141">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="8d862-141">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="8d862-142">Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="8d862-142">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d862-143">-Force</span><span class="sxs-lookup"><span data-stu-id="8d862-143">-Force</span></span>
<span data-ttu-id="8d862-144">Anger att denna cmdlet skriver över en befintlig Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="8d862-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="8d862-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d862-145">-PassThru</span></span>
<span data-ttu-id="8d862-146">Anger att den här cmdleten returnerar **AzureStorageFile** -objektet som skapas eller upprättas.</span><span class="sxs-lookup"><span data-stu-id="8d862-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="8d862-147">-Path</span><span class="sxs-lookup"><span data-stu-id="8d862-147">-Path</span></span>
<span data-ttu-id="8d862-148">Anger sökvägen till en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="8d862-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="8d862-149">Denna cmdlet laddar upp innehåll till filen som den här parametern anger, eller till en fil i mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8d862-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="8d862-150">Om du anger en mapp skapar denna cmdlet en fil med samma namn som käll filen.</span><span class="sxs-lookup"><span data-stu-id="8d862-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="8d862-151">Om du anger en sökväg till en fil som inte finns skapar den här cmdleten filen och sparar innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="8d862-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="8d862-152">Om du anger en fil som redan finns och du anger parametern _Force_ skriver denna cmdlet över innehållet i filen.</span><span class="sxs-lookup"><span data-stu-id="8d862-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="8d862-153">Om du anger en fil som redan finns och du inte anger _Force_ , gör denna cmdlet ingen ändring och returnerar ett fel.</span><span class="sxs-lookup"><span data-stu-id="8d862-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="8d862-154">Om du anger en sökväg till en mapp som inte finns görs ingen ändring av denna cmdlet och ett fel returneras.</span><span class="sxs-lookup"><span data-stu-id="8d862-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="8d862-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d862-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8d862-156">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="8d862-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8d862-157">-Dela</span><span class="sxs-lookup"><span data-stu-id="8d862-157">-Share</span></span>
<span data-ttu-id="8d862-158">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8d862-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8d862-159">Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8d862-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="8d862-160">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="8d862-160">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="8d862-161">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="8d862-161">This object contains the storage context.</span></span>
<span data-ttu-id="8d862-162">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="8d862-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d862-163">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8d862-163">-ShareName</span></span>
<span data-ttu-id="8d862-164">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="8d862-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="8d862-165">Denna cmdlet laddas upp till en fil i fil resursen den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8d862-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="8d862-166">-Källa</span><span class="sxs-lookup"><span data-stu-id="8d862-166">-Source</span></span>
<span data-ttu-id="8d862-167">Anger den källfil som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="8d862-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="8d862-168">Om du anger en fil som inte finns returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="8d862-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d862-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d862-169">-Confirm</span></span>
<span data-ttu-id="8d862-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d862-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d862-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d862-171">-WhatIf</span></span>
<span data-ttu-id="8d862-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d862-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d862-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d862-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d862-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d862-174">CommonParameters</span></span>
<span data-ttu-id="8d862-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d862-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d862-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d862-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d862-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d862-177">INPUTS</span></span>

### <span data-ttu-id="8d862-178">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8d862-178">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="8d862-179">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d862-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="8d862-180">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8d862-180">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="8d862-181">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d862-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="8d862-182">System. String</span><span class="sxs-lookup"><span data-stu-id="8d862-182">System.String</span></span>

### <span data-ttu-id="8d862-183">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d862-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d862-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d862-184">OUTPUTS</span></span>

### <span data-ttu-id="8d862-185">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="8d862-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="8d862-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d862-186">NOTES</span></span>

## <span data-ttu-id="8d862-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d862-187">RELATED LINKS</span></span>

[<span data-ttu-id="8d862-188">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8d862-188">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="8d862-189">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8d862-189">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="8d862-190">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d862-190">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
