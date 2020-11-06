---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572340"
---
# <span data-ttu-id="56cad-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56cad-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="56cad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56cad-102">SYNOPSIS</span></span>
<span data-ttu-id="56cad-103">Hämtar den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="56cad-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="56cad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56cad-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="56cad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56cad-105">DESCRIPTION</span></span>
<span data-ttu-id="56cad-106">Cmdleten **Get-AzureStorageTableStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="56cad-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="56cad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56cad-107">EXAMPLES</span></span>

### <span data-ttu-id="56cad-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="56cad-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="56cad-109">Det här kommandot får åtkomst principen med namnet Policy50 i lagrings tabellen med namnet Table02.</span><span class="sxs-lookup"><span data-stu-id="56cad-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="56cad-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="56cad-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="56cad-111">Det här kommandot får alla åtkomst principer i tabellen som heter Table02.</span><span class="sxs-lookup"><span data-stu-id="56cad-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="56cad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56cad-112">PARAMETERS</span></span>

### <span data-ttu-id="56cad-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="56cad-113">-Context</span></span>
<span data-ttu-id="56cad-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="56cad-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="56cad-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="56cad-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="56cad-116">-Princip</span><span class="sxs-lookup"><span data-stu-id="56cad-116">-Policy</span></span>
<span data-ttu-id="56cad-117">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="56cad-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="56cad-118">-Tabell</span><span class="sxs-lookup"><span data-stu-id="56cad-118">-Table</span></span>
<span data-ttu-id="56cad-119">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="56cad-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="56cad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cad-120">CommonParameters</span></span>
<span data-ttu-id="56cad-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56cad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cad-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56cad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cad-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56cad-123">INPUTS</span></span>

## <span data-ttu-id="56cad-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56cad-124">OUTPUTS</span></span>

## <span data-ttu-id="56cad-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56cad-125">NOTES</span></span>

## <span data-ttu-id="56cad-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56cad-126">RELATED LINKS</span></span>

[<span data-ttu-id="56cad-127">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56cad-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="56cad-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56cad-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="56cad-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56cad-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="56cad-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="56cad-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


