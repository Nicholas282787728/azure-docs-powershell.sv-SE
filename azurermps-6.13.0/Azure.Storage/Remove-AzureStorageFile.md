---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 4752612120da1f89729299c41df1b7af78580f92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574094"
---
# <span data-ttu-id="fdcbf-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fdcbf-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="fdcbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdcbf-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcbf-103">Tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdcbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdcbf-104">SYNTAX</span></span>

### <span data-ttu-id="fdcbf-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="fdcbf-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdcbf-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="fdcbf-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdcbf-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="fdcbf-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdcbf-108">Fil</span><span class="sxs-lookup"><span data-stu-id="fdcbf-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcbf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdcbf-109">DESCRIPTION</span></span>
<span data-ttu-id="fdcbf-110">Cmdleten **Remove-AzureStorageFile** tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="fdcbf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdcbf-111">EXAMPLES</span></span>

### <span data-ttu-id="fdcbf-112">Exempel 1: ta bort en fil från en fil resurs</span><span class="sxs-lookup"><span data-stu-id="fdcbf-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="fdcbf-113">Det här kommandot tar bort filen med namnet ContosoFile22 från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="fdcbf-114">Exempel 2: Hämta en fil från en fil resurs med hjälp av ett fil objekt</span><span class="sxs-lookup"><span data-stu-id="fdcbf-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="fdcbf-115">I det här kommandot används cmdleten **Get-AzureStorageShare** för att hämta fil resursen som heter ContosoShare06, och sedan överförs detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fdcbf-116">Det aktuella kommandot tar bort filen som heter ContosoFile22 från ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="fdcbf-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdcbf-117">PARAMETERS</span></span>

### <span data-ttu-id="fdcbf-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdcbf-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fdcbf-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fdcbf-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fdcbf-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fdcbf-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fdcbf-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fdcbf-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fdcbf-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fdcbf-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fdcbf-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fdcbf-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-127">The default value is 10.</span></span>

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

### <span data-ttu-id="fdcbf-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fdcbf-128">-Context</span></span>
<span data-ttu-id="fdcbf-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fdcbf-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fdcbf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcbf-131">-DefaultProfile</span></span>
<span data-ttu-id="fdcbf-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdcbf-133">-Katalog</span><span class="sxs-lookup"><span data-stu-id="fdcbf-133">-Directory</span></span>
<span data-ttu-id="fdcbf-134">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fdcbf-135">Denna cmdlet tar bort en fil i mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdcbf-136">-Fil</span><span class="sxs-lookup"><span data-stu-id="fdcbf-136">-File</span></span>
<span data-ttu-id="fdcbf-137">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="fdcbf-138">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="fdcbf-139">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcbf-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdcbf-140">-PassThru</span></span>
<span data-ttu-id="fdcbf-141">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fdcbf-142">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fdcbf-143">-Path</span><span class="sxs-lookup"><span data-stu-id="fdcbf-143">-Path</span></span>
<span data-ttu-id="fdcbf-144">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-144">Specifies the path of a file.</span></span>
<span data-ttu-id="fdcbf-145">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdcbf-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdcbf-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fdcbf-147">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fdcbf-148">-Dela</span><span class="sxs-lookup"><span data-stu-id="fdcbf-148">-Share</span></span>
<span data-ttu-id="fdcbf-149">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fdcbf-150">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="fdcbf-151">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="fdcbf-152">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-152">This object contains the storage context.</span></span>
<span data-ttu-id="fdcbf-153">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fdcbf-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fdcbf-154">-ShareName</span></span>
<span data-ttu-id="fdcbf-155">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="fdcbf-156">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="fdcbf-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdcbf-157">-Confirm</span></span>
<span data-ttu-id="fdcbf-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcbf-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdcbf-159">-WhatIf</span></span>
<span data-ttu-id="fdcbf-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdcbf-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcbf-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcbf-162">CommonParameters</span></span>
<span data-ttu-id="fdcbf-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdcbf-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcbf-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdcbf-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcbf-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdcbf-165">INPUTS</span></span>

### <span data-ttu-id="fdcbf-166">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fdcbf-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="fdcbf-167">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdcbf-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="fdcbf-168">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fdcbf-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="fdcbf-169">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdcbf-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="fdcbf-170">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="fdcbf-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="fdcbf-171">Parametrar: fil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdcbf-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="fdcbf-172">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdcbf-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fdcbf-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdcbf-173">OUTPUTS</span></span>

### <span data-ttu-id="fdcbf-174">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="fdcbf-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="fdcbf-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdcbf-175">NOTES</span></span>

## <span data-ttu-id="fdcbf-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdcbf-176">RELATED LINKS</span></span>

[<span data-ttu-id="fdcbf-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fdcbf-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="fdcbf-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fdcbf-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="fdcbf-179">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdcbf-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
