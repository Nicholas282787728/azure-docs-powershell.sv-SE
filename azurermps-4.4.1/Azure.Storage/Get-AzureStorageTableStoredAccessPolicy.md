---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755311"
---
# <span data-ttu-id="11991-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11991-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="11991-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11991-102">SYNOPSIS</span></span>
<span data-ttu-id="11991-103">Hämtar den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="11991-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11991-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11991-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="11991-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11991-105">DESCRIPTION</span></span>
<span data-ttu-id="11991-106">Cmdleten **Get-AzureStorageTableStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="11991-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="11991-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11991-107">EXAMPLES</span></span>

### <span data-ttu-id="11991-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="11991-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="11991-109">Det här kommandot får åtkomst principen med namnet Policy50 i lagrings tabellen med namnet Table02.</span><span class="sxs-lookup"><span data-stu-id="11991-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="11991-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="11991-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="11991-111">Det här kommandot får alla åtkomst principer i tabellen som heter Table02.</span><span class="sxs-lookup"><span data-stu-id="11991-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="11991-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11991-112">PARAMETERS</span></span>

### <span data-ttu-id="11991-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="11991-113">-Context</span></span>
<span data-ttu-id="11991-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="11991-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="11991-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="11991-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="11991-116">-Princip</span><span class="sxs-lookup"><span data-stu-id="11991-116">-Policy</span></span>
<span data-ttu-id="11991-117">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="11991-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11991-118">-Tabell</span><span class="sxs-lookup"><span data-stu-id="11991-118">-Table</span></span>
<span data-ttu-id="11991-119">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="11991-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="11991-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11991-120">CommonParameters</span></span>
<span data-ttu-id="11991-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11991-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11991-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11991-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11991-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11991-123">INPUTS</span></span>

### <span data-ttu-id="11991-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11991-124">IStorageContext</span></span>

<span data-ttu-id="11991-125">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11991-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="11991-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="11991-126">String</span></span>

<span data-ttu-id="11991-127">Parametern ' tabell ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="11991-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="11991-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11991-128">OUTPUTS</span></span>

### <span data-ttu-id="11991-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="11991-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="11991-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11991-130">NOTES</span></span>

## <span data-ttu-id="11991-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11991-131">RELATED LINKS</span></span>

[<span data-ttu-id="11991-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11991-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11991-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11991-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11991-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11991-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11991-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="11991-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


