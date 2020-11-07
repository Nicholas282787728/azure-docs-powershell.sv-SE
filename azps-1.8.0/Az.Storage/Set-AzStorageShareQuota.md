---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: e260ab25d2028fd970bf1c69e63a23e7dc190ce6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746254"
---
# <span data-ttu-id="4fb69-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4fb69-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="4fb69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fb69-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb69-103">Anger lagrings kapaciteten för en resurs.</span><span class="sxs-lookup"><span data-stu-id="4fb69-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="4fb69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fb69-104">SYNTAX</span></span>

### <span data-ttu-id="4fb69-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="4fb69-105">ShareName</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4fb69-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="4fb69-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fb69-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fb69-107">DESCRIPTION</span></span>
<span data-ttu-id="4fb69-108">Cmdleten **set-AzStorageShareQuota** anger lagrings kapaciteten för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="4fb69-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="4fb69-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fb69-109">EXAMPLES</span></span>

### <span data-ttu-id="4fb69-110">Exempel 1: Ange lagrings kapaciteten för en resurs</span><span class="sxs-lookup"><span data-stu-id="4fb69-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="4fb69-111">Det här kommandot anger lagrings kapaciteten för en resurs med namnet ContosoShare01 till 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="4fb69-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="4fb69-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fb69-112">PARAMETERS</span></span>

### <span data-ttu-id="4fb69-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fb69-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4fb69-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="4fb69-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4fb69-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="4fb69-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4fb69-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="4fb69-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4fb69-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4fb69-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4fb69-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="4fb69-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4fb69-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="4fb69-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4fb69-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="4fb69-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4fb69-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="4fb69-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4fb69-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="4fb69-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4fb69-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4fb69-123">-Context</span></span>
<span data-ttu-id="4fb69-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="4fb69-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fb69-125">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="4fb69-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fb69-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb69-126">-DefaultProfile</span></span>
<span data-ttu-id="4fb69-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb69-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb69-128">-Kvot</span><span class="sxs-lookup"><span data-stu-id="4fb69-128">-Quota</span></span>
<span data-ttu-id="4fb69-129">Anger kvot värde i GB (gigabyte).</span><span class="sxs-lookup"><span data-stu-id="4fb69-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="4fb69-130">Se kvot begränsningen i https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="4fb69-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb69-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fb69-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4fb69-132">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="4fb69-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4fb69-133">-Dela</span><span class="sxs-lookup"><span data-stu-id="4fb69-133">-Share</span></span>
<span data-ttu-id="4fb69-134">Anger ett **CloudFileShare** -objekt som representerar den resurs som den här cmdleten ställer in en kvot för.</span><span class="sxs-lookup"><span data-stu-id="4fb69-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="4fb69-135">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="4fb69-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="4fb69-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4fb69-136">-ShareName</span></span>
<span data-ttu-id="4fb69-137">Anger namnet på den fil resurs som du vill ange en kvot för.</span><span class="sxs-lookup"><span data-stu-id="4fb69-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb69-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb69-138">CommonParameters</span></span>
<span data-ttu-id="4fb69-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb69-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb69-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb69-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb69-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fb69-141">INPUTS</span></span>

### <span data-ttu-id="4fb69-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb69-142">System.String</span></span>

### <span data-ttu-id="4fb69-143">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4fb69-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4fb69-144">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fb69-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4fb69-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fb69-145">OUTPUTS</span></span>

### <span data-ttu-id="4fb69-146">Microsoft. WindowsAzure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="4fb69-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="4fb69-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fb69-147">NOTES</span></span>

## <span data-ttu-id="4fb69-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fb69-148">RELATED LINKS</span></span>

[<span data-ttu-id="4fb69-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fb69-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="4fb69-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fb69-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4fb69-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fb69-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
