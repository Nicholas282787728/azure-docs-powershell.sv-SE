---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571892"
---
# <span data-ttu-id="6d85b-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6d85b-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="6d85b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d85b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d85b-103">Tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="6d85b-103">Deletes a file.</span></span>

## <span data-ttu-id="6d85b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d85b-104">SYNTAX</span></span>

### <span data-ttu-id="6d85b-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="6d85b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d85b-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="6d85b-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d85b-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="6d85b-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d85b-108">Fil</span><span class="sxs-lookup"><span data-stu-id="6d85b-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d85b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d85b-109">DESCRIPTION</span></span>
<span data-ttu-id="6d85b-110">Cmdleten **Remove-AzureStorageFile** tar bort en fil.</span><span class="sxs-lookup"><span data-stu-id="6d85b-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="6d85b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d85b-111">EXAMPLES</span></span>

### <span data-ttu-id="6d85b-112">Exempel 1: ta bort en fil från en fil resurs</span><span class="sxs-lookup"><span data-stu-id="6d85b-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="6d85b-113">Det här kommandot tar bort filen med namnet ContosoFile22 från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6d85b-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="6d85b-114">Exempel 2: Hämta en fil från en fil resurs med hjälp av ett fil objekt</span><span class="sxs-lookup"><span data-stu-id="6d85b-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="6d85b-115">I det här kommandot används cmdleten **Get-AzureStorageShare** för att hämta fil resursen som heter ContosoShare06, och sedan överförs detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="6d85b-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6d85b-116">Det aktuella kommandot tar bort filen som heter ContosoFile22 från ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6d85b-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="6d85b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d85b-117">PARAMETERS</span></span>

### <span data-ttu-id="6d85b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d85b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6d85b-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="6d85b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6d85b-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="6d85b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6d85b-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="6d85b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6d85b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6d85b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6d85b-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6d85b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6d85b-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6d85b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6d85b-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="6d85b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6d85b-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="6d85b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6d85b-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="6d85b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="6d85b-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6d85b-128">-Context</span></span>
<span data-ttu-id="6d85b-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="6d85b-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6d85b-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="6d85b-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6d85b-131">-Katalog</span><span class="sxs-lookup"><span data-stu-id="6d85b-131">-Directory</span></span>
<span data-ttu-id="6d85b-132">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d85b-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6d85b-133">Denna cmdlet tar bort en fil i mappen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6d85b-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d85b-134">-Fil</span><span class="sxs-lookup"><span data-stu-id="6d85b-134">-File</span></span>
<span data-ttu-id="6d85b-135">Anger en fil som ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d85b-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="6d85b-136">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6d85b-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="6d85b-137">För att hämta ett **CloudFile** -objekt, Använd cmdleten Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="6d85b-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="6d85b-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d85b-138">-PassThru</span></span>
<span data-ttu-id="6d85b-139">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="6d85b-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6d85b-140">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="6d85b-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6d85b-141">-Path</span><span class="sxs-lookup"><span data-stu-id="6d85b-141">-Path</span></span>
<span data-ttu-id="6d85b-142">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="6d85b-142">Specifies the path of a file.</span></span>
<span data-ttu-id="6d85b-143">Denna cmdlet tar bort filen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6d85b-143">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d85b-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d85b-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6d85b-145">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="6d85b-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6d85b-146">-Dela</span><span class="sxs-lookup"><span data-stu-id="6d85b-146">-Share</span></span>
<span data-ttu-id="6d85b-147">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d85b-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6d85b-148">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6d85b-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="6d85b-149">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6d85b-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="6d85b-150">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="6d85b-150">This object contains the storage context.</span></span>
<span data-ttu-id="6d85b-151">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="6d85b-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="6d85b-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6d85b-152">-ShareName</span></span>
<span data-ttu-id="6d85b-153">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="6d85b-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="6d85b-154">Denna cmdlet tar bort filen i resursen dela den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6d85b-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="6d85b-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d85b-155">-Confirm</span></span>
<span data-ttu-id="6d85b-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d85b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d85b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d85b-157">-WhatIf</span></span>
<span data-ttu-id="6d85b-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d85b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d85b-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d85b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d85b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d85b-160">CommonParameters</span></span>
<span data-ttu-id="6d85b-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d85b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d85b-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d85b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d85b-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d85b-163">INPUTS</span></span>

## <span data-ttu-id="6d85b-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d85b-164">OUTPUTS</span></span>

## <span data-ttu-id="6d85b-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d85b-165">NOTES</span></span>

## <span data-ttu-id="6d85b-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d85b-166">RELATED LINKS</span></span>

[<span data-ttu-id="6d85b-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6d85b-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="6d85b-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d85b-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="6d85b-169">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d85b-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
