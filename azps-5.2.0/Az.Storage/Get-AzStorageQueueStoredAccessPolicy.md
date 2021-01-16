---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404187"
---
# <span data-ttu-id="a9f95-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f95-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a9f95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9f95-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f95-103">Hämtar den lagrade åtkomst principen för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="a9f95-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a9f95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9f95-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f95-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9f95-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f95-106">Cmdleten **Get-AzStorageQueueStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="a9f95-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a9f95-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9f95-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f95-108">Exempel 1: Hämta en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="a9f95-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="a9f95-109">Det här kommandot får åtkomst principen med namnet Policy12 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="a9f95-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="a9f95-110">Exempel 2: Hämta alla lagrade åtkomst principer i kön</span><span class="sxs-lookup"><span data-stu-id="a9f95-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="a9f95-111">Det här kommandot får alla lagrade åtkomst principer i kön som heter kön.</span><span class="sxs-lookup"><span data-stu-id="a9f95-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="a9f95-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9f95-112">PARAMETERS</span></span>

### <span data-ttu-id="a9f95-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a9f95-113">-Context</span></span>
<span data-ttu-id="a9f95-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="a9f95-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a9f95-115">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a9f95-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9f95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f95-116">-DefaultProfile</span></span>
<span data-ttu-id="a9f95-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f95-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="a9f95-118">-Policy</span></span>
<span data-ttu-id="a9f95-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="a9f95-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a9f95-120">-Kö</span><span class="sxs-lookup"><span data-stu-id="a9f95-120">-Queue</span></span>
<span data-ttu-id="a9f95-121">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="a9f95-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a9f95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f95-122">CommonParameters</span></span>
<span data-ttu-id="a9f95-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f95-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f95-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f95-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9f95-125">INPUTS</span></span>

### <span data-ttu-id="a9f95-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f95-126">System.String</span></span>

### <span data-ttu-id="a9f95-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9f95-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9f95-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9f95-128">OUTPUTS</span></span>

### <span data-ttu-id="a9f95-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="a9f95-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="a9f95-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9f95-130">NOTES</span></span>

## <span data-ttu-id="a9f95-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9f95-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9f95-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f95-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a9f95-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f95-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a9f95-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f95-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a9f95-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9f95-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


