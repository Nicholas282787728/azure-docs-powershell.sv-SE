---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930422"
---
# <span data-ttu-id="fdda8-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdda8-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fdda8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdda8-102">SYNOPSIS</span></span>
<span data-ttu-id="fdda8-103">Hämtar den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="fdda8-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdda8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdda8-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdda8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdda8-105">DESCRIPTION</span></span>
<span data-ttu-id="fdda8-106">Cmdleten **Get-AzureStorageTableStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="fdda8-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="fdda8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdda8-107">EXAMPLES</span></span>

### <span data-ttu-id="fdda8-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="fdda8-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="fdda8-109">Det här kommandot får åtkomst principen med namnet Policy50 i lagrings tabellen med namnet Table02.</span><span class="sxs-lookup"><span data-stu-id="fdda8-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="fdda8-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="fdda8-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="fdda8-111">Det här kommandot får alla åtkomst principer i tabellen som heter Table02.</span><span class="sxs-lookup"><span data-stu-id="fdda8-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="fdda8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdda8-112">PARAMETERS</span></span>

### <span data-ttu-id="fdda8-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fdda8-113">-Context</span></span>
<span data-ttu-id="fdda8-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="fdda8-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fdda8-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="fdda8-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fdda8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdda8-116">-DefaultProfile</span></span>
<span data-ttu-id="fdda8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdda8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdda8-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="fdda8-118">-Policy</span></span>
<span data-ttu-id="fdda8-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="fdda8-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdda8-120">-Tabell</span><span class="sxs-lookup"><span data-stu-id="fdda8-120">-Table</span></span>
<span data-ttu-id="fdda8-121">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fdda8-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="fdda8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdda8-122">CommonParameters</span></span>
<span data-ttu-id="fdda8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdda8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdda8-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdda8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdda8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdda8-125">INPUTS</span></span>

### <span data-ttu-id="fdda8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fdda8-126">System.String</span></span>

### <span data-ttu-id="fdda8-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdda8-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fdda8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdda8-128">OUTPUTS</span></span>

### <span data-ttu-id="fdda8-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="fdda8-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="fdda8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdda8-130">NOTES</span></span>

## <span data-ttu-id="fdda8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdda8-131">RELATED LINKS</span></span>

[<span data-ttu-id="fdda8-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdda8-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fdda8-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdda8-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fdda8-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdda8-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fdda8-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdda8-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


