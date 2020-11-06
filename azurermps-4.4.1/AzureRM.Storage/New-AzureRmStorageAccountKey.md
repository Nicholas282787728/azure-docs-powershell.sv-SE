---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586144"
---
# <span data-ttu-id="66f14-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="66f14-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="66f14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66f14-102">SYNOPSIS</span></span>
<span data-ttu-id="66f14-103">Återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="66f14-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66f14-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66f14-105">DESCRIPTION</span></span>
<span data-ttu-id="66f14-106">Cmdleten **New-AzureRmStorageAccountKey** återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="66f14-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="66f14-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66f14-107">EXAMPLES</span></span>

### <span data-ttu-id="66f14-108">Exempel 1: återskapa en lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="66f14-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="66f14-109">Det här kommandot återskapar en lagrings plats för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="66f14-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="66f14-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66f14-110">PARAMETERS</span></span>

### <span data-ttu-id="66f14-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="66f14-111">-KeyName</span></span>
<span data-ttu-id="66f14-112">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="66f14-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="66f14-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="66f14-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66f14-114">key1</span><span class="sxs-lookup"><span data-stu-id="66f14-114">key1</span></span> 
- <span data-ttu-id="66f14-115">key2</span><span class="sxs-lookup"><span data-stu-id="66f14-115">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f14-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="66f14-116">-Name</span></span>
<span data-ttu-id="66f14-117">Anger namnet på det lagrings konto som du vill återskapa en lagrings plats för.</span><span class="sxs-lookup"><span data-stu-id="66f14-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f14-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f14-118">-ResourceGroupName</span></span>
<span data-ttu-id="66f14-119">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="66f14-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f14-120">-DefaultProfile</span></span>
<span data-ttu-id="66f14-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66f14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f14-122">CommonParameters</span></span>
<span data-ttu-id="66f14-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f14-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f14-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f14-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66f14-125">INPUTS</span></span>

## <span data-ttu-id="66f14-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66f14-126">OUTPUTS</span></span>

## <span data-ttu-id="66f14-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66f14-127">NOTES</span></span>

## <span data-ttu-id="66f14-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66f14-128">RELATED LINKS</span></span>

[<span data-ttu-id="66f14-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="66f14-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)


