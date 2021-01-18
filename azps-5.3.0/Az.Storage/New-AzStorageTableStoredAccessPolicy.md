---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525322"
---
# <span data-ttu-id="3ecf4-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ecf4-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3ecf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ecf4-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecf4-103">Skapar en lagrad åtkomst princip för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="3ecf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ecf4-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ecf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ecf4-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecf4-106">Cmdleten **New-AzStorageTableStoredAccessPolicy** skapar en lagrad åtkomst policy för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="3ecf4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ecf4-107">EXAMPLES</span></span>

### <span data-ttu-id="3ecf4-108">Exempel 1: skapa en lagrad åtkomst princip i en tabell</span><span class="sxs-lookup"><span data-stu-id="3ecf4-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="3ecf4-109">Det här kommandot skapar en åtkomst princip med namnet Policy02 i lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="3ecf4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ecf4-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecf4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3ecf4-111">-Context</span></span>
<span data-ttu-id="3ecf4-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3ecf4-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ecf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecf4-114">-DefaultProfile</span></span>
<span data-ttu-id="3ecf4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ecf4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3ecf4-116">-ExpiryTime</span></span>
<span data-ttu-id="3ecf4-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3ecf4-118">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3ecf4-118">-Permission</span></span>
<span data-ttu-id="3ecf4-119">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="3ecf4-120">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="3ecf4-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3ecf4-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="3ecf4-121">-Policy</span></span>
<span data-ttu-id="3ecf4-122">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="3ecf4-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3ecf4-123">-StartTime</span></span>
<span data-ttu-id="3ecf4-124">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3ecf4-125">-Tabell</span><span class="sxs-lookup"><span data-stu-id="3ecf4-125">-Table</span></span>
<span data-ttu-id="3ecf4-126">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="3ecf4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecf4-127">CommonParameters</span></span>
<span data-ttu-id="3ecf4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecf4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecf4-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecf4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecf4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ecf4-130">INPUTS</span></span>

### <span data-ttu-id="3ecf4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3ecf4-131">System.String</span></span>

### <span data-ttu-id="3ecf4-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ecf4-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3ecf4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ecf4-133">OUTPUTS</span></span>

### <span data-ttu-id="3ecf4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ecf4-134">System.String</span></span>

## <span data-ttu-id="3ecf4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ecf4-135">NOTES</span></span>

## <span data-ttu-id="3ecf4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ecf4-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ecf4-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ecf4-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3ecf4-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ecf4-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3ecf4-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ecf4-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3ecf4-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ecf4-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


