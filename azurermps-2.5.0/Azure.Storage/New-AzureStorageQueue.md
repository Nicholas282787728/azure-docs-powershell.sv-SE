---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930398"
---
# <span data-ttu-id="1af1e-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1af1e-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="1af1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1af1e-102">SYNOPSIS</span></span>
<span data-ttu-id="1af1e-103">Skapar en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="1af1e-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1af1e-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1af1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1af1e-105">DESCRIPTION</span></span>
<span data-ttu-id="1af1e-106">Cmdleten **New-AzureStorageQueue** skapar en lagrings kö i Azure.</span><span class="sxs-lookup"><span data-stu-id="1af1e-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="1af1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1af1e-107">EXAMPLES</span></span>

### <span data-ttu-id="1af1e-108">Exempel 1: skapa en Azure Storage-kö</span><span class="sxs-lookup"><span data-stu-id="1af1e-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="1af1e-109">I det här exemplet skapas en lagrings kö med namnet queueabc.</span><span class="sxs-lookup"><span data-stu-id="1af1e-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="1af1e-110">Exempel 2: skapa flera Azure Storage-köer</span><span class="sxs-lookup"><span data-stu-id="1af1e-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="1af1e-111">I det här exemplet skapas flera lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="1af1e-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="1af1e-112">Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="1af1e-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="1af1e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1af1e-113">PARAMETERS</span></span>

### <span data-ttu-id="1af1e-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1af1e-114">-Context</span></span>
<span data-ttu-id="1af1e-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="1af1e-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1af1e-116">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af1e-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1af1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af1e-117">-DefaultProfile</span></span>
<span data-ttu-id="1af1e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1af1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af1e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1af1e-119">-Name</span></span>
<span data-ttu-id="1af1e-120">Anger ett namn för kön.</span><span class="sxs-lookup"><span data-stu-id="1af1e-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="1af1e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af1e-121">CommonParameters</span></span>
<span data-ttu-id="1af1e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af1e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af1e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af1e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af1e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1af1e-124">INPUTS</span></span>

### <span data-ttu-id="1af1e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1af1e-125">System.String</span></span>

### <span data-ttu-id="1af1e-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1af1e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1af1e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1af1e-127">OUTPUTS</span></span>

### <span data-ttu-id="1af1e-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1af1e-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="1af1e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1af1e-129">NOTES</span></span>

## <span data-ttu-id="1af1e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1af1e-130">RELATED LINKS</span></span>

[<span data-ttu-id="1af1e-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1af1e-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="1af1e-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1af1e-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


