---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931581"
---
# <span data-ttu-id="635a2-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="635a2-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="635a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="635a2-102">SYNOPSIS</span></span>
<span data-ttu-id="635a2-103">Visar lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="635a2-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="635a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="635a2-104">SYNTAX</span></span>

### <span data-ttu-id="635a2-105">QueueName (standard)</span><span class="sxs-lookup"><span data-stu-id="635a2-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="635a2-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="635a2-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="635a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="635a2-107">DESCRIPTION</span></span>
<span data-ttu-id="635a2-108">Cmdleten **Get-AzureStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="635a2-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="635a2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="635a2-109">EXAMPLES</span></span>

### <span data-ttu-id="635a2-110">Exempel 1: lista alla köer för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="635a2-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="635a2-111">Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="635a2-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="635a2-112">Exempel 2: lista Azure Storage-köer med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="635a2-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="635a2-113">Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="635a2-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="635a2-114">Exempel 3: lista Azure Storage köer med prefixet könamn</span><span class="sxs-lookup"><span data-stu-id="635a2-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="635a2-115">I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="635a2-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="635a2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="635a2-116">PARAMETERS</span></span>

### <span data-ttu-id="635a2-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="635a2-117">-Context</span></span>
<span data-ttu-id="635a2-118">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="635a2-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="635a2-119">Du kan skapa det med hjälp av **New-AzureStorageContext** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="635a2-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="635a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635a2-120">-DefaultProfile</span></span>
<span data-ttu-id="635a2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="635a2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="635a2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="635a2-122">-Name</span></span>
<span data-ttu-id="635a2-123">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="635a2-123">Specifies a name.</span></span>
<span data-ttu-id="635a2-124">Om du inte anger något namn visas en lista över alla köer i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="635a2-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="635a2-125">Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="635a2-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="635a2-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="635a2-126">-Prefix</span></span>
<span data-ttu-id="635a2-127">Anger ett prefix som används i namnet på de köer som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="635a2-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="635a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635a2-128">CommonParameters</span></span>
<span data-ttu-id="635a2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="635a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635a2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="635a2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635a2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="635a2-131">INPUTS</span></span>

### <span data-ttu-id="635a2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="635a2-132">System.String</span></span>

### <span data-ttu-id="635a2-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="635a2-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="635a2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="635a2-134">OUTPUTS</span></span>

### <span data-ttu-id="635a2-135">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="635a2-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="635a2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="635a2-136">NOTES</span></span>

## <span data-ttu-id="635a2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="635a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="635a2-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="635a2-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="635a2-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="635a2-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


