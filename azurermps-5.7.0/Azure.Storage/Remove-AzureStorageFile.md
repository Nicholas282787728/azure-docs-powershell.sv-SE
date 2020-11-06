---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 9055f447093a0e10242824e1e2381523e0b0e81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581240"
---
# <span data-ttu-id="b8898-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8898-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="b8898-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8898-102">SYNOPSIS</span></span>
<span data-ttu-id="b8898-103">Tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="b8898-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8898-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8898-104">SYNTAX</span></span>

### <span data-ttu-id="b8898-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="b8898-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8898-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="b8898-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8898-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="b8898-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8898-108">Fil</span><span class="sxs-lookup"><span data-stu-id="b8898-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8898-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8898-109">DESCRIPTION</span></span>
<span data-ttu-id="b8898-110">Cmdleten **Remove-AzureStorageFile** tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="b8898-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="b8898-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8898-111">EXAMPLES</span></span>

### <span data-ttu-id="b8898-112">Exempel 1: ta bort en fil från en fil resurs</span><span class="sxs-lookup"><span data-stu-id="b8898-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="b8898-113">Det här kommandot tar bort filen med namnet ContosoFile22 från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b8898-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="b8898-114">Exempel 2: Hämta en fil från en fil resurs med hjälp av ett fil objekt</span><span class="sxs-lookup"><span data-stu-id="b8898-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="b8898-115">I det här kommandot används cmdleten **Get-AzureStorageShare** för att hämta fil resursen som heter ContosoShare06, och sedan överförs detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b8898-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8898-116">Det aktuella kommandot tar bort filen som heter ContosoFile22 från ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b8898-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="b8898-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8898-117">PARAMETERS</span></span>

### <span data-ttu-id="b8898-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8898-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8898-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="b8898-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8898-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="b8898-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8898-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b8898-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8898-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8898-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b8898-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8898-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b8898-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8898-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="b8898-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8898-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="b8898-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8898-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b8898-127">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b8898-128">-Context</span></span>
<span data-ttu-id="b8898-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="b8898-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b8898-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="b8898-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-131">-Katalog</span><span class="sxs-lookup"><span data-stu-id="b8898-131">-Directory</span></span>
<span data-ttu-id="b8898-132">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8898-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b8898-133">Denna cmdlet tar bort en fil i mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8898-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-134">-Fil</span><span class="sxs-lookup"><span data-stu-id="b8898-134">-File</span></span>
<span data-ttu-id="b8898-135">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8898-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="b8898-136">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b8898-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="b8898-137">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="b8898-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8898-138">-PassThru</span></span>
<span data-ttu-id="b8898-139">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="b8898-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b8898-140">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="b8898-140">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-141">-Path</span><span class="sxs-lookup"><span data-stu-id="b8898-141">-Path</span></span>
<span data-ttu-id="b8898-142">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="b8898-142">Specifies the path of a file.</span></span>
<span data-ttu-id="b8898-143">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b8898-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8898-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8898-145">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="b8898-145">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-146">-Dela</span><span class="sxs-lookup"><span data-stu-id="b8898-146">-Share</span></span>
<span data-ttu-id="b8898-147">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8898-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b8898-148">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8898-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="b8898-149">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b8898-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b8898-150">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="b8898-150">This object contains the storage context.</span></span>
<span data-ttu-id="b8898-151">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="b8898-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b8898-152">-ShareName</span></span>
<span data-ttu-id="b8898-153">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="b8898-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="b8898-154">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8898-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8898-155">-Confirm</span></span>
<span data-ttu-id="b8898-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8898-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8898-157">-WhatIf</span></span>
<span data-ttu-id="b8898-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8898-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8898-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8898-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8898-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8898-160">CommonParameters</span></span>
<span data-ttu-id="b8898-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8898-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8898-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8898-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8898-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8898-163">INPUTS</span></span>

### <span data-ttu-id="b8898-164">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8898-164">IStorageContext</span></span>

<span data-ttu-id="b8898-165">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b8898-165">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b8898-166">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b8898-166">CloudFileDirectory</span></span>

<span data-ttu-id="b8898-167">Parametern ' Directory ' godkänner värdet av typen ' CloudFileDirectory ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b8898-167">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="b8898-168">CloudFile</span><span class="sxs-lookup"><span data-stu-id="b8898-168">CloudFile</span></span>

<span data-ttu-id="b8898-169">Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b8898-169">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="b8898-170">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b8898-170">CloudFileShare</span></span>

<span data-ttu-id="b8898-171">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b8898-171">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="b8898-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8898-172">OUTPUTS</span></span>

## <span data-ttu-id="b8898-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8898-173">NOTES</span></span>

## <span data-ttu-id="b8898-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8898-174">RELATED LINKS</span></span>

[<span data-ttu-id="b8898-175">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8898-175">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="b8898-176">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b8898-176">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b8898-177">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8898-177">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
