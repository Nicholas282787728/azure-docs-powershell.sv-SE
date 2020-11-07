---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756647"
---
# <span data-ttu-id="2bfec-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2bfec-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2bfec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bfec-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfec-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2bfec-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bfec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bfec-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bfec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bfec-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfec-106">Cmdleten **Get-AzureStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2bfec-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="2bfec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bfec-107">EXAMPLES</span></span>

### <span data-ttu-id="2bfec-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="2bfec-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="2bfec-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="2bfec-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="2bfec-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="2bfec-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="2bfec-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="2bfec-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="2bfec-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bfec-112">PARAMETERS</span></span>

### <span data-ttu-id="2bfec-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2bfec-113">-Context</span></span>
<span data-ttu-id="2bfec-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="2bfec-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2bfec-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2bfec-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2bfec-116">-Princip</span><span class="sxs-lookup"><span data-stu-id="2bfec-116">-Policy</span></span>
<span data-ttu-id="2bfec-117">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="2bfec-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="2bfec-118">-Kö</span><span class="sxs-lookup"><span data-stu-id="2bfec-118">-Queue</span></span>
<span data-ttu-id="2bfec-119">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="2bfec-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2bfec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfec-120">CommonParameters</span></span>
<span data-ttu-id="2bfec-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfec-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfec-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfec-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bfec-123">INPUTS</span></span>

### <span data-ttu-id="2bfec-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2bfec-124">IStorageContext</span></span>

<span data-ttu-id="2bfec-125">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2bfec-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2bfec-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="2bfec-126">String</span></span>

<span data-ttu-id="2bfec-127">Parametern ' Queue ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="2bfec-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2bfec-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bfec-128">OUTPUTS</span></span>

### <span data-ttu-id="2bfec-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="2bfec-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="2bfec-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bfec-130">NOTES</span></span>

## <span data-ttu-id="2bfec-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bfec-131">RELATED LINKS</span></span>

[<span data-ttu-id="2bfec-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2bfec-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2bfec-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2bfec-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2bfec-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2bfec-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2bfec-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2bfec-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


