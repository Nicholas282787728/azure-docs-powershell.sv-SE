---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572015"
---
# <span data-ttu-id="25ce1-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="25ce1-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="25ce1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="25ce1-103">Skapar en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="25ce1-103">Creates a storage queue.</span></span>

## <span data-ttu-id="25ce1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25ce1-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="25ce1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="25ce1-106">Cmdleten **New-AzureStorageQueue** skapar en lagrings kö i Azure.</span><span class="sxs-lookup"><span data-stu-id="25ce1-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="25ce1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="25ce1-108">Exempel 1: skapa en Azure Storage-kö</span><span class="sxs-lookup"><span data-stu-id="25ce1-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="25ce1-109">I det här exemplet skapas en lagrings kö med namnet queueabc.</span><span class="sxs-lookup"><span data-stu-id="25ce1-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="25ce1-110">Exempel 2: skapa flera Azure Storage-köer</span><span class="sxs-lookup"><span data-stu-id="25ce1-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="25ce1-111">I det här exemplet skapas flera lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="25ce1-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="25ce1-112">Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="25ce1-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="25ce1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25ce1-113">PARAMETERS</span></span>

### <span data-ttu-id="25ce1-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="25ce1-114">-Context</span></span>
<span data-ttu-id="25ce1-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="25ce1-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="25ce1-116">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ce1-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="25ce1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="25ce1-117">-Name</span></span>
<span data-ttu-id="25ce1-118">Anger ett namn för kön.</span><span class="sxs-lookup"><span data-stu-id="25ce1-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="25ce1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ce1-119">CommonParameters</span></span>
<span data-ttu-id="25ce1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ce1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ce1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ce1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ce1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25ce1-122">INPUTS</span></span>

## <span data-ttu-id="25ce1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25ce1-123">OUTPUTS</span></span>

## <span data-ttu-id="25ce1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25ce1-124">NOTES</span></span>

## <span data-ttu-id="25ce1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25ce1-125">RELATED LINKS</span></span>

[<span data-ttu-id="25ce1-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="25ce1-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="25ce1-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="25ce1-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


