---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 55ee72941f49954bcc56f9558bc7ffb444ae9e6b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930386"
---
# <span data-ttu-id="7a1f3-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7a1f3-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="7a1f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1f3-103">Skapar en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a1f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a1f3-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a1f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1f3-106">Cmdleten **New-AzureStorageShare** skapar en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="7a1f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="7a1f3-108">Exempel 1: skapa en fil resurs</span><span class="sxs-lookup"><span data-stu-id="7a1f3-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="7a1f3-109">Det här kommandot skapar en fil resurs med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="7a1f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="7a1f3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a1f3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7a1f3-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7a1f3-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7a1f3-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7a1f3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7a1f3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7a1f3-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7a1f3-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7a1f3-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7a1f3-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7a1f3-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7a1f3-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7a1f3-121">-Context</span></span>
<span data-ttu-id="7a1f3-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7a1f3-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7a1f3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1f3-124">-DefaultProfile</span></span>
<span data-ttu-id="7a1f3-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a1f3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a1f3-126">-Name</span></span>
<span data-ttu-id="7a1f3-127">Anger namnet på en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="7a1f3-128">Denna cmdlet skapar en fil resurs som har det namn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a1f3-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7a1f3-130">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7a1f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1f3-131">CommonParameters</span></span>
<span data-ttu-id="7a1f3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1f3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1f3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a1f3-134">INPUTS</span></span>

### <span data-ttu-id="7a1f3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7a1f3-135">System.String</span></span>

### <span data-ttu-id="7a1f3-136">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a1f3-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a1f3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a1f3-137">OUTPUTS</span></span>

### <span data-ttu-id="7a1f3-138">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7a1f3-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="7a1f3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a1f3-139">NOTES</span></span>

## <span data-ttu-id="7a1f3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a1f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="7a1f3-141">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7a1f3-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="7a1f3-142">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a1f3-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7a1f3-143">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7a1f3-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
