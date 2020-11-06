---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577312"
---
# <span data-ttu-id="03182-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="03182-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="03182-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03182-102">SYNOPSIS</span></span>
<span data-ttu-id="03182-103">Skapar en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="03182-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03182-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03182-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="03182-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03182-105">DESCRIPTION</span></span>
<span data-ttu-id="03182-106">Cmdleten **New-AzureStorageQueue** skapar en lagrings kö i Azure.</span><span class="sxs-lookup"><span data-stu-id="03182-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="03182-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03182-107">EXAMPLES</span></span>

### <span data-ttu-id="03182-108">Exempel 1: skapa en Azure Storage-kö</span><span class="sxs-lookup"><span data-stu-id="03182-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="03182-109">I det här exemplet skapas en lagrings kö med namnet queueabc.</span><span class="sxs-lookup"><span data-stu-id="03182-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="03182-110">Exempel 2: skapa flera Azure Storage-köer</span><span class="sxs-lookup"><span data-stu-id="03182-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="03182-111">I det här exemplet skapas flera lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="03182-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="03182-112">Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="03182-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="03182-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03182-113">PARAMETERS</span></span>

### <span data-ttu-id="03182-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="03182-114">-Context</span></span>
<span data-ttu-id="03182-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="03182-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="03182-116">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03182-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03182-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="03182-117">-Name</span></span>
<span data-ttu-id="03182-118">Anger ett namn för kön.</span><span class="sxs-lookup"><span data-stu-id="03182-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03182-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03182-119">CommonParameters</span></span>
<span data-ttu-id="03182-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03182-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03182-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03182-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03182-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03182-122">INPUTS</span></span>

### <span data-ttu-id="03182-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03182-123">IStorageContext</span></span>

<span data-ttu-id="03182-124">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="03182-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="03182-125">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="03182-125">String</span></span>

<span data-ttu-id="03182-126">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="03182-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="03182-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03182-127">OUTPUTS</span></span>

### <span data-ttu-id="03182-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="03182-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="03182-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03182-129">NOTES</span></span>

## <span data-ttu-id="03182-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03182-130">RELATED LINKS</span></span>

[<span data-ttu-id="03182-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="03182-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="03182-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="03182-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


