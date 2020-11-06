---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571672"
---
# <span data-ttu-id="8f518-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f518-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="8f518-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f518-102">SYNOPSIS</span></span>
<span data-ttu-id="8f518-103">Skapar en lagrad åtkomst princip på en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="8f518-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="8f518-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f518-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f518-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f518-105">DESCRIPTION</span></span>
<span data-ttu-id="8f518-106">Cmdleten **New-AzureStorageShareStoredAccessPolicy** skapar en lagrad åtkomst princip på en Azure lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="8f518-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="8f518-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f518-107">EXAMPLES</span></span>

### <span data-ttu-id="8f518-108">Exempel 1: skapa en lagrad åtkomst princip i en resurs</span><span class="sxs-lookup"><span data-stu-id="8f518-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="8f518-109">Det här kommandot skapar en lagrad åtkomst princip med fullständig behörighet i en resurs.</span><span class="sxs-lookup"><span data-stu-id="8f518-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="8f518-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f518-110">PARAMETERS</span></span>

### <span data-ttu-id="8f518-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8f518-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8f518-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="8f518-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8f518-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="8f518-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8f518-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="8f518-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8f518-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8f518-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8f518-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8f518-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8f518-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="8f518-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8f518-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="8f518-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8f518-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="8f518-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8f518-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="8f518-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8f518-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8f518-121">-Context</span></span>
<span data-ttu-id="8f518-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="8f518-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8f518-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="8f518-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f518-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f518-124">-ExpiryTime</span></span>
<span data-ttu-id="8f518-125">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="8f518-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f518-126">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="8f518-126">-Permission</span></span>
<span data-ttu-id="8f518-127">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings resursen eller filerna under den.</span><span class="sxs-lookup"><span data-stu-id="8f518-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

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

### <span data-ttu-id="8f518-128">-Princip</span><span class="sxs-lookup"><span data-stu-id="8f518-128">-Policy</span></span>
<span data-ttu-id="8f518-129">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="8f518-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f518-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8f518-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8f518-131">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="8f518-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8f518-132">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8f518-132">-ShareName</span></span>
<span data-ttu-id="8f518-133">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="8f518-133">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f518-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f518-134">-StartTime</span></span>
<span data-ttu-id="8f518-135">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="8f518-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f518-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f518-136">CommonParameters</span></span>
<span data-ttu-id="8f518-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f518-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f518-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f518-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f518-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f518-139">INPUTS</span></span>

## <span data-ttu-id="8f518-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f518-140">OUTPUTS</span></span>

## <span data-ttu-id="8f518-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f518-141">NOTES</span></span>

## <span data-ttu-id="8f518-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f518-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f518-143">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f518-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8f518-144">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f518-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8f518-145">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f518-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8f518-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f518-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
