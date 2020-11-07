---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 247de1e6c93f8f581f6e34beb778b079d6c9987e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755562"
---
# <span data-ttu-id="b6583-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6583-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b6583-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6583-102">SYNOPSIS</span></span>
<span data-ttu-id="b6583-103">Hämtar lagrade åtkomst principer för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="b6583-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6583-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6583-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b6583-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6583-105">DESCRIPTION</span></span>
<span data-ttu-id="b6583-106">Cmdleten **Get-AzureStorageShareStoredAccessPolicy** hämtar åtkomst principer för en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="b6583-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="b6583-107">För att få en viss princip anger du den efter namn.</span><span class="sxs-lookup"><span data-stu-id="b6583-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="b6583-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6583-108">EXAMPLES</span></span>

### <span data-ttu-id="b6583-109">Exempel 1: Hämta en lagrad åtkomst princip i en resurs</span><span class="sxs-lookup"><span data-stu-id="b6583-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="b6583-110">Det här kommandot får en lagrad åtkomst princip med namnet GeneralPolicy i ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="b6583-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="b6583-111">Exempel 2: Hämta alla lagrade åtkomst principer i dela</span><span class="sxs-lookup"><span data-stu-id="b6583-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="b6583-112">Det här kommandot får alla lagrade åtkomst principer i ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="b6583-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="b6583-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6583-113">PARAMETERS</span></span>

### <span data-ttu-id="b6583-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6583-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b6583-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="b6583-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6583-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="b6583-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6583-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b6583-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6583-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b6583-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b6583-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b6583-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b6583-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b6583-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b6583-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="b6583-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b6583-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="b6583-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b6583-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b6583-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b6583-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b6583-124">-Context</span></span>
<span data-ttu-id="b6583-125">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="b6583-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b6583-126">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="b6583-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b6583-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6583-127">-DefaultProfile</span></span>
<span data-ttu-id="b6583-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6583-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6583-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="b6583-129">-Policy</span></span>
<span data-ttu-id="b6583-130">Anger namnet på den lagrade åtkomst principen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b6583-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6583-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6583-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b6583-132">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="b6583-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b6583-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b6583-133">-ShareName</span></span>
<span data-ttu-id="b6583-134">Anger namnet på den lagrings resurs som denna cmdlet hämtar principer för.</span><span class="sxs-lookup"><span data-stu-id="b6583-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="b6583-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6583-135">CommonParameters</span></span>
<span data-ttu-id="b6583-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6583-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6583-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6583-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6583-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6583-138">INPUTS</span></span>

### <span data-ttu-id="b6583-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b6583-139">System.String</span></span>

### <span data-ttu-id="b6583-140">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6583-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6583-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6583-141">OUTPUTS</span></span>

### <span data-ttu-id="b6583-142">Microsoft. WindowsAzure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="b6583-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="b6583-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6583-143">NOTES</span></span>

## <span data-ttu-id="b6583-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6583-144">RELATED LINKS</span></span>

[<span data-ttu-id="b6583-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6583-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b6583-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6583-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b6583-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6583-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b6583-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6583-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
