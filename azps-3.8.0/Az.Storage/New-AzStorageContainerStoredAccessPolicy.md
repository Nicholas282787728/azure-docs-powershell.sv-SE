---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090330"
---
# <span data-ttu-id="92da6-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92da6-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="92da6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92da6-102">SYNOPSIS</span></span>
<span data-ttu-id="92da6-103">Skapar en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="92da6-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="92da6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92da6-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="92da6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92da6-105">DESCRIPTION</span></span>
<span data-ttu-id="92da6-106">Cmdleten **New-AzStorageContainerStoredAccessPolicy** skapar en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="92da6-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="92da6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92da6-107">EXAMPLES</span></span>

### <span data-ttu-id="92da6-108">Exempel 1: skapa en lagrad åtkomst princip i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="92da6-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="92da6-109">Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagrings behållaren som heter $.</span><span class="sxs-lookup"><span data-stu-id="92da6-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="92da6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92da6-110">PARAMETERS</span></span>

### <span data-ttu-id="92da6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92da6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92da6-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="92da6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92da6-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="92da6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92da6-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="92da6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92da6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92da6-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="92da6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="92da6-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="92da6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="92da6-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="92da6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="92da6-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="92da6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="92da6-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="92da6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="92da6-121">-Container</span><span class="sxs-lookup"><span data-stu-id="92da6-121">-Container</span></span>
<span data-ttu-id="92da6-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="92da6-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="92da6-123">-Context</span></span>
<span data-ttu-id="92da6-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="92da6-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="92da6-125">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="92da6-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="92da6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92da6-126">-DefaultProfile</span></span>
<span data-ttu-id="92da6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92da6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92da6-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="92da6-128">-ExpiryTime</span></span>
<span data-ttu-id="92da6-129">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="92da6-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-130">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="92da6-130">-Permission</span></span>
<span data-ttu-id="92da6-131">Anger behörigheter i den lagrade åtkomst principen för att komma åt behållaren.</span><span class="sxs-lookup"><span data-stu-id="92da6-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="92da6-132">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="92da6-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-133">-Princip</span><span class="sxs-lookup"><span data-stu-id="92da6-133">-Policy</span></span>
<span data-ttu-id="92da6-134">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="92da6-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92da6-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92da6-136">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="92da6-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92da6-137">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="92da6-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92da6-138">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="92da6-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="92da6-139">-StartTime</span></span>
<span data-ttu-id="92da6-140">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="92da6-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92da6-141">CommonParameters</span></span>
<span data-ttu-id="92da6-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92da6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92da6-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92da6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92da6-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92da6-144">INPUTS</span></span>

### <span data-ttu-id="92da6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="92da6-145">System.String</span></span>

### <span data-ttu-id="92da6-146">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="92da6-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="92da6-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92da6-147">OUTPUTS</span></span>

### <span data-ttu-id="92da6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="92da6-148">System.String</span></span>

## <span data-ttu-id="92da6-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92da6-149">NOTES</span></span>

## <span data-ttu-id="92da6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92da6-150">RELATED LINKS</span></span>

[<span data-ttu-id="92da6-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92da6-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="92da6-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="92da6-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="92da6-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92da6-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="92da6-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92da6-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


