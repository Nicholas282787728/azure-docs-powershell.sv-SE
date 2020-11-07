---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: e2e1f8952e0b785c5856585ad3e3371074194afd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746319"
---
# <span data-ttu-id="a2c4f-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c4f-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a2c4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c4f-103">Skapar en lagrad åtkomst princip för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="a2c4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2c4f-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c4f-106">Cmdleten **New-AzStorageTableStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="a2c4f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="a2c4f-108">Exempel 1: skapa en lagrad åtkomst princip i en tabell</span><span class="sxs-lookup"><span data-stu-id="a2c4f-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="a2c4f-109">Det här kommandot skapar en åtkomst princip med namnet Policy02 i lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="a2c4f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="a2c4f-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a2c4f-111">-Context</span></span>
<span data-ttu-id="a2c4f-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a2c4f-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a2c4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c4f-114">-DefaultProfile</span></span>
<span data-ttu-id="a2c4f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c4f-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a2c4f-116">-ExpiryTime</span></span>
<span data-ttu-id="a2c4f-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a2c4f-118">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="a2c4f-118">-Permission</span></span>
<span data-ttu-id="a2c4f-119">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="a2c4f-120">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="a2c4f-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a2c4f-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="a2c4f-121">-Policy</span></span>
<span data-ttu-id="a2c4f-122">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="a2c4f-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a2c4f-123">-StartTime</span></span>
<span data-ttu-id="a2c4f-124">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a2c4f-125">-Tabell</span><span class="sxs-lookup"><span data-stu-id="a2c4f-125">-Table</span></span>
<span data-ttu-id="a2c4f-126">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="a2c4f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c4f-127">CommonParameters</span></span>
<span data-ttu-id="a2c4f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c4f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c4f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c4f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c4f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2c4f-130">INPUTS</span></span>

### <span data-ttu-id="a2c4f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c4f-131">System.String</span></span>

### <span data-ttu-id="a2c4f-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2c4f-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2c4f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2c4f-133">OUTPUTS</span></span>

### <span data-ttu-id="a2c4f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c4f-134">System.String</span></span>

## <span data-ttu-id="a2c4f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2c4f-135">NOTES</span></span>

## <span data-ttu-id="a2c4f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2c4f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2c4f-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c4f-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a2c4f-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2c4f-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a2c4f-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c4f-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a2c4f-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c4f-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


