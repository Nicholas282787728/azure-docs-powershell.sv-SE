---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 7fa9ebe8c64cca3f05e3bad4ab890d990861b399
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746302"
---
# <span data-ttu-id="09b27-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="09b27-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="09b27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09b27-102">SYNOPSIS</span></span>
<span data-ttu-id="09b27-103">Tar bort CORS för en lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="09b27-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="09b27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09b27-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="09b27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09b27-105">DESCRIPTION</span></span>
<span data-ttu-id="09b27-106">Cmdleten **Remove-AzStorageCORSRule** tar bort resurs delning av över-ursprung (CORS) för en Azure Storage-tjänst.</span><span class="sxs-lookup"><span data-stu-id="09b27-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="09b27-107">Denna cmdlet tar bort alla CORS-regler i en lagrings tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="09b27-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="09b27-108">Typerna av lagrings tjänster för denna cmdlet är BLOB, tabell, kö och fil.</span><span class="sxs-lookup"><span data-stu-id="09b27-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="09b27-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09b27-109">EXAMPLES</span></span>

### <span data-ttu-id="09b27-110">Exempel 1: ta bort CORS-regler för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="09b27-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="09b27-111">Det här kommandot tar bort CORS-regler för typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="09b27-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="09b27-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09b27-112">PARAMETERS</span></span>

### <span data-ttu-id="09b27-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09b27-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09b27-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="09b27-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09b27-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="09b27-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09b27-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="09b27-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09b27-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09b27-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09b27-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="09b27-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="09b27-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="09b27-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="09b27-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="09b27-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="09b27-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="09b27-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="09b27-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="09b27-122">The default value is 10.</span></span>

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

### <span data-ttu-id="09b27-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="09b27-123">-Context</span></span>
<span data-ttu-id="09b27-124">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="09b27-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="09b27-125">New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="09b27-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09b27-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b27-126">-DefaultProfile</span></span>
<span data-ttu-id="09b27-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09b27-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09b27-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09b27-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09b27-129">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="09b27-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="09b27-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="09b27-130">-ServiceType</span></span>
<span data-ttu-id="09b27-131">Anger typen för Azure Storage-tjänsten för vilken denna cmdlet tar bort regler.</span><span class="sxs-lookup"><span data-stu-id="09b27-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="09b27-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="09b27-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09b27-133">Object</span><span class="sxs-lookup"><span data-stu-id="09b27-133">Blob</span></span> 
- <span data-ttu-id="09b27-134">Tabell</span><span class="sxs-lookup"><span data-stu-id="09b27-134">Table</span></span> 
- <span data-ttu-id="09b27-135">Svarskö</span><span class="sxs-lookup"><span data-stu-id="09b27-135">Queue</span></span> 
- <span data-ttu-id="09b27-136">Fil</span><span class="sxs-lookup"><span data-stu-id="09b27-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b27-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b27-137">CommonParameters</span></span>
<span data-ttu-id="09b27-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b27-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b27-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b27-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b27-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09b27-140">INPUTS</span></span>

### <span data-ttu-id="09b27-141">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09b27-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="09b27-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09b27-142">OUTPUTS</span></span>

### <span data-ttu-id="09b27-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="09b27-143">System.Void</span></span>

## <span data-ttu-id="09b27-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09b27-144">NOTES</span></span>

## <span data-ttu-id="09b27-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09b27-145">RELATED LINKS</span></span>

[<span data-ttu-id="09b27-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="09b27-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="09b27-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="09b27-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)

