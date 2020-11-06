---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586288"
---
# <span data-ttu-id="beea8-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="beea8-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="beea8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beea8-102">SYNOPSIS</span></span>
<span data-ttu-id="beea8-103">Skapar en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="beea8-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beea8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beea8-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="beea8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beea8-105">DESCRIPTION</span></span>
<span data-ttu-id="beea8-106">Cmdleten **New-AzureStorageQueueStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="beea8-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="beea8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beea8-107">EXAMPLES</span></span>

### <span data-ttu-id="beea8-108">Exempel 1: skapa en lagrad åtkomst princip i en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="beea8-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="beea8-109">Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="beea8-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="beea8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beea8-110">PARAMETERS</span></span>

### <span data-ttu-id="beea8-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="beea8-111">-Context</span></span>
<span data-ttu-id="beea8-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="beea8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="beea8-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="beea8-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="beea8-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="beea8-114">-ExpiryTime</span></span>
<span data-ttu-id="beea8-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="beea8-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="beea8-116">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="beea8-116">-Permission</span></span>
<span data-ttu-id="beea8-117">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="beea8-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="beea8-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="beea8-118">-Policy</span></span>
<span data-ttu-id="beea8-119">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="beea8-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="beea8-120">-Kö</span><span class="sxs-lookup"><span data-stu-id="beea8-120">-Queue</span></span>
<span data-ttu-id="beea8-121">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="beea8-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="beea8-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="beea8-122">-StartTime</span></span>
<span data-ttu-id="beea8-123">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="beea8-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="beea8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beea8-124">CommonParameters</span></span>
<span data-ttu-id="beea8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beea8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beea8-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beea8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beea8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beea8-127">INPUTS</span></span>

### <span data-ttu-id="beea8-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="beea8-128">IStorageContext</span></span>

<span data-ttu-id="beea8-129">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="beea8-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="beea8-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="beea8-130">String</span></span>

<span data-ttu-id="beea8-131">Parametern ' Queue ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="beea8-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="beea8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beea8-132">OUTPUTS</span></span>

### <span data-ttu-id="beea8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="beea8-133">System.String</span></span>

## <span data-ttu-id="beea8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beea8-134">NOTES</span></span>

## <span data-ttu-id="beea8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beea8-135">RELATED LINKS</span></span>

[<span data-ttu-id="beea8-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="beea8-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="beea8-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="beea8-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="beea8-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="beea8-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="beea8-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="beea8-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


