---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572347"
---
# <span data-ttu-id="787bf-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="787bf-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="787bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="787bf-102">SYNOPSIS</span></span>
<span data-ttu-id="787bf-103">Hämtar lagrade åtkomst principer för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="787bf-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="787bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="787bf-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="787bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="787bf-105">DESCRIPTION</span></span>
<span data-ttu-id="787bf-106">Cmdleten **Get-AzureStorageShareStoredAccessPolicy** hämtar åtkomst principer för en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="787bf-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="787bf-107">För att få en viss princip anger du den efter namn.</span><span class="sxs-lookup"><span data-stu-id="787bf-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="787bf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="787bf-108">EXAMPLES</span></span>

### <span data-ttu-id="787bf-109">Exempel 1: Hämta en lagrad åtkomst princip i en resurs</span><span class="sxs-lookup"><span data-stu-id="787bf-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="787bf-110">Det här kommandot får en lagrad åtkomst princip med namnet GeneralPolicy i ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="787bf-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="787bf-111">Exempel 2: Hämta alla lagrade åtkomst principer i dela</span><span class="sxs-lookup"><span data-stu-id="787bf-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="787bf-112">Det här kommandot får alla lagrade åtkomst principer i ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="787bf-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="787bf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="787bf-113">PARAMETERS</span></span>

### <span data-ttu-id="787bf-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="787bf-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="787bf-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="787bf-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="787bf-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="787bf-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="787bf-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="787bf-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="787bf-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="787bf-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="787bf-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="787bf-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="787bf-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="787bf-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="787bf-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="787bf-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="787bf-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="787bf-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="787bf-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="787bf-123">The default value is 10.</span></span>

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

### <span data-ttu-id="787bf-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="787bf-124">-Context</span></span>
<span data-ttu-id="787bf-125">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="787bf-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="787bf-126">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="787bf-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="787bf-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="787bf-127">-Policy</span></span>
<span data-ttu-id="787bf-128">Anger namnet på den lagrade åtkomst principen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="787bf-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="787bf-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="787bf-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="787bf-130">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="787bf-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="787bf-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="787bf-131">-ShareName</span></span>
<span data-ttu-id="787bf-132">Anger namnet på den lagrings resurs som denna cmdlet hämtar principer för.</span><span class="sxs-lookup"><span data-stu-id="787bf-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="787bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787bf-133">CommonParameters</span></span>
<span data-ttu-id="787bf-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787bf-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787bf-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="787bf-136">INPUTS</span></span>

## <span data-ttu-id="787bf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="787bf-137">OUTPUTS</span></span>

## <span data-ttu-id="787bf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="787bf-138">NOTES</span></span>

## <span data-ttu-id="787bf-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="787bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="787bf-140">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="787bf-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="787bf-141">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="787bf-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="787bf-142">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="787bf-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="787bf-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="787bf-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
