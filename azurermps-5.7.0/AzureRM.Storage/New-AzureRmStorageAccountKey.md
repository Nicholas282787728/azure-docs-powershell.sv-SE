---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580940"
---
# <span data-ttu-id="d7c68-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d7c68-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="d7c68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7c68-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c68-103">Återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="d7c68-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7c68-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d7c68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7c68-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c68-106">Cmdleten **New-AzureRmStorageAccountKey** återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="d7c68-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d7c68-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7c68-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c68-108">Exempel 1: återskapa en lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="d7c68-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="d7c68-109">Det här kommandot återskapar en lagrings plats för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d7c68-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="d7c68-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7c68-110">PARAMETERS</span></span>

### <span data-ttu-id="d7c68-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7c68-111">-KeyName</span></span>
<span data-ttu-id="d7c68-112">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d7c68-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d7c68-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d7c68-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7c68-114">key1</span><span class="sxs-lookup"><span data-stu-id="d7c68-114">key1</span></span>
- <span data-ttu-id="d7c68-115">key2</span><span class="sxs-lookup"><span data-stu-id="d7c68-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c68-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7c68-116">-Name</span></span>
<span data-ttu-id="d7c68-117">Anger namnet på det lagrings konto som du vill återskapa en lagrings plats för.</span><span class="sxs-lookup"><span data-stu-id="d7c68-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c68-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c68-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7c68-119">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d7c68-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c68-120">CommonParameters</span></span>
<span data-ttu-id="d7c68-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c68-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c68-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c68-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7c68-123">INPUTS</span></span>

### <span data-ttu-id="d7c68-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7c68-124">None</span></span>
<span data-ttu-id="d7c68-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d7c68-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7c68-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7c68-126">OUTPUTS</span></span>

## <span data-ttu-id="d7c68-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7c68-127">NOTES</span></span>

## <span data-ttu-id="d7c68-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7c68-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7c68-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d7c68-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
