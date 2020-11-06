---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3fe38645f4903e2020199b10b277da856046ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581572"
---
# <span data-ttu-id="ff698-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ff698-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="ff698-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff698-102">SYNOPSIS</span></span>
<span data-ttu-id="ff698-103">Visar lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="ff698-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff698-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff698-104">SYNTAX</span></span>

### <span data-ttu-id="ff698-105">QueueName (standard)</span><span class="sxs-lookup"><span data-stu-id="ff698-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ff698-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="ff698-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ff698-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff698-107">DESCRIPTION</span></span>
<span data-ttu-id="ff698-108">Cmdleten **Get-AzureStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="ff698-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="ff698-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff698-109">EXAMPLES</span></span>

### <span data-ttu-id="ff698-110">Exempel 1: lista alla köer för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="ff698-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="ff698-111">Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ff698-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="ff698-112">Exempel 2: lista Azure Storage-köer med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="ff698-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="ff698-113">Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="ff698-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="ff698-114">Exempel 3: lista Azure Storage köer med prefixet könamn</span><span class="sxs-lookup"><span data-stu-id="ff698-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="ff698-115">I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="ff698-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="ff698-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff698-116">PARAMETERS</span></span>

### <span data-ttu-id="ff698-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ff698-117">-Context</span></span>
<span data-ttu-id="ff698-118">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="ff698-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ff698-119">Du kan skapa det med hjälp av **New-AzureStorageContext** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff698-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="ff698-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff698-120">-Name</span></span>
<span data-ttu-id="ff698-121">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="ff698-121">Specifies a name.</span></span>
<span data-ttu-id="ff698-122">Om du inte anger något namn visas en lista över alla köer i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff698-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="ff698-123">Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="ff698-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="ff698-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ff698-124">-Prefix</span></span>
<span data-ttu-id="ff698-125">Anger ett prefix som används i namnet på de köer som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="ff698-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff698-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff698-126">CommonParameters</span></span>
<span data-ttu-id="ff698-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff698-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff698-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff698-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff698-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff698-129">INPUTS</span></span>

### <span data-ttu-id="ff698-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff698-130">IStorageContext</span></span>

<span data-ttu-id="ff698-131">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ff698-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ff698-132">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="ff698-132">String</span></span>

<span data-ttu-id="ff698-133">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="ff698-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ff698-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff698-134">OUTPUTS</span></span>

### <span data-ttu-id="ff698-135">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ff698-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="ff698-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff698-136">NOTES</span></span>

## <span data-ttu-id="ff698-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff698-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff698-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ff698-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="ff698-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ff698-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


