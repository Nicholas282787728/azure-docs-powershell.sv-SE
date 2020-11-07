---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931082"
---
# <span data-ttu-id="ab3e2-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab3e2-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ab3e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3e2-103">Skapar en lagrad åtkomst princip för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab3e2-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab3e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab3e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3e2-106">Cmdleten **New-AzureStorageTableStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ab3e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab3e2-107">EXAMPLES</span></span>

### <span data-ttu-id="ab3e2-108">Exempel 1: skapa en lagrad åtkomst princip i en tabell</span><span class="sxs-lookup"><span data-stu-id="ab3e2-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="ab3e2-109">Det här kommandot skapar en åtkomst princip med namnet Policy02 i lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="ab3e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab3e2-110">PARAMETERS</span></span>

### <span data-ttu-id="ab3e2-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ab3e2-111">-Context</span></span>
<span data-ttu-id="ab3e2-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ab3e2-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ab3e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3e2-114">-DefaultProfile</span></span>
<span data-ttu-id="ab3e2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab3e2-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ab3e2-116">-ExpiryTime</span></span>
<span data-ttu-id="ab3e2-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3e2-118">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="ab3e2-118">-Permission</span></span>
<span data-ttu-id="ab3e2-119">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="ab3e2-120">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="ab3e2-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3e2-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="ab3e2-121">-Policy</span></span>
<span data-ttu-id="ab3e2-122">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3e2-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ab3e2-123">-StartTime</span></span>
<span data-ttu-id="ab3e2-124">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3e2-125">-Tabell</span><span class="sxs-lookup"><span data-stu-id="ab3e2-125">-Table</span></span>
<span data-ttu-id="ab3e2-126">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3e2-127">CommonParameters</span></span>
<span data-ttu-id="ab3e2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3e2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3e2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3e2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab3e2-130">INPUTS</span></span>

### <span data-ttu-id="ab3e2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ab3e2-131">System.String</span></span>

### <span data-ttu-id="ab3e2-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab3e2-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab3e2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab3e2-133">OUTPUTS</span></span>

### <span data-ttu-id="ab3e2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab3e2-134">System.String</span></span>

## <span data-ttu-id="ab3e2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab3e2-135">NOTES</span></span>

## <span data-ttu-id="ab3e2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab3e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab3e2-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab3e2-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ab3e2-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab3e2-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ab3e2-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab3e2-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ab3e2-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab3e2-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


