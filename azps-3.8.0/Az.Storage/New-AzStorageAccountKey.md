---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090871"
---
# <span data-ttu-id="4cc57-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4cc57-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="4cc57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cc57-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc57-103">Återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="4cc57-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="4cc57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cc57-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cc57-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc57-106">Cmdleten **New-AzStorageAccountKey** återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="4cc57-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="4cc57-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cc57-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc57-108">Exempel 1: återskapa en lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="4cc57-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="4cc57-109">Det här kommandot återskapar en lagrings plats för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4cc57-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="4cc57-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cc57-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc57-111">-DefaultProfile</span></span>
<span data-ttu-id="4cc57-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc57-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc57-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cc57-113">-KeyName</span></span>
<span data-ttu-id="4cc57-114">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4cc57-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="4cc57-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4cc57-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4cc57-116">key1</span><span class="sxs-lookup"><span data-stu-id="4cc57-116">key1</span></span>
- <span data-ttu-id="4cc57-117">key2</span><span class="sxs-lookup"><span data-stu-id="4cc57-117">key2</span></span>

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

### <span data-ttu-id="4cc57-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cc57-118">-Name</span></span>
<span data-ttu-id="4cc57-119">Anger namnet på det lagrings konto som du vill återskapa en lagrings plats för.</span><span class="sxs-lookup"><span data-stu-id="4cc57-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="4cc57-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc57-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cc57-121">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4cc57-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="4cc57-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc57-122">CommonParameters</span></span>
<span data-ttu-id="4cc57-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc57-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc57-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc57-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc57-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cc57-125">INPUTS</span></span>

### <span data-ttu-id="4cc57-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc57-126">System.String</span></span>

## <span data-ttu-id="4cc57-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cc57-127">OUTPUTS</span></span>

### <span data-ttu-id="4cc57-128">Microsoft. Azure. Management. Storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="4cc57-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="4cc57-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cc57-129">NOTES</span></span>

## <span data-ttu-id="4cc57-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cc57-130">RELATED LINKS</span></span>

[<span data-ttu-id="4cc57-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4cc57-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
