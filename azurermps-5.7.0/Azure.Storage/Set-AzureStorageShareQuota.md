---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
ms.openlocfilehash: 54636c226d3e8eb7ca9572a8f2e6c95e96981875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758243"
---
# <span data-ttu-id="142a7-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="142a7-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="142a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="142a7-102">SYNOPSIS</span></span>
<span data-ttu-id="142a7-103">Anger lagrings kapaciteten för en resurs.</span><span class="sxs-lookup"><span data-stu-id="142a7-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="142a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="142a7-104">SYNTAX</span></span>

### <span data-ttu-id="142a7-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="142a7-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="142a7-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="142a7-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="142a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="142a7-107">DESCRIPTION</span></span>
<span data-ttu-id="142a7-108">Cmdleten **set-AzureStorageShareQuota** anger lagrings kapaciteten för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="142a7-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="142a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="142a7-109">EXAMPLES</span></span>

### <span data-ttu-id="142a7-110">Exempel 1: Ange lagrings kapaciteten för en resurs</span><span class="sxs-lookup"><span data-stu-id="142a7-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="142a7-111">Det här kommandot anger lagrings kapaciteten för en resurs med namnet ContosoShare01 till 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="142a7-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="142a7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="142a7-112">PARAMETERS</span></span>

### <span data-ttu-id="142a7-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="142a7-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="142a7-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="142a7-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="142a7-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="142a7-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="142a7-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="142a7-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="142a7-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="142a7-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="142a7-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="142a7-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="142a7-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="142a7-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="142a7-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="142a7-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="142a7-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="142a7-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="142a7-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="142a7-122">The default value is 10.</span></span>

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

### <span data-ttu-id="142a7-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="142a7-123">-Context</span></span>
<span data-ttu-id="142a7-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="142a7-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="142a7-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="142a7-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="142a7-126">-Kvot</span><span class="sxs-lookup"><span data-stu-id="142a7-126">-Quota</span></span>
<span data-ttu-id="142a7-127">Anger kvot värde i GB (gigabyte).</span><span class="sxs-lookup"><span data-stu-id="142a7-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142a7-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="142a7-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="142a7-129">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="142a7-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="142a7-130">-Dela</span><span class="sxs-lookup"><span data-stu-id="142a7-130">-Share</span></span>
<span data-ttu-id="142a7-131">Anger ett **CloudFileShare** -objekt som representerar den resurs som den här cmdleten ställer in en kvot för.</span><span class="sxs-lookup"><span data-stu-id="142a7-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="142a7-132">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="142a7-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="142a7-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="142a7-133">-ShareName</span></span>
<span data-ttu-id="142a7-134">Anger namnet på den fil resurs som du vill ange en kvot för.</span><span class="sxs-lookup"><span data-stu-id="142a7-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="142a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142a7-135">CommonParameters</span></span>
<span data-ttu-id="142a7-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="142a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142a7-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="142a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142a7-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="142a7-138">INPUTS</span></span>

### <span data-ttu-id="142a7-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="142a7-139">IStorageContext</span></span>

<span data-ttu-id="142a7-140">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="142a7-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="142a7-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="142a7-141">CloudFileShare</span></span>

<span data-ttu-id="142a7-142">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="142a7-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="142a7-143">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="142a7-143">String</span></span>

<span data-ttu-id="142a7-144">Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="142a7-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="142a7-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="142a7-145">OUTPUTS</span></span>

### <span data-ttu-id="142a7-146">Microsoft. WindowsAzure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="142a7-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="142a7-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="142a7-147">NOTES</span></span>

## <span data-ttu-id="142a7-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="142a7-148">RELATED LINKS</span></span>

[<span data-ttu-id="142a7-149">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="142a7-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="142a7-150">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="142a7-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="142a7-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="142a7-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
