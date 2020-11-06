---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572368"
---
# <span data-ttu-id="813b3-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="813b3-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="813b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="813b3-102">SYNOPSIS</span></span>
<span data-ttu-id="813b3-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="813b3-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="813b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="813b3-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="813b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="813b3-105">DESCRIPTION</span></span>
<span data-ttu-id="813b3-106">Cmdleten **Get-AzureStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="813b3-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="813b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="813b3-107">EXAMPLES</span></span>

### <span data-ttu-id="813b3-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="813b3-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="813b3-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="813b3-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="813b3-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="813b3-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="813b3-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="813b3-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="813b3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="813b3-112">PARAMETERS</span></span>

### <span data-ttu-id="813b3-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="813b3-113">-Context</span></span>
<span data-ttu-id="813b3-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="813b3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="813b3-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="813b3-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="813b3-116">-Princip</span><span class="sxs-lookup"><span data-stu-id="813b3-116">-Policy</span></span>
<span data-ttu-id="813b3-117">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="813b3-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="813b3-118">-Kö</span><span class="sxs-lookup"><span data-stu-id="813b3-118">-Queue</span></span>
<span data-ttu-id="813b3-119">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="813b3-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="813b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813b3-120">CommonParameters</span></span>
<span data-ttu-id="813b3-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813b3-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813b3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813b3-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="813b3-123">INPUTS</span></span>

## <span data-ttu-id="813b3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="813b3-124">OUTPUTS</span></span>

## <span data-ttu-id="813b3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="813b3-125">NOTES</span></span>

## <span data-ttu-id="813b3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="813b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="813b3-127">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="813b3-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="813b3-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="813b3-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="813b3-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="813b3-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="813b3-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="813b3-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


