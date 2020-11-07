---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9ef4be8331c1de38789d25903db9e98f4e2d8cd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929157"
---
# <span data-ttu-id="6e51c-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e51c-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6e51c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e51c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e51c-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="6e51c-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e51c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e51c-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e51c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e51c-105">DESCRIPTION</span></span>
<span data-ttu-id="6e51c-106">Cmdleten **Get-AzureStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="6e51c-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="6e51c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e51c-107">EXAMPLES</span></span>

### <span data-ttu-id="6e51c-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="6e51c-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="6e51c-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="6e51c-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="6e51c-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="6e51c-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="6e51c-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="6e51c-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="6e51c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e51c-112">PARAMETERS</span></span>

### <span data-ttu-id="6e51c-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6e51c-113">-Context</span></span>
<span data-ttu-id="6e51c-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="6e51c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6e51c-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="6e51c-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e51c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e51c-116">-DefaultProfile</span></span>
<span data-ttu-id="6e51c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e51c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e51c-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="6e51c-118">-Policy</span></span>
<span data-ttu-id="6e51c-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="6e51c-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="6e51c-120">-Kö</span><span class="sxs-lookup"><span data-stu-id="6e51c-120">-Queue</span></span>
<span data-ttu-id="6e51c-121">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="6e51c-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6e51c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e51c-122">CommonParameters</span></span>
<span data-ttu-id="6e51c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e51c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e51c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e51c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e51c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e51c-125">INPUTS</span></span>

### <span data-ttu-id="6e51c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6e51c-126">System.String</span></span>

### <span data-ttu-id="6e51c-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e51c-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e51c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e51c-128">OUTPUTS</span></span>

### <span data-ttu-id="6e51c-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="6e51c-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="6e51c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e51c-130">NOTES</span></span>

## <span data-ttu-id="6e51c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e51c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e51c-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e51c-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e51c-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e51c-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e51c-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e51c-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e51c-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e51c-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


