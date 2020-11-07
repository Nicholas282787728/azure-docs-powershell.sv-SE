---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754996"
---
# <span data-ttu-id="2ebcc-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ebcc-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2ebcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ebcc-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebcc-103">Skapar en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2ebcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ebcc-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="2ebcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ebcc-105">DESCRIPTION</span></span>
<span data-ttu-id="2ebcc-106">Cmdleten **New-AzureStorageQueueStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2ebcc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ebcc-107">EXAMPLES</span></span>

### <span data-ttu-id="2ebcc-108">Exempel 1: skapa en lagrad åtkomst princip i en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="2ebcc-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="2ebcc-109">Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="2ebcc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ebcc-110">PARAMETERS</span></span>

### <span data-ttu-id="2ebcc-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2ebcc-111">-Context</span></span>
<span data-ttu-id="2ebcc-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2ebcc-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ebcc-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2ebcc-114">-ExpiryTime</span></span>
<span data-ttu-id="2ebcc-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebcc-116">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="2ebcc-116">-Permission</span></span>
<span data-ttu-id="2ebcc-117">Anger nivån för offentlig åtkomst till den här lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-117">Specifies the level of public access to this storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebcc-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="2ebcc-118">-Policy</span></span>
<span data-ttu-id="2ebcc-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebcc-120">-Kö</span><span class="sxs-lookup"><span data-stu-id="2ebcc-120">-Queue</span></span>
<span data-ttu-id="2ebcc-121">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ebcc-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2ebcc-122">-StartTime</span></span>
<span data-ttu-id="2ebcc-123">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebcc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebcc-124">CommonParameters</span></span>
<span data-ttu-id="2ebcc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebcc-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ebcc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebcc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ebcc-127">INPUTS</span></span>

## <span data-ttu-id="2ebcc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ebcc-128">OUTPUTS</span></span>

## <span data-ttu-id="2ebcc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ebcc-129">NOTES</span></span>

## <span data-ttu-id="2ebcc-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ebcc-130">RELATED LINKS</span></span>

[<span data-ttu-id="2ebcc-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ebcc-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2ebcc-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ebcc-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2ebcc-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ebcc-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2ebcc-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ebcc-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


