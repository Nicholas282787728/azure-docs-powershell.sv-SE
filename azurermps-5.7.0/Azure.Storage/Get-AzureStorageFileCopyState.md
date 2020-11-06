---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
ms.openlocfilehash: bd88b82a358e10de8a738382e29bdb785f89c1e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577355"
---
# <span data-ttu-id="05b8d-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="05b8d-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="05b8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="05b8d-103">Hämtar tillståndet för en kopiering.</span><span class="sxs-lookup"><span data-stu-id="05b8d-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05b8d-104">SYNTAX</span></span>

### <span data-ttu-id="05b8d-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="05b8d-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="05b8d-106">Fil</span><span class="sxs-lookup"><span data-stu-id="05b8d-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="05b8d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05b8d-107">DESCRIPTION</span></span>
<span data-ttu-id="05b8d-108">Cmdleten **Get-AzureStorageFileCopyState** får statusen för en Azure Storage File Copy-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="05b8d-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="05b8d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05b8d-109">EXAMPLES</span></span>

### <span data-ttu-id="05b8d-110">Exempel 1: Hämta kopierings status efter fil namn</span><span class="sxs-lookup"><span data-stu-id="05b8d-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="05b8d-111">Det här kommandot får statusen för kopierings åtgärden för en fil som har det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="05b8d-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="05b8d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05b8d-112">PARAMETERS</span></span>

### <span data-ttu-id="05b8d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="05b8d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="05b8d-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="05b8d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="05b8d-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="05b8d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="05b8d-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="05b8d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="05b8d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="05b8d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="05b8d-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="05b8d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="05b8d-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="05b8d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="05b8d-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="05b8d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="05b8d-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="05b8d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="05b8d-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="05b8d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="05b8d-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="05b8d-123">-Context</span></span>
<span data-ttu-id="05b8d-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="05b8d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="05b8d-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="05b8d-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="05b8d-126">-Fil</span><span class="sxs-lookup"><span data-stu-id="05b8d-126">-File</span></span>
<span data-ttu-id="05b8d-127">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="05b8d-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="05b8d-128">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b8d-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="05b8d-129">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="05b8d-129">-FilePath</span></span>
<span data-ttu-id="05b8d-130">Anger sökvägen till filen i förhållande till en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="05b8d-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="05b8d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="05b8d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="05b8d-132">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="05b8d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="05b8d-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="05b8d-133">-ShareName</span></span>
<span data-ttu-id="05b8d-134">Anger namnet på en resurs.</span><span class="sxs-lookup"><span data-stu-id="05b8d-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="05b8d-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="05b8d-135">-WaitForComplete</span></span>
<span data-ttu-id="05b8d-136">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="05b8d-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="05b8d-137">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="05b8d-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="05b8d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b8d-138">CommonParameters</span></span>
<span data-ttu-id="05b8d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b8d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b8d-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b8d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b8d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05b8d-141">INPUTS</span></span>

### <span data-ttu-id="05b8d-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="05b8d-142">IStorageContext</span></span>

<span data-ttu-id="05b8d-143">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="05b8d-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="05b8d-144">CloudFile</span><span class="sxs-lookup"><span data-stu-id="05b8d-144">CloudFile</span></span>

<span data-ttu-id="05b8d-145">Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="05b8d-145">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="05b8d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05b8d-146">OUTPUTS</span></span>

## <span data-ttu-id="05b8d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05b8d-147">NOTES</span></span>

## <span data-ttu-id="05b8d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05b8d-148">RELATED LINKS</span></span>

[<span data-ttu-id="05b8d-149">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="05b8d-149">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="05b8d-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="05b8d-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="05b8d-151">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="05b8d-151">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="05b8d-152">Stopp-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="05b8d-152">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
