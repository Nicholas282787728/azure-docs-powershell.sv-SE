---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 39e83844898771d25c5e2f8a62e4814b36b5e85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919517"
---
# <span data-ttu-id="00d03-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00d03-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="00d03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00d03-102">SYNOPSIS</span></span>
<span data-ttu-id="00d03-103">Skapar en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="00d03-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="00d03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00d03-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00d03-105">DESCRIPTION</span></span>
<span data-ttu-id="00d03-106">Cmdleten **New-AzStorageQueueStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="00d03-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="00d03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00d03-107">EXAMPLES</span></span>

### <span data-ttu-id="00d03-108">Exempel 1: skapa en lagrad åtkomst princip i en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="00d03-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="00d03-109">Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="00d03-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="00d03-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00d03-110">PARAMETERS</span></span>

### <span data-ttu-id="00d03-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="00d03-111">-Context</span></span>
<span data-ttu-id="00d03-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="00d03-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="00d03-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="00d03-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="00d03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d03-114">-DefaultProfile</span></span>
<span data-ttu-id="00d03-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00d03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00d03-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="00d03-116">-ExpiryTime</span></span>
<span data-ttu-id="00d03-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="00d03-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="00d03-118">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="00d03-118">-Permission</span></span>
<span data-ttu-id="00d03-119">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="00d03-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="00d03-120">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="00d03-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="00d03-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="00d03-121">-Policy</span></span>
<span data-ttu-id="00d03-122">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="00d03-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="00d03-123">-Kö</span><span class="sxs-lookup"><span data-stu-id="00d03-123">-Queue</span></span>
<span data-ttu-id="00d03-124">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="00d03-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="00d03-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="00d03-125">-StartTime</span></span>
<span data-ttu-id="00d03-126">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="00d03-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="00d03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d03-127">CommonParameters</span></span>
<span data-ttu-id="00d03-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d03-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d03-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d03-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00d03-130">INPUTS</span></span>

### <span data-ttu-id="00d03-131">System. String</span><span class="sxs-lookup"><span data-stu-id="00d03-131">System.String</span></span>

### <span data-ttu-id="00d03-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="00d03-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="00d03-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00d03-133">OUTPUTS</span></span>

### <span data-ttu-id="00d03-134">System. String</span><span class="sxs-lookup"><span data-stu-id="00d03-134">System.String</span></span>

## <span data-ttu-id="00d03-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00d03-135">NOTES</span></span>

## <span data-ttu-id="00d03-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00d03-136">RELATED LINKS</span></span>

[<span data-ttu-id="00d03-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00d03-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="00d03-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="00d03-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="00d03-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00d03-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="00d03-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00d03-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

