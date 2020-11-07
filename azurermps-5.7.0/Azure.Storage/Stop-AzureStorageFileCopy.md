---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
ms.openlocfilehash: ea9902b9bf678ad8f914104022a5ce5a7d04eb07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580459"
---
# <span data-ttu-id="8d28a-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d28a-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="8d28a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d28a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d28a-103">Stoppar en kopierings åtgärd till angiven målfil.</span><span class="sxs-lookup"><span data-stu-id="8d28a-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d28a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d28a-104">SYNTAX</span></span>

### <span data-ttu-id="8d28a-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="8d28a-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d28a-106">Fil</span><span class="sxs-lookup"><span data-stu-id="8d28a-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d28a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d28a-107">DESCRIPTION</span></span>
<span data-ttu-id="8d28a-108">Cmdleten **Stop-AzureStorageFileCopy** slutar kopiera en fil till en målfil.</span><span class="sxs-lookup"><span data-stu-id="8d28a-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="8d28a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d28a-109">EXAMPLES</span></span>

### <span data-ttu-id="8d28a-110">Exempel 1: stoppa en kopiering</span><span class="sxs-lookup"><span data-stu-id="8d28a-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="8d28a-111">Det här kommandot avslutar kopiering av en fil med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="8d28a-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="8d28a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d28a-112">PARAMETERS</span></span>

### <span data-ttu-id="8d28a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d28a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8d28a-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="8d28a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8d28a-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="8d28a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8d28a-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="8d28a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d28a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8d28a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8d28a-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8d28a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8d28a-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8d28a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8d28a-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="8d28a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8d28a-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="8d28a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8d28a-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="8d28a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8d28a-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8d28a-123">-Context</span></span>
<span data-ttu-id="8d28a-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="8d28a-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d28a-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="8d28a-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8d28a-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="8d28a-126">-CopyId</span></span>
<span data-ttu-id="8d28a-127">Anger ID för kopierings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8d28a-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d28a-128">-Fil</span><span class="sxs-lookup"><span data-stu-id="8d28a-128">-File</span></span>
<span data-ttu-id="8d28a-129">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8d28a-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="8d28a-130">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d28a-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="8d28a-131">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="8d28a-131">-FilePath</span></span>
<span data-ttu-id="8d28a-132">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="8d28a-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d28a-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8d28a-133">-Force</span></span>
<span data-ttu-id="8d28a-134">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8d28a-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d28a-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d28a-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8d28a-136">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="8d28a-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8d28a-137">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8d28a-137">-ShareName</span></span>
<span data-ttu-id="8d28a-138">Anger namnet på en resurs.</span><span class="sxs-lookup"><span data-stu-id="8d28a-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="8d28a-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d28a-139">-Confirm</span></span>
<span data-ttu-id="8d28a-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d28a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d28a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d28a-141">-WhatIf</span></span>
<span data-ttu-id="8d28a-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d28a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d28a-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d28a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d28a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d28a-144">CommonParameters</span></span>
<span data-ttu-id="8d28a-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d28a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d28a-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d28a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d28a-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d28a-147">INPUTS</span></span>

### <span data-ttu-id="8d28a-148">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d28a-148">IStorageContext</span></span>

<span data-ttu-id="8d28a-149">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8d28a-149">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8d28a-150">CloudFile</span><span class="sxs-lookup"><span data-stu-id="8d28a-150">CloudFile</span></span>

<span data-ttu-id="8d28a-151">Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8d28a-151">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="8d28a-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d28a-152">OUTPUTS</span></span>

## <span data-ttu-id="8d28a-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d28a-153">NOTES</span></span>

## <span data-ttu-id="8d28a-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d28a-154">RELATED LINKS</span></span>

[<span data-ttu-id="8d28a-155">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8d28a-155">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="8d28a-156">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="8d28a-156">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="8d28a-157">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d28a-157">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8d28a-158">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d28a-158">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)