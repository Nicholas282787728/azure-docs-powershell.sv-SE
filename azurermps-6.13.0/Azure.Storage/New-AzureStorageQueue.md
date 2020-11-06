---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 62fc501c267e388498cb1563206d2efac083c058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575401"
---
# <span data-ttu-id="7735a-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7735a-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="7735a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7735a-102">SYNOPSIS</span></span>
<span data-ttu-id="7735a-103">Skapar en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="7735a-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7735a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7735a-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7735a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7735a-105">DESCRIPTION</span></span>
<span data-ttu-id="7735a-106">Cmdleten **New-AzureStorageQueue** skapar en lagrings kö i Azure.</span><span class="sxs-lookup"><span data-stu-id="7735a-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="7735a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7735a-107">EXAMPLES</span></span>

### <span data-ttu-id="7735a-108">Exempel 1: skapa en Azure Storage-kö</span><span class="sxs-lookup"><span data-stu-id="7735a-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="7735a-109">I det här exemplet skapas en lagrings kö med namnet queueabc.</span><span class="sxs-lookup"><span data-stu-id="7735a-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="7735a-110">Exempel 2: skapa flera Azure Storage-köer</span><span class="sxs-lookup"><span data-stu-id="7735a-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="7735a-111">I det här exemplet skapas flera lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="7735a-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="7735a-112">Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="7735a-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="7735a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7735a-113">PARAMETERS</span></span>

### <span data-ttu-id="7735a-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7735a-114">-Context</span></span>
<span data-ttu-id="7735a-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="7735a-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7735a-116">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7735a-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7735a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7735a-117">-DefaultProfile</span></span>
<span data-ttu-id="7735a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7735a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7735a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7735a-119">-Name</span></span>
<span data-ttu-id="7735a-120">Anger ett namn för kön.</span><span class="sxs-lookup"><span data-stu-id="7735a-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7735a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7735a-121">CommonParameters</span></span>
<span data-ttu-id="7735a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7735a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7735a-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7735a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7735a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7735a-124">INPUTS</span></span>

### <span data-ttu-id="7735a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7735a-125">System.String</span></span>

### <span data-ttu-id="7735a-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7735a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7735a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7735a-127">OUTPUTS</span></span>

### <span data-ttu-id="7735a-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7735a-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="7735a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7735a-129">NOTES</span></span>

## <span data-ttu-id="7735a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7735a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7735a-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7735a-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="7735a-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7735a-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


