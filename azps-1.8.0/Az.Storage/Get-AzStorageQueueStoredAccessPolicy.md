---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 77e51cbc29c740ecd1b7631a8da5f255b6168fa4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746380"
---
# <span data-ttu-id="443a7-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="443a7-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="443a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="443a7-102">SYNOPSIS</span></span>
<span data-ttu-id="443a7-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="443a7-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="443a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="443a7-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="443a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="443a7-105">DESCRIPTION</span></span>
<span data-ttu-id="443a7-106">Cmdleten **Get-AzStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="443a7-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="443a7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="443a7-107">EXAMPLES</span></span>

### <span data-ttu-id="443a7-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="443a7-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="443a7-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="443a7-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="443a7-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="443a7-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="443a7-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="443a7-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="443a7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="443a7-112">PARAMETERS</span></span>

### <span data-ttu-id="443a7-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="443a7-113">-Context</span></span>
<span data-ttu-id="443a7-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="443a7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="443a7-115">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="443a7-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="443a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443a7-116">-DefaultProfile</span></span>
<span data-ttu-id="443a7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="443a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="443a7-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="443a7-118">-Policy</span></span>
<span data-ttu-id="443a7-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="443a7-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="443a7-120">-Kö</span><span class="sxs-lookup"><span data-stu-id="443a7-120">-Queue</span></span>
<span data-ttu-id="443a7-121">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="443a7-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="443a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443a7-122">CommonParameters</span></span>
<span data-ttu-id="443a7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="443a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443a7-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="443a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443a7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="443a7-125">INPUTS</span></span>

### <span data-ttu-id="443a7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="443a7-126">System.String</span></span>

### <span data-ttu-id="443a7-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="443a7-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="443a7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="443a7-128">OUTPUTS</span></span>

### <span data-ttu-id="443a7-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="443a7-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="443a7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="443a7-130">NOTES</span></span>

## <span data-ttu-id="443a7-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="443a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="443a7-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="443a7-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="443a7-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="443a7-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="443a7-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="443a7-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="443a7-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="443a7-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


