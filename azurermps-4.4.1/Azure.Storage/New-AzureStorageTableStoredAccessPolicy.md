---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b87dd24c78b835e16ab1c4e8e9c0c3bb265d4feb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586283"
---
# <span data-ttu-id="7e994-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7e994-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7e994-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e994-102">SYNOPSIS</span></span>
<span data-ttu-id="7e994-103">Skapar en lagrad åtkomst princip för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="7e994-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e994-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e994-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="7e994-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e994-105">DESCRIPTION</span></span>
<span data-ttu-id="7e994-106">Cmdleten **New-AzureStorageTableStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="7e994-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="7e994-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e994-107">EXAMPLES</span></span>

### <span data-ttu-id="7e994-108">Exempel 1: skapa en lagrad åtkomst princip i en tabell</span><span class="sxs-lookup"><span data-stu-id="7e994-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="7e994-109">Det här kommandot skapar en åtkomst princip med namnet Policy02 i lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="7e994-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="7e994-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e994-110">PARAMETERS</span></span>

### <span data-ttu-id="7e994-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7e994-111">-Context</span></span>
<span data-ttu-id="7e994-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="7e994-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7e994-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="7e994-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7e994-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7e994-114">-ExpiryTime</span></span>
<span data-ttu-id="7e994-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="7e994-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7e994-116">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="7e994-116">-Permission</span></span>
<span data-ttu-id="7e994-117">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="7e994-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="7e994-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="7e994-118">-Policy</span></span>
<span data-ttu-id="7e994-119">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="7e994-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="7e994-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7e994-120">-StartTime</span></span>
<span data-ttu-id="7e994-121">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="7e994-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7e994-122">-Tabell</span><span class="sxs-lookup"><span data-stu-id="7e994-122">-Table</span></span>
<span data-ttu-id="7e994-123">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="7e994-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="7e994-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e994-124">CommonParameters</span></span>
<span data-ttu-id="7e994-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e994-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e994-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e994-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e994-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e994-127">INPUTS</span></span>

### <span data-ttu-id="7e994-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e994-128">IStorageContext</span></span>

<span data-ttu-id="7e994-129">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7e994-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7e994-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="7e994-130">String</span></span>

<span data-ttu-id="7e994-131">Parametern ' tabell ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="7e994-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7e994-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e994-132">OUTPUTS</span></span>

### <span data-ttu-id="7e994-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7e994-133">System.String</span></span>

## <span data-ttu-id="7e994-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e994-134">NOTES</span></span>

## <span data-ttu-id="7e994-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e994-135">RELATED LINKS</span></span>

[<span data-ttu-id="7e994-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7e994-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7e994-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e994-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7e994-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7e994-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7e994-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7e994-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


