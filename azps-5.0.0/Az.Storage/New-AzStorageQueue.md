---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270387"
---
# <span data-ttu-id="2f80d-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2f80d-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="2f80d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f80d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f80d-103">Skapar en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="2f80d-103">Creates a storage queue.</span></span>

## <span data-ttu-id="2f80d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f80d-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f80d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f80d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f80d-106">Cmdleten **New-AzStorageQueue** skapar en lagrings kö i Azure.</span><span class="sxs-lookup"><span data-stu-id="2f80d-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="2f80d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f80d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f80d-108">Exempel 1: skapa en Azure Storage-kö</span><span class="sxs-lookup"><span data-stu-id="2f80d-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="2f80d-109">I det här exemplet skapas en lagrings kö med namnet queueabc.</span><span class="sxs-lookup"><span data-stu-id="2f80d-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="2f80d-110">Exempel 2: skapa flera Azure Storage-köer</span><span class="sxs-lookup"><span data-stu-id="2f80d-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="2f80d-111">I det här exemplet skapas flera lagrings köer.</span><span class="sxs-lookup"><span data-stu-id="2f80d-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="2f80d-112">Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="2f80d-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2f80d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-113">PARAMETERS</span></span>

### <span data-ttu-id="2f80d-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2f80d-114">-Context</span></span>
<span data-ttu-id="2f80d-115">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="2f80d-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2f80d-116">Du kan skapa det med hjälp av New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f80d-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2f80d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f80d-117">-DefaultProfile</span></span>
<span data-ttu-id="2f80d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f80d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f80d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f80d-119">-Name</span></span>
<span data-ttu-id="2f80d-120">Anger ett namn för kön.</span><span class="sxs-lookup"><span data-stu-id="2f80d-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="2f80d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f80d-121">CommonParameters</span></span>
<span data-ttu-id="2f80d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f80d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f80d-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f80d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f80d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f80d-124">INPUTS</span></span>

### <span data-ttu-id="2f80d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f80d-125">System.String</span></span>

### <span data-ttu-id="2f80d-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f80d-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2f80d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f80d-127">OUTPUTS</span></span>

### <span data-ttu-id="2f80d-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2f80d-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="2f80d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-129">NOTES</span></span>

## <span data-ttu-id="2f80d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f80d-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2f80d-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="2f80d-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2f80d-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)

