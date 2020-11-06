---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571371"
---
# <span data-ttu-id="6f5d4-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5d4-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="6f5d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5d4-103">Skapar en lagrad åtkomst princip för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6f5d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f5d4-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6f5d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5d4-106">Cmdleten **New-AzureStorageTableStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6f5d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="6f5d4-108">Exempel 1: skapa en lagrad åtkomst princip i en tabell</span><span class="sxs-lookup"><span data-stu-id="6f5d4-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="6f5d4-109">Det här kommandot skapar en åtkomst princip med namnet Policy02 i lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="6f5d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f5d4-110">PARAMETERS</span></span>

### <span data-ttu-id="6f5d4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6f5d4-111">-Context</span></span>
<span data-ttu-id="6f5d4-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6f5d4-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6f5d4-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6f5d4-114">-ExpiryTime</span></span>
<span data-ttu-id="6f5d4-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6f5d4-116">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="6f5d4-116">-Permission</span></span>
<span data-ttu-id="6f5d4-117">Anger nivån för offentlig åtkomst till den här lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="6f5d4-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="6f5d4-118">-Policy</span></span>
<span data-ttu-id="6f5d4-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="6f5d4-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="6f5d4-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6f5d4-120">-StartTime</span></span>
<span data-ttu-id="6f5d4-121">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6f5d4-122">-Tabell</span><span class="sxs-lookup"><span data-stu-id="6f5d4-122">-Table</span></span>
<span data-ttu-id="6f5d4-123">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="6f5d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5d4-124">CommonParameters</span></span>
<span data-ttu-id="6f5d4-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f5d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5d4-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5d4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5d4-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f5d4-127">INPUTS</span></span>

## <span data-ttu-id="6f5d4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f5d4-128">OUTPUTS</span></span>

## <span data-ttu-id="6f5d4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f5d4-129">NOTES</span></span>

## <span data-ttu-id="6f5d4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f5d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f5d4-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5d4-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6f5d4-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f5d4-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6f5d4-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5d4-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6f5d4-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5d4-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


