---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 1b1e3b793e2c71e782b21618e5f8b8fe952eca36
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923546"
---
# <span data-ttu-id="1ae3d-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae3d-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="1ae3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ae3d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae3d-103">Skapar en lagrad åtkomst princip på en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="1ae3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ae3d-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1ae3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ae3d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae3d-106">Cmdleten **New-AzStorageShareStoredAccessPolicy** skapar en lagrad åtkomst princip på en Azure lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="1ae3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ae3d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae3d-108">Exempel 1: skapa en lagrad åtkomst princip i en resurs</span><span class="sxs-lookup"><span data-stu-id="1ae3d-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="1ae3d-109">Det här kommandot skapar en lagrad åtkomst princip med fullständig behörighet i en resurs.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="1ae3d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ae3d-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae3d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1ae3d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1ae3d-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1ae3d-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1ae3d-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1ae3d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1ae3d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1ae3d-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1ae3d-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1ae3d-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1ae3d-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1ae3d-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="1ae3d-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1ae3d-121">-Context</span></span>
<span data-ttu-id="1ae3d-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1ae3d-123">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1ae3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae3d-124">-DefaultProfile</span></span>
<span data-ttu-id="1ae3d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae3d-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ae3d-126">-ExpiryTime</span></span>
<span data-ttu-id="1ae3d-127">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="1ae3d-128">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="1ae3d-128">-Permission</span></span>
<span data-ttu-id="1ae3d-129">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings resursen eller filerna under den.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="1ae3d-130">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="1ae3d-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="1ae3d-131">-Princip</span><span class="sxs-lookup"><span data-stu-id="1ae3d-131">-Policy</span></span>
<span data-ttu-id="1ae3d-132">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="1ae3d-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1ae3d-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1ae3d-134">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1ae3d-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1ae3d-135">-ShareName</span></span>
<span data-ttu-id="1ae3d-136">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="1ae3d-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1ae3d-137">-StartTime</span></span>
<span data-ttu-id="1ae3d-138">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="1ae3d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae3d-139">CommonParameters</span></span>
<span data-ttu-id="1ae3d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae3d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae3d-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae3d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae3d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ae3d-142">INPUTS</span></span>

### <span data-ttu-id="1ae3d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae3d-143">System.String</span></span>

### <span data-ttu-id="1ae3d-144">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ae3d-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1ae3d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ae3d-145">OUTPUTS</span></span>

### <span data-ttu-id="1ae3d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae3d-146">System.String</span></span>

## <span data-ttu-id="1ae3d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ae3d-147">NOTES</span></span>

## <span data-ttu-id="1ae3d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ae3d-148">RELATED LINKS</span></span>

[<span data-ttu-id="1ae3d-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae3d-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1ae3d-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ae3d-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1ae3d-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae3d-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1ae3d-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae3d-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)