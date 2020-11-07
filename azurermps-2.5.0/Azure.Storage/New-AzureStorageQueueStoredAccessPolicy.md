---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 054a5d979a13f5592f062f729e4c8c393a35134a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930390"
---
# <span data-ttu-id="a5e54-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5e54-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a5e54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5e54-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e54-103">Skapar en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="a5e54-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5e54-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e54-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5e54-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e54-106">Cmdleten **New-AzureStorageQueueStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="a5e54-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a5e54-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5e54-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e54-108">Exempel 1: skapa en lagrad åtkomst princip i en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="a5e54-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="a5e54-109">Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="a5e54-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="a5e54-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5e54-110">PARAMETERS</span></span>

### <span data-ttu-id="a5e54-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a5e54-111">-Context</span></span>
<span data-ttu-id="a5e54-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="a5e54-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a5e54-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a5e54-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a5e54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e54-114">-DefaultProfile</span></span>
<span data-ttu-id="a5e54-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e54-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e54-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a5e54-116">-ExpiryTime</span></span>
<span data-ttu-id="a5e54-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="a5e54-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a5e54-118">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="a5e54-118">-Permission</span></span>
<span data-ttu-id="a5e54-119">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="a5e54-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="a5e54-120">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="a5e54-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a5e54-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="a5e54-121">-Policy</span></span>
<span data-ttu-id="a5e54-122">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="a5e54-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="a5e54-123">-Kö</span><span class="sxs-lookup"><span data-stu-id="a5e54-123">-Queue</span></span>
<span data-ttu-id="a5e54-124">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="a5e54-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a5e54-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a5e54-125">-StartTime</span></span>
<span data-ttu-id="a5e54-126">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="a5e54-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a5e54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e54-127">CommonParameters</span></span>
<span data-ttu-id="a5e54-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e54-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e54-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e54-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5e54-130">INPUTS</span></span>

### <span data-ttu-id="a5e54-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e54-131">System.String</span></span>

### <span data-ttu-id="a5e54-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5e54-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5e54-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5e54-133">OUTPUTS</span></span>

### <span data-ttu-id="a5e54-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e54-134">System.String</span></span>

## <span data-ttu-id="a5e54-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5e54-135">NOTES</span></span>

## <span data-ttu-id="a5e54-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5e54-136">RELATED LINKS</span></span>

[<span data-ttu-id="a5e54-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5e54-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a5e54-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5e54-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a5e54-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5e54-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a5e54-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5e54-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


