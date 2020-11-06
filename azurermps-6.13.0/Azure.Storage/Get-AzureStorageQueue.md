---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576367"
---
# <span data-ttu-id="5c2b4-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5c2b4-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="5c2b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2b4-103">Visar lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c2b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c2b4-104">SYNTAX</span></span>

### <span data-ttu-id="5c2b4-105">QueueName (standard)</span><span class="sxs-lookup"><span data-stu-id="5c2b4-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c2b4-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="5c2b4-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c2b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c2b4-107">DESCRIPTION</span></span>
<span data-ttu-id="5c2b4-108">Cmdleten **Get-AzureStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="5c2b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c2b4-109">EXAMPLES</span></span>

### <span data-ttu-id="5c2b4-110">Exempel 1: lista alla köer för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="5c2b4-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="5c2b4-111">Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="5c2b4-112">Exempel 2: lista Azure Storage-köer med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="5c2b4-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="5c2b4-113">Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="5c2b4-114">Exempel 3: lista Azure Storage köer med prefixet könamn</span><span class="sxs-lookup"><span data-stu-id="5c2b4-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="5c2b4-115">I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="5c2b4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c2b4-116">PARAMETERS</span></span>

### <span data-ttu-id="5c2b4-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5c2b4-117">-Context</span></span>
<span data-ttu-id="5c2b4-118">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5c2b4-119">Du kan skapa det med hjälp av **New-AzureStorageContext** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="5c2b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2b4-120">-DefaultProfile</span></span>
<span data-ttu-id="5c2b4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2b4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c2b4-122">-Name</span></span>
<span data-ttu-id="5c2b4-123">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-123">Specifies a name.</span></span>
<span data-ttu-id="5c2b4-124">Om du inte anger något namn visas en lista över alla köer i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="5c2b4-125">Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2b4-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5c2b4-126">-Prefix</span></span>
<span data-ttu-id="5c2b4-127">Anger ett prefix som används i namnet på de köer som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2b4-128">CommonParameters</span></span>
<span data-ttu-id="5c2b4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c2b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2b4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c2b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2b4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c2b4-131">INPUTS</span></span>

### <span data-ttu-id="5c2b4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c2b4-132">System.String</span></span>

### <span data-ttu-id="5c2b4-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c2b4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5c2b4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c2b4-134">OUTPUTS</span></span>

### <span data-ttu-id="5c2b4-135">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5c2b4-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="5c2b4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c2b4-136">NOTES</span></span>

## <span data-ttu-id="5c2b4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c2b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="5c2b4-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5c2b4-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="5c2b4-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5c2b4-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


