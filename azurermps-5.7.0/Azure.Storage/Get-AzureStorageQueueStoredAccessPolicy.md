---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ebf5596ba63a86e3865c5a6dc05bdea648dc18c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577347"
---
# <span data-ttu-id="9b7a5-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7a5-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9b7a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7a5-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b7a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b7a5-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b7a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b7a5-105">DESCRIPTION</span></span>
<span data-ttu-id="9b7a5-106">Cmdleten **Get-AzureStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="9b7a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b7a5-107">EXAMPLES</span></span>

### <span data-ttu-id="9b7a5-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="9b7a5-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="9b7a5-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="9b7a5-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="9b7a5-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="9b7a5-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="9b7a5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b7a5-112">PARAMETERS</span></span>

### <span data-ttu-id="9b7a5-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9b7a5-113">-Context</span></span>
<span data-ttu-id="9b7a5-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9b7a5-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9b7a5-116">-Princip</span><span class="sxs-lookup"><span data-stu-id="9b7a5-116">-Policy</span></span>
<span data-ttu-id="9b7a5-117">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="9b7a5-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="9b7a5-118">-Kö</span><span class="sxs-lookup"><span data-stu-id="9b7a5-118">-Queue</span></span>
<span data-ttu-id="9b7a5-119">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="9b7a5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7a5-120">CommonParameters</span></span>
<span data-ttu-id="9b7a5-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7a5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7a5-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7a5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7a5-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b7a5-123">INPUTS</span></span>

### <span data-ttu-id="9b7a5-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b7a5-124">IStorageContext</span></span>

<span data-ttu-id="9b7a5-125">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9b7a5-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9b7a5-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="9b7a5-126">String</span></span>

<span data-ttu-id="9b7a5-127">Parametern ' Queue ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="9b7a5-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9b7a5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b7a5-128">OUTPUTS</span></span>

### <span data-ttu-id="9b7a5-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="9b7a5-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="9b7a5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b7a5-130">NOTES</span></span>

## <span data-ttu-id="9b7a5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b7a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b7a5-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7a5-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9b7a5-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7a5-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9b7a5-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7a5-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9b7a5-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b7a5-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


