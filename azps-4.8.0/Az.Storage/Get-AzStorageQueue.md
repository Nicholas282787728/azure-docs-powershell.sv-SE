---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100750"
---
# <span data-ttu-id="b2afc-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b2afc-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="b2afc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2afc-102">SYNOPSIS</span></span>
<span data-ttu-id="b2afc-103">Visar lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="b2afc-103">Lists storage queues.</span></span>

## <span data-ttu-id="b2afc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2afc-104">SYNTAX</span></span>

### <span data-ttu-id="b2afc-105">QueueName (standard)</span><span class="sxs-lookup"><span data-stu-id="b2afc-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2afc-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b2afc-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2afc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2afc-107">DESCRIPTION</span></span>
<span data-ttu-id="b2afc-108">Cmdleten **Get-AzStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="b2afc-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b2afc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2afc-109">EXAMPLES</span></span>

### <span data-ttu-id="b2afc-110">Exempel 1: lista alla köer för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="b2afc-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="b2afc-111">Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b2afc-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b2afc-112">Exempel 2: lista Azure Storage-köer med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="b2afc-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="b2afc-113">Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="b2afc-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b2afc-114">Exempel 3: lista Azure Storage köer med prefixet könamn</span><span class="sxs-lookup"><span data-stu-id="b2afc-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="b2afc-115">I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.</span><span class="sxs-lookup"><span data-stu-id="b2afc-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b2afc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2afc-116">PARAMETERS</span></span>

### <span data-ttu-id="b2afc-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b2afc-117">-Context</span></span>
<span data-ttu-id="b2afc-118">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="b2afc-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b2afc-119">Du kan skapa det med hjälp av **New-AzStorageContext** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2afc-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="b2afc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2afc-120">-DefaultProfile</span></span>
<span data-ttu-id="b2afc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2afc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2afc-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2afc-122">-Name</span></span>
<span data-ttu-id="b2afc-123">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="b2afc-123">Specifies a name.</span></span>
<span data-ttu-id="b2afc-124">Om du inte anger något namn visas en lista över alla köer i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2afc-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b2afc-125">Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="b2afc-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="b2afc-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b2afc-126">-Prefix</span></span>
<span data-ttu-id="b2afc-127">Anger ett prefix som används i namnet på de köer som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="b2afc-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="b2afc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2afc-128">CommonParameters</span></span>
<span data-ttu-id="b2afc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2afc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2afc-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2afc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2afc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2afc-131">INPUTS</span></span>

### <span data-ttu-id="b2afc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b2afc-132">System.String</span></span>

### <span data-ttu-id="b2afc-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2afc-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b2afc-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2afc-134">OUTPUTS</span></span>

### <span data-ttu-id="b2afc-135">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b2afc-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b2afc-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2afc-136">NOTES</span></span>

## <span data-ttu-id="b2afc-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2afc-137">RELATED LINKS</span></span>

[<span data-ttu-id="b2afc-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b2afc-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="b2afc-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b2afc-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


